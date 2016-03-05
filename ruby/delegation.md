Use `Forwardable` and `def_delegators` when we only want to delegate a few methods of a PORO to a component. This allows us to be explicit about what we're delegating.

Contrast this with `SimpleDelegator` which passes through all undefined methods to the wrapped object.

In Rails, the `delegate` method provides this functionality without needing to `extend Forwardable`.

[2015-11-17]
