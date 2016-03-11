The organization of your locale files is irrelevant to how translation keys are looked up. Rails will load all the files it can find and store all the keys and values together in a single structure.

We can tell Rails to load files in nested directories with the following:

```ruby
# config/application.rb

config.i18n_load_path += Dir[File.join(
  Rails.root, "config", "locales", "**", "*.yml"
)]
```

See http://guides.rubyonrails.org/i18n.html for more.
