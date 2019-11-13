# How to Use the W Function to Show Top N Products by Category

This example demonstrates how to show the products with top N sales by category.

![](images/screenshot.png)


The dashboard contains calculated fields with the following expressions:

| Field | Expression |
| --- | --- |
| ProductRankInCategory | aggr(w(RankDense(Sum([ProductSales]), 'desc'), PartitionBy([CategoryName]), OrderBy()), [CategoryName], [ProductName])

The grid shows the products with the **ProductRankInCategory** value that is more or equal to the parameter value (default value is 2).

Grid rows in the _Top Products_ and _OTHERS_ are sorted by the 
**TopNProductsSortOrder** calculated field for proper arrangement.

See also:

* [Data Analysis](https://docs.devexpress.com/Dashboard/115868)