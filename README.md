# Customer Segment Bias

## Overview
This project aims to allow like-minded companies and individuals to co-operate in using and developing a basic model to measuring product positioning by the type of customers that buy that product.  The setting is exemplified by grocery retail, but can no doubt be applied to other settings which share similar product purchasing characteristics.


## Definition: What is a Customer Segment Bias?
Customer Segment Bias is a number that estimates where a product sits on some spectrum between opposite product charactistics.  The most common implementation is the spectrum between price and quality, which can equally be labelled and interpreted as the spectrum between price sensitive and insensitive.

The term "Customer Segment Bias" is intended for inward use.  Business stakeholder would probably benefit from more application specific label like Price Sensitivity, or Quality Positioning.  Business stakeholders might even prefer a classification output (very low, low, average, high, very high) as opposed to an abstract number.


## Ethos

Until there is source code associated with this project, the question of licensing is probably mute.

The intention is to provide this knowledge on a Copyleft (GPLv3) basis.  If you don't know what a Copyleft license is, please educate yourself before cloning / copying this repository.

The intention is to make this project free for anyone to use to measure customer segment bias within their own organisation.  "Anyone" could be an employee of a retailer, a researcher or a student.

The intention is to discourage companies or individuals from re-selling this work and gaining payment, partly or wholly, as a consequence.  At least, not without seeking explicit permission first.  In principle, permission will be granted, but in exchange for suitable contribution to the project (financial or otherwise - dependent on scale of commercial gain).

The technical methodology outlined here is not complex and probably too generic to even consider questions of authorship and ownership.  The intention for making this methodology openly available is to enable collaborative improvements between individuals and companies that are otherwise unwilling to collaborate due to perceived or real conflicts of interest.  

By making a methodology openly available we also hope to faciliate some side-effects:
* To make it harder for software and consulting vendors to hide behind a mask of having a "complex proprietory algorithm" which turns out to be as straight-forward as the one presented here. 
* To equipe inhouse Data / Analytics / Insight / Science teams to deliver externally credible models themselves.
* If a company wants Versible to help implement, we are of course happy to be engaged ;-).


## Data Sources
Ideal source data is one year's worth of customer product sales.

Details are given in the separate `Data Sources.md` file in this repository. 


## Methodology

The core of the methodology is a simple weighted average of the attitudinal score, with the weighting being each product's share of sales by segment.

Dtails are given in the separate `Methodology.md` file in this repository. 

## Code

Until we are aware of a suitably licensed openly available data set, we are not providing the source code of an implementation of this methodology.  While at first sight the lack of source code might disappoint, anyone fully engaging in this topic will realise it is the methodological description that is far more important.  Specific technical implementations should be straight-forward for any Analyst with suitable skills, data access and compute resource.

## Caveats about this Approach

The key strength or this approach can also be its primary weakness.  The model is usually so good it is easy to get lazy with interpreting the output.

Consider an implementation to assess quality or price focus of products.  It is all too easy to slip in to saying "these products are high quality".  From experience 99% of the time, this interpretation is correct (and simple and easy to communicate).  But the strict interpretation is "these products are preferentially bought by shoppers who rate quality as more important than price".  

To illustrate the difference between the lazy and strict interpretation, consider loose mushrooms.  This is a real example demonstrated across multiple implementations of this model.  A retailer's lowest priced loose mushroom (Value/Economy/Basic/Everyday/Etc) is surely all about price rather than quality.  Yet it often scores towards the quality end of a price-quality customer segment bias scale.
* Lazy interpretation: Value/Economy/Basic/Everyday Loose Mushrooms are a high quality product.
* Correct interpretation: Value/Economy/Basic/Everyday Loose Mushrooms are bought preferentially by customers that rate quality highly, even though the product itself can still be relatively low quality.

With awareness of this caveat, these occassional examples should been treated as valuable insight.  There is a reassuring expensive branded lager, whose entire marketing proposition is about its quality, yet it typically scores towards the price end of a price-quality customer segment bias scale.
   

---

© Versible 2022