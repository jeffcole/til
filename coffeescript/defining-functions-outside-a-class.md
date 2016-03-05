Defining a function outside of a class uses different syntax than defining a method inside of a class. Methods use a colon, while functions use an equals sign.

```coffee
class MyClass
  myMethod: ->
    console.log "Hello from MyClass#myMethod"

myFunction = ->
  console.log "Hello from myFunction"
```

[2014-06-09]
