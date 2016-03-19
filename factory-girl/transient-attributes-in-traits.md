You can use transient attributes in traits. This is useful for succinctly passing attributes to associated objects.

```ruby
factory :invoice do
  trait :with_amount do
    transient do
      amount 1
    end

    after(:create) do |invoice, evaluator|
      create :line_item, invoice: invoice, amount: evaluator.amount
    end
  end
end

create :invoice, :with_amount, amount: 2
```
