It's a good idea to qualify references to things that come from modules outside the current one. This makes it easier to see where things come from without having to go hunting.

Here's how we qualify references to the types defined by a union type from another module.

```elm
-- Types.elm

module Types exposing (..)

type Visibility
    = Active
    | Completed
```

```elm
-- Main.elm

import Types exposing (Visibility(Active, Completed))

exclaim : Visiblity -> String
exclaim visibility =
    case visibility of
        Types.Active ->
            "Active!"

        Types.Completed ->
            "Completed!"
```
