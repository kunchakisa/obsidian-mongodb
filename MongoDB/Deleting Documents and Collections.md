# Deleting Documents and Collections

We can see a trash icon when we hover to our desired documents in Atlas. With that, we can delete documents, and even collections. But what if we want to delete them with mongo shell?

## Commands

- `deleteOne()` deletes one matching documents
- `deleteMany()` deletes all matching documents
- `drop()` is used in collections to delete them

**See**: [Commands that affects only one item](Commands%20that%20affects%20only%20one%20item.md) -> When to use

## Commands Used

```BASH
db.inspections.deleteMany({ "test": 1 })
db.inspections.deleteMany({ "test": 3 })
db.inspections.drop()
```