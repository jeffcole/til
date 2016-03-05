You can use controller-specific layouts. For example, the `PostsController` class will use `app/views/layouts/posts.html.erb`.

You can also supply a method that will determine the layout at runtime.

```ruby
class PostsController < ApplicationController
  layout :posts_layout

  # ...

  private

  def posts_layout
    condition? ? "one_layout" : "another_layout"
  end
end
```

[2013-11-13]
