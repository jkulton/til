# psql Expanded Display

`psql` offers an expanded display mode which reformats query results in an alternative format that is more efficient for narrower displays.


```
db=# \x
Expanded display is on.
```

```
db=# SELECT * FROM users;
-[ RECORD 1 ]-
username       | jane
favorite_color | blue
-[ RECORD 2 ]-
username       | jon
favorite_color | black
```