If when you try to update a gem with,

```bash
bundle update gem-name
```

you get something similar to,

```
Bundler could not find compatible versions for gem "rspec-mocks"
```

it might be because of a conflicting locked dependency. You can try to remedy this by upgrading a whole bundle group at once.

```
bundle update --group test
```

[2015-12-03]
