It is a fully managed database with wide range of applications, with [MongoDB](MongoDB.md) at its core. It is a [database](Database.md) service in the cloud. Atlas users can deploy [clusters](Clusters.md). When MongoDB Atlas cluster is deployed, it will automatically be configured as a [replica set](Replica%20Set.md).

## Services

- Manage **cluster creation**
- **Run** and **maintain** database deployment
- Use cloud service provider of your **choice**
- Experiment with new tools and features

## Pricing

**Atlas Free Tier**

- Free cluster
- 3-server replica set
- 512 MB storage
- Never expires
- Free features like **Charts**. **Realm**.
- Good tier for small-scale apps

## URI String

- URI stands for Uniform Resource Identifier
- srv - establishes a **secure** connection.
- `mongodb+srv://user:password@clusterURI.mongodb.net/database`
- `user:password` is replaced by the credentials set in the Atlas settings.
- `clusterURI` refers to the unique Atlas cluster.
- `database` is the name of the database we want to interact with.

## Data Explorer

- It is a feature in Atlas to view data in your MongoDB directly in the Atlas UI.
- Navigate to it by going to `Cluster` -> `<Inside a cluster of your choice>` -> `Collections`.
- Select a particular [namespace](Namespace.md), and we can interact with the documents in the selection.
- You can see in there the **Collection Size**, **Total Documents**, and **Indexes Total Size**.
- Below, you'll see the first 20 results out of many documents. You can filter them by typing a query in JSON format. 
- It's recommended to try it by yourself with the sample dataset available in MongoDB Atlas.

### Sample Filters

- `{"state": "NY"}`
- `{"state": "NY", "city": "ALBANY"}`

### NOTE

The instruction on how to go to the Data Exlorer in the video is **OUTDATED**. Here is what it looks like when you try to use the Data Explorer feature in Atlas (as of this writing).

![](assets/20221016202830%20Data%20Explorer%20Screenshot.png)

## Find Command

- We can query results from our MongoDB instance with the **find** command.
- **Pretty** command returns the documents result from the find command formatted for **ease of reading**.

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

## Quiz

**Don't scroll too far! The answers are next after the questions**

### Q: What is Atlas?

**Choose the right answers!**

- MongoDB Database has the same functionality as Atlas, but without the friendly user interface.
- They are both MongoDB products.
- Atlas is a MongoDB service that can work with any database, but in this course it will be used with MongoDB.
- Atlas has many tools and services within it that are built specifically for the MongoDB Database.


#### Answer

**They are both MongoDB products.**

> This is **correct**.

---

**Atlas has many tools and services within it that are built specifically for the MongoDB Database.**

> This is **correct**.

---

**MongoDB Database has the same functionality as Atlas, but without the friendly user interface.**

> This is **incorrect**.
> 
> Atlas features go beyond the functionality of organizing and storing data, examples are Charts, Realm, Security features and more.

---

**Atlas is a MongoDB service that can work with any database, but in this course it will be used with MongoDB.**

> This is **incorrect**.
> 
> Atlas is built specifically for the MongoDB database, and can not be used in the same way with other databases.

### Q: The mongo shell (mixed with answers)

Honestly, I don't know where to get this answer, but the MongoDB University staff **encouraged** people to read documentations.

![](assets/20221017001419%20Quiz%20Answer%20The%20mongo%20shell.png)