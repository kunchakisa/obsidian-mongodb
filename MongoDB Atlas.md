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

## Subtopics
- [Data Explorer](MongoDB%20Atlas/Data%20Explorer.md)
- [Updating Data with Data Explorer](MongoDB%20Atlas/Updating%20Data%20with%20Data%20Explorer.md)

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