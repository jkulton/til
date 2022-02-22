# Create Index Without Locking Table

Creating an index on a column typically locks a table from inserts, updates, or deletes
for the entire index process. For tables with less data or typical load this might be
acceptable. For tables with lots of data or under heavy query load you might consider
using PostgreSQL's `CONCURRENTLY` create index option.

```sql
CREATE INDEX CONCURRENTLY idx_created_at ON users(created_at);
```

This allows for creating an index without needing a table lock for the entire index process.

There are some caveats worth considering that are available in [the docs](https://www.postgresql.org/docs/9.1/sql-createindex.html).
