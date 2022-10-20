You see some operators in the `update()` command that starts with the `$` sign right? Query operators are like that too, but they modify the behavior of the filter.

## Subtopics

- [Comparison Operators](Query%20Operators/Comparison%20Operators.md)
- [Logic Operators](Query%20Operators/Logic%20Operators.md)
- [Expressive Query Operator](Query%20Operators/Expressive%20Query%20Operator.md)
- [Array Operators](Query%20Operators/Array%20Operators.md)
- Sub-documents - [Dot Notation](Dot%20Notation.md)

## Query Syntax

**Conditional Operators**
```BASH
# Syntax for conditional operators
{ "<field>": { "$<operator>":"<value>" } }

# Find a bike rent that lasted for only 70 seconds or less
{ "tripduration": {"$lte":70} }

# Add a query that only shows rents that aren't covered by subscription
{ "tripduration": {"$lte":70}, "usertype": { "$ne": "Subscriber" }
```

**Logical Operators**
```BASH
{ "$<operator>": [{ <clause1> } , { <clause2> }, ...] }

# Syntac for $not
{ $not: { <clause> } }
```