From the [docs]:

> The complexity of `a ++ b` is proportional to `length(a)`, so avoid repeatedly appending to lists of arbitrary length, e.g. `list ++ [item]`.

> Instead, consider prepending via `[item | rest]` and then reversing.

This can have substantial performance implications when recursing.

Prefer

```elixir
def recurse(args) when base_case, do: []
def recurse(args) do
  [new_item | recurse(updated_params)]
end
```

over

```elixir
def recurse(args, acc) when base_case, do: acc
def recurse(args, acc) do
  recurse(updated_params, acc ++ [new_item])
end
```

for this reason.

[docs]: http://elixir-lang.org/docs/stable/elixir/Kernel.html#++/2
