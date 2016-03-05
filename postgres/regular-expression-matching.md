You can perform a case insensitive regular expression search with `~*`.

This example will return rows where `first_name` is `'Jeffrey'`.
```sql
SELECT *
FROM people
WHERE first_name ~* 'fre'
```

[2014-02-24]
