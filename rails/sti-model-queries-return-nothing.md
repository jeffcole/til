If queries on a subclass of a STI class (e.g. a subclass created for a specific scope) aren't returning any records, do the following.

```ruby
class MyClass < ClassUsingSTI
  self.inheritance_column = :_disabled
end
```

This is necessary to override the STI `type` column.

[2015-06-16]
