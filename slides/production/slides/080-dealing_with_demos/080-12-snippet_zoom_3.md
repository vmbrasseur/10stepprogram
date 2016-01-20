## Dealing With Demos

```sql
... (
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
( ... ) 
as start_connects;
```

note:

Who: Josh
