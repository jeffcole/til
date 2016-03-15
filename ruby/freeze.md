You can get some peace of mind that your objects won't be modified after calling `#freeze` on them. This is handy for when you want an immutable object.

```ruby
Config = Struct.new(:host, :port)
config = Config.new("https://www.example.com", 443).freeze

config.port = 80
# => can't modify frozen #<Class:0x007ff0c9dc72f8> (RuntimeError)
```
