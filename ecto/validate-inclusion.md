[`Ecto.Changeset.validate_inclusion/4`](https://hexdocs.pm/ecto/Ecto.Changeset.html#validate_inclusion/4) does not require a field to be present.

```elixir
params = %{}

changeset =
  struct
  |> cast(params, [:type])
  |> validate_inclusion(:type, ["valid", "types"])

changeset.valid? # true
```

You must also add the field to the required validation.

```elixir
params = %{}

changeset =
  struct
  |> cast(params, [:type])
  |> validate_required(:type)
  |> validate_inclusion(:type, ["valid", "types"])

changeset.valid? # false
changeset.errors # [type: {"can't be blank", [validation: :required]}]
```
