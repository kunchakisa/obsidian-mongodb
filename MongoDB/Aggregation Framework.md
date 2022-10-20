# What is the Aggregation Framework for?

To use the aggregation framework, we use aggregate instead of find. The reason for that is because sometimes we might want to aggregate, as in group or modify our data in some way, instead of always just filtering for the right documents. This means that you can perform operations other than finding and projecting data. And you can also calculate using aggregation.

![](assets/20221020174325%20Aggregate%20Syntax%20Example.png)

In `aggregate()`, we use an array as an argument, because the order matters. Meaning, we give the data to the pipeline, and we describe how the pipeline will treat the data using **aggregation stages**. The transformed data will be returned at the end of the pipeline.

## Subtopics

- [Stages](Aggregation%20Framework/Stages.md)
- [Operators](Aggregation%20Framework/Operators.md)