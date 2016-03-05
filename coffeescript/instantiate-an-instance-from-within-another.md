Instantiate an instance from within another instance.

```coffee
class MyClass
  constructor: (params) ->
    console.log("Instantiating a MyClass")

  anotherPlease: (params)->
    new @constructor(params)
```

[2015-07-21]
