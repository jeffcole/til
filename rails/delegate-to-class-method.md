You can delegate to a class method.

```ruby
class << self
  delegate :some_method, to: :SomeClass
end
```

Here, `SomeClass` could also be a method that returns a class.

[2015-01-23]
