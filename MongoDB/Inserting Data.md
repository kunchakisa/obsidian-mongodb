## Inserting New Documents

I'll put the summary first, as the topic might be too long to read for a review.

### Summary

- `_id` is the unique identifier for a document in a collection.
- `_id` is required in every MongoDB document.
- `ObjectId()` is the default value for the `_id` field, unless otherwise specified.
- MongoDB auto generates the `ObjectId()`, but when you specify a custom `_id` data type, you need to generate or make one manually.

### Extra Knowledge

**See**: [ObjectId](../ObjectId.md)

### Content

When inserting new documents with the **MongoDB Atlas** UI, or MongoDB Compass, you'll see that you can choose between two view options. One is using **JSON notation** (the curly braces sign), and the **Default View** (the sign that looks like a list).

**Insert UI in Default View**
![](assets/20221017084529%20Insert%20Document%20UI.png)

**Insert UI in JSON View**
![](assets/20221017084707%20Insert%20in%20JSON%20View.png)

You will notice that in whichever viewing option you chose, the `_id` field is there. Every document in the collection must have a **unique** `_id` value. Do note that the rest of the fields and values are **not forced to be unique by default**. You can have a hundred documents containing the exact same field-value pairs, as long as their `_id` values differ from each other.

![](assets/20221017085033%20Documents%20with%20same%20contents.png)

Likewise, you can have different documents with different values and even unique keys from each other. But this is not a good practice to organize your data.

**Back to inserting data**, you see in the insert UI that MongoDB populates the `_id` field with an ObjectId data type. `_id` don't need to be an ObjectId by default. It can be a Number, a String, or anything.

**See**: [Inserting Documents to a Non-Existing Collection](Inserting%20Documents%20to%20a%20Non-Existing%20Collection.md)

## Insert Order

You can insert multiple documents in one `insert()` function by passing an array instead of an object. But when an error occurs on one of the documents, the other documents **won't be inserted**. Why is that?

By default, documents will be inserted in an **ordered manner**. So, when we try to insert 5 documents and encounter an error in the 2nd document, the other 3 won't be inserted. To avoid this error, we can add the `"ordered": false` option in the 2nd argument of the insert function.

### Codes Used

```SHELL
# Default ordered command
db.inspection.insert([{ "_id": 1, "test": 1 },{ "_id": 3, "test": 3 }])

# Unordered command by passing a 2nd argument of options
db.inspections.insert([{ "_id": 1, "test": 1 },{ "_id": 1, "test": 2 }, { "_id": 3, "test": 3 }],{ "ordered": false })
```