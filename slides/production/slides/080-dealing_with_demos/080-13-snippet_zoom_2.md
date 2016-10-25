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

The idea of snippet zoom is to show a little code at a time, and elide portions of code
which are too long to show on the screen.  Do this in a way which lets students see 
function start/end.  Some IDEs will help you do this by letting you "roll up" portions
of the code.