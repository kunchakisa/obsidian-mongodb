# Array Operators

`$size` - compares the size of the array. Value is a number or an operator.
`$all` - compares the content of the arrays in an **unordered manner**. Value accepts an array of the required matches.
`$elemMatch` - matches if the specified array has an object with the expression inside. Value is a query object. (see examples). This can also be used in [Query Projection](../Query%20Projection.md).

## Note

Querying an array field using an array returns only the exact match

```BASH
# Returns only when the array field has the exact same array
{"<array field>": [...]}
```

## Codes Used

**`$elemMatch`**
```BASH
# Match the documents where the array scores has an object with a type field with "extra credit"
db.grades.find({
	"scores": {
		"$elemMatch":
				{ "type": "extra credit" }
	}
}).pretty()
```