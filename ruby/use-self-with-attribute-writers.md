You _must_ use `self.` when calling an attribute writer from within an instance method. Otherwise, you'll assign to a local variable.

```ruby
class MyClass
  attr_writer :my_attribute

  def set_my_attribute
    self.my_attribute = "sets my attribute"
  end

  def do_not_set_my_attribute
    my_attribute = "doesn't set my attribute"
  end
end
```

[2013-11-08]
