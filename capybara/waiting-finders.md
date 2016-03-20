Some of Capybara's finders will wait for elements to appear on the page, while others will not. `find` will wait, `first` and `all` will not. If you want to use `all`, you can call `find` first to get the waiting behavior.

```ruby
find(".transient")
all(".transient")
```

https://robots.thoughtbot.com/write-reliable-asynchronous-integration-tests-with-capybara
