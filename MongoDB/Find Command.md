## Find Command

- We can query results from our MongoDB instance with the **find** command.
- **`pretty`** command returns the documents result from the find command formatted for **ease of reading**.

### Note

- When you issued the find command without a query, the first 20 documents from the collection will show, but they appear without specific order. 
- Use `show dbs` and `show collections` for available namespaces.
- `find()` returns a cursor with documents that match the query.
- `count()` returns the number of documents that match the query.
- `pretty()` formats the documents in the cursor. It is formatted for ease of reading. 

### Codes Used

```BASH
# All databases will be listed, including "admin" and "local", which are default database that is managed by Atlas.
show dbs

# To use the desired database... (ie, sample_training)
use sample_training

# List all the collections in there
show collections

# When we used the use command, the db will point to the database we used
db.zips.find( {"state": "NY"} )
db.zips.find( {"state": "NY"} ).count()

# it iterates through the cursor if there's a lot of results.
it
it

db.zips.find( {"state": "NY", "city": "ALBANY"} ).pretty()
```
