# Index

In a database - it is a special data structure that stores a small portion of the collection's data set in an easy to traverse form. It **optimizes** query by making some extra data that cuts the time needed when locating an indexed field.

```JavaScript
// Creating single field index
db.trips.createIndex({"birth year": 1})

// Creating compound index
db.trips.createIndex({"start station id": 1, "birth year": 1})

// The index can be in descending order
db.trips.createIndex({"birth year": -1})
```

## Comparison of a non-indexed and an indexed field

- For a non-indexed field, you need to go through each documents one-by-one and check the field.
- For an indexed field, you can refer to the index and search it in a more efficient data structure for searching.
![](assets/20221020194240%20Index%20comparison.png)

## When to index

Use it when a field is accessed and sorted often. Even if some of the fields are not indexed, some indexed fields can help with the query time of the database.