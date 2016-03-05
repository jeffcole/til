Lazy lookup makes it easy to translate keys.

It is only available in views.

```yaml
# config/locales/views/posts/en.yml

en:
  posts:
    index:
      title: "Really Neat Posts"
```

```erb
<!-- app/views/posts/index.html.erb -->

<%= t ".title" %>
```

[2014-12-19]
