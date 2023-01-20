### Validation
---
> `save` and `update` they return **false** when validation fails and they don't actually perform any operations on the database. All of these have a bang counterpart (that is, `save!` and `update!`), which are stricter in that they raise the exception **ActiveRecord::RecordInvalid** if validation fails

> Finder methods that return a collection, such as `where` and `group`, return an instance of **ActiveRecord::Relation**

> `Customer.all.each` instructs Active Record to fetch the entire table in a single pass, build a model object per row, and then keep the entire array of model objects in memory. 
- The first method, find_each, retrieves a batch of records and then yields each record to the block individually as a model. 
- The second method, find_in_batches, retrieves a batch of records and then yields the entire batch to the block as an array of models.

> use `sanitize_sql_like` to escape wildcard characters in the relevant portion of the argument.

```ruby
Book.where("title LIKE ?",
  Book.sanitize_sql_like(params[:title]) + "%")
```
> Beginless and endless ranges are supported and can be used to build less/greater than conditions.
```ruby
Book.where(created_at: (Time.now.midnight - 1.day)..)
```
This would generate SQL like:
```sql
SELECT * FROM books WHERE books.created_at >= '2008-12-21 00:00:00'
```
> Use `limit` to specify the number of records to be retrieved, and use `offset`to specify the number of records to skip before starting to return the records.
```ruby
Customer.limit(5).offset(30)
```
> SQL uses the HAVING clause to specify conditions on the GROUP BY fields. You can add the HAVING clause to the SQL fired by the Model.find by adding the `having` method to the find.


```ruby
Order.select("created_at, sum(total) as total_price").
  group("created_at").having("sum(total) > ?", 200)
```
```sql
SELECT created_at as ordered_date, sum(total) as total_price
FROM orders
GROUP BY created_at
HAVING sum(total) > 200
```
### Locking
Active Record provides two locking mechanisms:

- Optimistic Locking
    - the table needs to have a column called lock_version of type integer
- Pessimistic Locking