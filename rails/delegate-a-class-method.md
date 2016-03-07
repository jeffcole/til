You can delegate a class method.

```ruby
class << self
  delegate :some_method, to: :SomeClass
end
```

Note that the `:to` option can also be a method that returns a class.

[2015-01-23]
