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
