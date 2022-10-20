# Comparison Operators

- `$eq` - ==eq==ual to
- `$ne` - ==n==ot ==e==qual to
- `$gt` - greater than
- `$lt` - less than
- `$gte` - greater than or equal
- `$lte` - less than or equal

## Implicit `$eq`

When an operator is not defined, the `$eq` operator is the default operator used for individual fields. The two queries below have the same effect.

```BASH
{ "student_id": 36 }

{ "student_id": { "$eq": 36 } }
```