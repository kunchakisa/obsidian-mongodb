# What is MongoDB

- It is a [NoSQL](NoSQL%20Database.md) document [database](Database.md) in which data is stored as **[documents](Document.md)**.
- Documents are stored in a **[collection of documents](Collection.md)**.
- Data is stored in a structured way, but **not** in the traditional way of tables with rows and columns.
- MongoDB uses [BSON](BSON.md) to **store data**, but that does not mean you can't store what you can in [JSON](JSON.md). Most of the time, BSON **can be represented** with JSON, as long as the JSON **supports the data type** used in it.

## Importing and Exporting Data

- MongoDB data is stored in [BSON](BSON.md), but is viewed in [JSON](JSON.md).
- If data is passed from a machine to another machine, using **BSON** is the best choice.
- If data is supposed to be stored locally and be read easily, **JSON** is the better choice.
- Commands used to import/export in **JSON** is `mongoimport` and `mongoexport`.
- Commands used to import/export in **BSON** is `mongorestore` and `mongodump`.
- `mongoimport` supports **JSON** and the popular format, **CSV (Comma Separated Values)**.

### Codes used

```
mongodump --uri "mongodb+srv://<your username>:<your password>@<your cluster>.mongodb.net/sample_supplies" 

mongoexport --uri="mongodb+srv://<your username>:<your password>@<your cluster>.mongodb.net/sample_supplies" --collection=sales --out=sales.json

mongorestore --uri "mongodb+srv://<your username>:<your password>@<your cluster>.mongodb.net/sample_supplies" --drop dump

mongoimport --uri="mongodb+srv://<your username>:<your password>@<your cluster>.mongodb.net/sample_supplies" --drop sales.json
```

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