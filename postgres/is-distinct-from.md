It's easy to forget that since "the null value represents an unknown value, and it is not known whether two unknown values are equal," the result of the inequality operator is falsy when comparing anything to `NULL`.

For instance, sometimes we want to write the following.

```sql
WHERE (t.field <> u.field)
```

If either field is `NULL`, then `NULL` is yielded by the inequality operator, and the comparison is effectively falsy — when intuitively we might expect it to be truthy in the case that e.g. `t.field` has a known value and `u.field` is `NULL`.

We can cleanly achieve our intended semantics without worrying about `NULL` by using the `IS DISTINCT FROM` predicate supported by Postgres.

```sql
WHERE (t.field IS DISTINCT FROM u.field)
```

See the [PostgreSQL Comparison Functions and Operators docs][docs] for more information.

[docs]: https://www.postgresql.org/docs/current/static/functions-comparison.html
