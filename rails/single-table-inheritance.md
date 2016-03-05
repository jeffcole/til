In Single Table Inheritance (STI), "single table" means there is only one table shared between multiple models (subclasses of the parent model or table). A type column in the table differentiates between each subclass. An explicit subclass is required for each type.

Rule of thumb: if you have many fields in your table that only apply to one subclass, STI may not be the best choice.

[2013-09-23]
