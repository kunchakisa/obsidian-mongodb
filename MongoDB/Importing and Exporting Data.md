## Importing and Exporting Data

- MongoDB data is stored in [BSON](BSON.md), but is viewed in [JSON](JSON.md).
- If data is passed from a machine to another machine, using **BSON** is the best choice.
- If data is supposed to be stored locally and be read easily, **JSON** is the better choice.
- Commands used to import/export in **JSON** is `mongoimport` and `mongoexport`.
- Commands used to import/export in **BSON** is `mongorestore` and `mongodump`.
- `mongoimport` supports **JSON** and the popular format, **CSV (Comma Separated Values)**.
- in `mongorestore`, and `mongoimport`, you see the `--drop` option. It is used to avoid duplicate error messages by dropping the existing documents first, before importing/restoring. (Not a safe thing to do tbh)

### Codes used

```BASH
mongodump --uri "mongodb+srv://<your username>:<your password>@<your cluster>.mongodb.net/sample_supplies" 

mongoexport --uri="mongodb+srv://<your username>:<your password>@<your cluster>.mongodb.net/sample_supplies" --collection=sales --out=sales.json

mongorestore --uri "mongodb+srv://<your username>:<your password>@<your cluster>.mongodb.net/sample_supplies" --drop dump

mongoimport --uri="mongodb+srv://<your username>:<your password>@<your cluster>.mongodb.net/sample_supplies" --drop sales.json
```