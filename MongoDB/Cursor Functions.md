# Cursor Functions

Cursor are the pointer to a result of a query. When we say cursor functions/methods, they are functions we can use to the cursor output of a command in the `mongo shell`.

- `count()` - returns the number of the documents in the resulting query.
- `sort()` - arrange the results by the specified field and order pair
- `limit()` - restrict the number of the results
- `skip()` - skips the specified amount of data in the results. Useful with the `sort()` command.
- `pretty()` - returns the documents result from cursor formatted for **ease of reading**.

## Sample Codes

``` JavaScript
// Returns the documents in pretty format
db.collection.find({...}).pretty()

// Returns the count
db.collection.find({...}).count()

// Sort the data by the population in increasing order
db.collection.find({...}).sort({pop: 1})
// Return the document with the least population record
db.collection.find({...}).sort({pop: 1}).limit(1)

// Return the documents with the 2nd and 3rd least population record
// This sorts the results in descending order first, then skip 1 document, and return two
db.collection.find({...}).sort({pop: -1}).skip(1).limit(2)
```