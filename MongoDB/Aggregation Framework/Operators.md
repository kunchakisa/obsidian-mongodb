# Aggregation Operators

## `$sum` operator

It adds the array of expressions

**Syntax: **
```JavaScript
// In stages where there's a previous value, or where it is counting something
// This can also be used in other supported stages
{ $sum: <expression> }

// In other supported stages, this expression can also be used
{ $sum: [ <expression1>, <expression2> ... ] }
```
