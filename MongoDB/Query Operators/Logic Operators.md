# Logic Operators

- `$and` - match **all** the conditions of the specified query
- `$or` - **At least one** of the query clauses is matched
- `$nor` - **Fail to match both** given clauses
- `$not` - **Negates** the query requirement

## Implicit `$and`

**`$and`** is used as the default operator when an operator is not specified. The two queries below have the same effect.

```BASH
{sector: "Mobile Food Vendor - 881", result: "Warning"}

{"$and": [{sector: "Mobile Food Vendor - 881"}, {result: "Warning"}]}
```

Another example of Implicit `$and` is when we use multiple conditions in the same field. In this example, we need to find which student ids ad `> 25` and `< 100`.

```BASH
{"$and": [{"student_id": {"$gt":25}}, {"student_id": {"$lt": 100}}]}

# Better
{"student_id": {"$gt": 25, "$lt": 100}}
```

## Explicit `$and`

The case when you need to use an explicit `$and` operator is when you need to use the **same** operator more than once in the same query.

```BASH
# Example

{ "$and": [
	{ "$or" :[
		{ "dst_airport": "KZN" },
		{ "src_airport": "KZN" }
	] },
	{ "$or" :[
		{ "airplane": "CR2" },
		{ "airplane": "A81" }
	] }
]}
```