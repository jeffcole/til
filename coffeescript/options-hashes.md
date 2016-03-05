CoffeeScript supports passing a curly-brace-less object as the last argument to a function, like Ruby.

```coffee
myFunction = (param, options) ->
  console.log param
  console.log options.someKey
  console.log options.anotherKey

myFunction "Hello", someKey: "from", anotherKey: "myFunction"
```

[2013-09-12]
