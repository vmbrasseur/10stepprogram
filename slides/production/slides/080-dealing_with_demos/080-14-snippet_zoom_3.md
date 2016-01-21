## Dealing With Demos

```sql
... (
select minstart,
        coalesce(conn_count,0) as conn_count,
        coalesce(disc_count,0) as disc_count
from log_minutes
        left outer join
        ( ... ) as conns
        on minstart = conns.contime
        left outer join
        ( ... ) as disconns
        on minstart = disconns.contime
) as connects,
( ... ) 
as start_connects;
```

note:

Who: Josh
