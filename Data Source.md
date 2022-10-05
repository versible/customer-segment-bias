# Customer Segment Bias - Source Data
There are 2 critical data pre-requisites to running this model (beyond the obvious need for sales data).
1. Some form of customer identifier to link baskets together across time.  Some form of customer card is the ideal way to do this, but payment card based basket linking might be possible providing the second critical data pre-requisite can be met too.
1. Work to have measured the importance of the attribute of interest to customers.  This likely involves a previous customer segmentation project, where all customers are classified in to a small set of customer segments (Foodies, Traditional, Large Families, Time Pressured, Healthy Eaters...). Attitudinal research of these customer segments then gives the source of "importance of" data.

## Time Period
This analysis is based on a snapshot of data.  Experience suggests customer segment bias results tend not to vary across time.  Therefore the duration and recentcy of the snapshot is primarily about capturing newly listed products.

A year duration would seem sensible.  But if aggregating on this volume of source data is too much, smaller snapshot durations are probably OK.  The limitation of using a short duration (like a week) will be ensuring there is a representative sample of customer segments buying each product.  Some form of limit will help outputing potentially eronious results, but at the expense of not outputing any data for slower selling products.


## Customer
* A customer identifier 
* A reference table mapping customer identifier to a customer segment

## Product
* Product identifier
* Reference name of product descriptions and reporting heirarchy (for use presenting output only)

## Sales or Volume
It doesn't matter whether you take sales or volume, and both will get normalised (turned in to share of product by customer segment).

## Importance Of Scores
For each customer segment, you need a suitably scaled score for where each segment sits on some spectrum.

Taking price-quality as a worked example.  Say research asked Importance Of Price and separate Importance Of Quality questions to each customer segment.  You'll have a small table of each segment (rows) holding the two Importance of scores.  You need to invent some simple logic to transform this so your most price focused segment is -1.0 and your most quality focused segment is +1.0, and all other segments are scored in between.  Given the data volumes are so low, this fun little problem could be done well without recourse to any maths.  Or, if you like maths, try dimensionality reduction / principle component analysis to project the 2 features onto a single dimension.

The example is price-quality, but could be applied to any other attitudinal spectrum.  Importance of healthiness.  Adventureousness.  Convinenience...

---

© Versible 2022