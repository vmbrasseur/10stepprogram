## Dealing With Demos

```sql
create table reports.connections_by_minute as
select cast(minstart as time) as minstart, 
        start_count + sum( conn_count - disc_count ) 
        OVER ( order by minstart ) as conns
from (
select minstart,
        coalesce(conn_count,0) as conn_count,
        coalesce(disc_count,0) as disc_count
from log_minutes
        left outer join
        ( select date_trunc('minute', log_time) as contime,
                count(*) as conn_count
                from connections
                group by 1 ) as conns
        on minstart = conns.contime
        left outer join
        ( select date_trunc('minute', log_time) as contime,
                count(*) as disc_count
                from disconnections
                group by 1 ) as disconns
        on minstart = disconns.contime
) as connects,
( select count(*) 
  as start_count 
  from monitor.pg_stat_activity_start ) 
as start_connects;
```

note:

Who: Josh

As you can see by the scrollbars, this is WAY too much code for one slide.
While you can scroll, it's better to highlight the code you want to talk
about in a series of slides.  We call this "snippet zoom".
