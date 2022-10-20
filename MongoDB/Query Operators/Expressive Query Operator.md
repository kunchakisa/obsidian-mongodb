# Expressive Query Operator

To use expressive query operator, we use the `$expr` function. It let us use aggregation functions inside it.

## Some difference between normal query syntax and the Aggregation Pipeline

Aggregation function may differ to the normal function. For example, the syntax of the `$gt` function in MQL is `"fieldname": {"$gt": 5}`, but in aggregation pipeline, it is `$gt: ["$fieldname", 5]`. This is partly because the aggregation pipeline focuses on function use and parameters, while MQL is a simpler version that focuses more on fields.

### What does the `$` symbol do with the fieldname?

It tells the program that it is looking to the **value** in that field name. The `$` symbol can either refer to an operator name, or a field name.