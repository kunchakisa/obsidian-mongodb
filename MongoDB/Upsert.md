# Upsert

In upsert, everything in MQL that is used to **locate** a document in a collection can also be used to modify this document.

Upsert is a hybrid of **update** and **insert**, it should only be used when it is needed. The upsert option is placed at the 3rd argument of the update command.

```JavaScript
db.collection.updateOne({<query to update>}, {<update>}, {upsert: true})
```

If upsert is true, you can expect an update to insert, or update. If the query and the update arguments have enough information to identify a document, it can **both** update and insert.

![](assets/20221020200955%20Upsert%20Graph.png)

## Tips

- Upsert is good for conditional updates, when you may want to have a new document instead of an updated document.
- Don't use upsert if you only need to update a document, or insert a brand new one.

## Quiz

**Don't scroll too far, or you will see the answers!**

### Q: Upsert

How does the upsert option work?

Choose all answers that apply:

- It is used with the `update` operator, and needs to have its value specified every time that the update operator is called.
- When `upsert` is set to `false` and the query predicate returns an empty cursor then there will be no updated documents as a result of this operation.
- By default `upsert` is set to `false`.
- When `upsert` is set to `true` and the query predicate returns an empty cursor, the update operation creates a new document using the directive from the query predicate and the update predicate.

#### Answer

**It is used with the update operator, and needs to have its value specified every time that the update operator is called.**

> This is **incorrect**.
> 
> The upsert option only needs its value specified if you want to change the default `false` setting to `true`.

---

**By default** `upsert` **is set to false.**

> This is **correct**.
> 
> If the `upsert` option is not specified, then it will have the value of `false` by default.

---

**When** `upsert` **is set to** `true` **and the query predicate returns an empty cursor, the update operation creates a new document using the directive from the query predicate and the update predicate.**

> This is **correct**.
> 
> When `upsert` is set to `true` it can perform an insert if the query predicate doesn't return a matching document.

---

**When** `upsert` **is set to** `false` **and the query predicate returns an empty cursor then there will be no updated documents as a result of this operation.**

> This is **correct**.
> 
> When `upsert` is set to `false` an update will happen only when the query predicate is matched with a document from the collection.