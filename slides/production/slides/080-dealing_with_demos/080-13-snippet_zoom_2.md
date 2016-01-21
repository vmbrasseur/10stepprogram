## Dealing With Demos

```sql
create table reports.connections_by_minute as
select cast(minstart as time) as minstart, 
        start_count + sum( conn_count - disc_count ) 
        OVER ( order by minstart ) as conns
from (
...
) as connects,
( ... ) 
as start_connects;
```

note:

Who: Josh
