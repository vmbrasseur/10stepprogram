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

If you need to show more of the code, you can then expand and contract sections,
allowing you to display each section you're talking about in a large point size
on the screen.  