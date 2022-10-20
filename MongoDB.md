# What is MongoDB

- It is a [NoSQL](NoSQL%20Database.md) document [database](Database.md) in which data is stored as **[documents](Document.md)**.
- Documents are stored in a **[collection of documents](Collection.md)**.
- Data is stored in a structured way, but **not** in the traditional way of tables with rows and columns.
- MongoDB uses [BSON](BSON.md) to **store data**, but that does not mean you can't store what you can in [JSON](JSON.md). Most of the time, BSON **can be represented** with JSON, as long as the JSON **supports the data type** used in it.

## Subtopics
- [Importing and Exporting Data](MongoDB/Importing%20and%20Exporting%20Data.md)
- [Find Command](MongoDB/Find%20Command.md)
- [Inserting Data](MongoDB/Inserting%20Data.md)
- [Updating Data](MongoDB/Updating%20Data.md)
- [Deleting Documents and Collections](MongoDB/Deleting%20Documents%20and%20Collections.md)

## Quiz

**Don't scroll too far, or you will see the answer!**

### Q: Importing and Exporting Data

1. You wanted to import the data stored in a file named `Animals.json`. What commands do you need to use? **Choices:** `mongoimport`, `mongoexport`, `mongodump`, `mongorestore`.
2. You need to transfer the data from one database to another, what is the **best** command to export the data? **Choices:** `mongoimport`, `mongoexport`, `mongodump`, `mongorestore`.
3. You like to impress your friends and show them some things you and them **can't** understand. You have thought of a brilliant idea and used the data in the sample data set of your MongoDB tutorial. What command do you need to use to impress your friends? **Choices:** `mongoimport`, `mongoexport`, `mongodump`, `mongorestore`.

#### Answers

1. Since the file is a `.json` file, you need to use **`mongoimport`**.
2. The best format to use when transferring data from a machine to another machine is **BSON**. **`mongodump`** is the command to export the data into BSON. See [Importing and Exporting Data](#Importing%20and%20Exporting%20Data).
3. JSON is readable while **BSON is not**. Since you want to export BSON, **`mongodump`** is the command you need. See [Comparison between JSON and BSON](BSON.md#Comparison%20between%20JSON%20and%20BSON).

### Q: Import Errors

![](assets/20221017095101%20Quiz%20Inspect%20Errors.png)

#### Answers

**MongoDB can store duplicate documents in the same collection, as long as their** _id **values are different.**

> This is **true**.
> 
> The only value that is being checked for duplicates on insertion by default is the _id value, since it serves as a unique identifier for the document.

---

**If a document is inserted without a provided** _id **value, then that field and value will be automatically generated for the inserted document before insertion.**

> This is **true**.
> 
> MongoDB ensures that each inserted document has a unique _id value.

---

**MongoDB can always store duplicate documents in the same collection.**

> This is **false**.
> 
> While documents that have duplicate content are allowed, they still have to have unique _id values.

---

**There is no way to ensure that duplicate records are not stored in MongoDB.**

> This is **false**.
> 
> You can place additional rules on which documents can and cannot be inserted into a collection using MongoDB's schema validation functionality.

---

**If a document is inserted without a provided** _id **value, then that document will fail to be inserted and cause a write error.**

> This is **false**.
> 
> MongoDB will automatically add an _id field and assign it an ObjectId type value when inserting such documents into a collection.