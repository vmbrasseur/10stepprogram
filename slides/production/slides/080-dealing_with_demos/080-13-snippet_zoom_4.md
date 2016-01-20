## Dealing With Demos

```sql
...
from (
...
) as connects,
( select count(*) 
  as start_count 
  from monitor.pg_stat_activity_start ) 
as start_connects;
```

note:

Who: Josh
