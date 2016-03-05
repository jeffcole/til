This is a SQL injection risk.

```ruby
Client.where("orders_count = #{some_string}")
```

This is not, because Rails will perform automatic escaping.

```ruby
Client.where("orders_count = ?", some_string)
```

[2015-01-12]
