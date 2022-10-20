# Data Modeling

[MongoDB](MongoDB.md) does not enforce how data is organized by default. This is where data modeling enters. It is a way to organize fields in a document to support your application performance and querying capabilities. 

**See**: [documentation](https://www.mongodb.com/docs/manual/core/data-modeling-introduction/), [blog](https://www.mongodb.com/blog/post/building-with-patterns-a-summary)

## Tips

- Data that is accessed together, should be stored together
- As an example, don't clump up all of data about a user, personal info, their medical history, and their video watch history in a single collection. Separate them into a user collection, medical history collection, and a video watch collection. Of course, don't merge videos and video history together too.
- Evolving application implies an evolving data model.