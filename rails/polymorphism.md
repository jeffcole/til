When using polymorphism in Active Record models, you add `type` and `id` columns to the interface table for the relationship (e.g. `rel_type` and `rel_id`). The model that corresponds to this table gets a `belongs_to` association with the name of the interface. Then the models that implement the interface have (one or many) association(s) to the interface as `relationship`.

[2013-09-23]
