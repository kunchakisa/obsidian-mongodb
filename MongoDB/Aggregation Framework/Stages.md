# Aggregation Stages

They are the objects that appear at the array passed to the `aggregate()` function.
```JavaScript
db.collection.aggregate( [ { <stage> }, ... ] )
```

For a more comprehensive list, visit the [source](https://www.mongodb.com/docs/manual/reference/operator/aggregation-pipeline/).

## Match Stage

Filters the document stream to allow only matching documents to pass unmodified into the next pipeline stage. `$match` uses standard MongoDB queries. For each input document, outputs either one document (a match) or zero documents (no match). 

This command is like the first argument in the `find()` command, where you declare the filter for your documents.

## Project Stage

Reshapes each document in the stream, such as by adding new fields or removing existing fields. For each input document, outputs one document.

This command is like the second argument in the `find()` command, where you can choose what fields of the result you only want to see.

## Group Stage

The `$group` stage is an operator that takes the incoming stream of data, and siphons it into multiple distinct reservoirs.

![](assets/20221020174823%20Group%20Visual.png)
### Sample Code

```JavaScript
// List the room types present in the database
{ $group: {_id: "$room_type"} }

// List the room types and count them in the database, a count field will appear at the result
{ $group: {_id: "$room_type"}. count: {$sum: 1} }
```

### Note

Non-filtering stages do not modify the original data. Instead, they work with the data that they get from the **previous pipeline**, which is stored in the cursor.

## See Also

- [Aggregation Operators](Operators.md)