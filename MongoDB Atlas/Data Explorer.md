# Data Explorer

- It is a feature in Atlas to view data in your MongoDB directly in the Atlas UI.
- Navigate to it by going to `Cluster` -> `<Inside a cluster of your choice>` -> `Collections`.
- Select a particular [namespace](Namespace.md), and we can interact with the documents in the selection.
- You can see in there the **Collection Size**, **Total Documents**, and **Indexes Total Size**.
- Below, you'll see the first 20 results out of many documents. You can filter them by typing a query in JSON format. 
- It's recommended to try it by yourself with the sample dataset available in MongoDB Atlas.

## Sample Filters

- `{"state": "NY"}`
- `{"state": "NY", "city": "ALBANY"}`

## NOTE

The instruction on how to go to the Data Exlorer in the video is **OUTDATED**. Here is what it looks like when you try to use the Data Explorer feature in Atlas (as of this writing).

![](assets/20221016202830%20Data%20Explorer%20Screenshot.png)

## More Features

- The **Find** tab let's you search for a document.
- **Indexes** lets you add index and an insight on how often some fields are accessed.
- The **Schema Anti-Pattern** can gives you sound advice about your data model once enough queries have been issued against the collection.
- **Aggregation** tab is a useful and helpful tool to build an aggregation pipeline. It shows the sample results from the aggregation stage, and it also reminds you of the syntax you need to use. You can **export** the pipeline to your desired language, or export it for you to reimport it in the Atlas.
- **Search Indexes** - more advanced search with indexes available in the Atlas UI.
- You can use **Teams** to easily manage the permission of the users, instead of changing them individually. Use teams to assign projects to users.
- In Atlas, billing happens in the **organization** level, and projects are within organizations.
- **MongoDB Charts** is a product that helps you build visualizations of the data stored in your Atlas Cluster.