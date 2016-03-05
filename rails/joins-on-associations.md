Active Record joins must use the exact name of the association (singular or plural).


You can specify conditions on joined tables

```ruby
joins(:comments).where(comments: { flagged: true })
```

You can nest the joins as far as you need to.

```ruby
joins(comments: { author: :profile })
```

[2013-10-03]
