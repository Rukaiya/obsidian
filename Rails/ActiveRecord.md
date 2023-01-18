### Validation
---
> `save` and `update` they return **false** when validation fails and they don't actually perform any operations on the database. All of these have a bang counterpart (that is, `save!` and `update!`), which are stricter in that they raise the exception **ActiveRecord::RecordInvalid** if validation fails

> Finder methods that return a collection, such as `where` and `group`, return an instance of **ActiveRecord::Relation**

> `Customer.all.each` instructs Active Record to fetch the entire table in a single pass, build a model object per row, and then keep the entire array of model objects in memory. 
- The first method, find_each, retrieves a batch of records and then yields each record to the block individually as a model. 
- The second method, find_in_batches, retrieves a batch of records and then yields the entire batch to the block as an array of models.
