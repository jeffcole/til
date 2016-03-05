You can configure multiple allowed messages in a single call.

```ruby
allow(object).to receive_messages(
  some_message: "Hello",
  another_message: "Howdy"
)
```

[2015-10-19]
