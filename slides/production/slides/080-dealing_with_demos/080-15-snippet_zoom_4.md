## Dealing With Demos

```sql
...
from log_minutes
        left outer join
        ( select date_trunc('minute', log_time) 
          as contime,
                count(*) as conn_count
                from connections
                group by 1 ) as conns
) as connects ...
```

note:

Who: Josh

And continue.

Some presentation software will, alternately, let you graphically
"zoom" on portions of the code; this can also work if used well.