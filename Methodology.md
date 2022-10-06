# Customer Segment Bias - Methodology

Assuming you have 2 pieces of source data:
* Snapshot of sales by product and customer segment.
* Attitudinal Score for each customer segment.


The steps are simple:
1. Compute each products share of sales by customer segment
1. Use each product's share of sales by customer segment as the weighting to compute that products average attitudinal score.

That's it!

If you think like an Excel Analyst:
1. A pivot table of products (row) versus customer segments (columns) with the metric (sales) displayed as % of row total.
1. Use each row of the pivot table as the weightings to calculate the average attitudinal scores for each product.

If you think like a SQL Analyst:
1. Divide every product-segment sales by the sum of that product's sales.  Use a windowing function to compute the sum of each product's sales.
1. Join in the attitudinal scores (on customer segment), then aggregate on product computing the weighted average attitudinal score.


There are doubtless 101 other ways to compute this.

---

If the methodology felt too easy, maybe invest your time on beautiful and insightful ways to report the output.

* Look at the overall distribution of your scores.  They probably don't centre on zero.
* How do Category averages compare?
* Pull out some examples.  Jams & Marmalades if often good.  Single pot yoghurts.  Anything from BWS.  And if them in your sales data, newspapers often provides solid data to backup preconceptions about the attitudes of each title's readers.
* Can you use a report tool to present the data in a visual and drillable way?  For example, showing the distribution of scores within a category and allowing the user to click the chart and see which products fall where.

---

© Versible 2022