# Updating Data in MongoDB

There are two commands to use to update documents in MongoDB, depending on the quantity of the documents you want to update.
- `updateOne()` - updates one of the filtered results. It is like the `findOne()` command.
- `updateMany()` - updates **all** of the filtered results. It is like the `find()` command.

When using these commands, the first argument is the query for the filter (see [Find Command](Find%20Command.md)'s query). The second command is the update operation that you want to do. Here are some of the operations that you can use:

```BASH
# Increments the value by the selected amount. Use negative values to subtract
{"$inc": {"<field1>": "<increment value>", "<field2>": "<increment>", ...}}

# Multiply the value by the selected amount. Use fractions to divide
{"$mul": {"<field1>": "<multiply value>", "<field2>": "<multiplier>", ...}}

# Sets field value to a new specified value
{"$set": {"<field1>": "<new value>", "<field2>": "<value>", ...}}

# Remove the value of fields. The values of the operations are just empty strings
{"$unset": {"<field1>": "", "<field2>": "", ...}}

# Adds an element to an array field
{"$push": {"<arrayfield1>": "<new item>", "<arrayfield2>": "<value>", ...}}

# Remove the last (with 1) or the first element (with -1) of an array field
{"$pop": {"<arrayfield>": 1, "<arrayfield>": -1, ...}}
```

### Notes

To specify a `<field>` in an embedded document or in an array, use [Dot Notation](Dot%20Notation.md).

## See Also
- [Updating Data with Data Explorer](../MongoDB%20Atlas/Updating%20Data%20with%20Data%20Explorer.md) - basic data updates. It only tackles updating one document at a time.