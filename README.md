# forecastingFloodInundation
Forecasting Flood Inundation modeling project for CPLN 675 at University of Pennsylvania, Spring 2022


Basic procedure
1.	Gather open data from both Calgary’s open data site and your comparable city’s open data site as well as other internet sources.
2.	Using what we’ve learned about feature engineering over the first part of the semester, build as many useful variables describing the natural, hydrological and built environment features that might help explain flood inundation. You must include at least one feature from the watershed analysis. 
3.	Join these features to the vector Fishnet. Remember that ‘distance or density to Feature A’ might describe the spatial relationship better than simply, ‘Feature A’.
4.	Move your Fishnet dataset into R and run some logistic regressions with both a test set and a training set. Experiment until you find a model with enough statistically significant variables. 
5.	Run goodness of fit metrics; More advanced groups (e.g. if you have taken MUSA 508) should experiment with spatial cross-validation. Visualize your results in chart and map form.

Deliverables 
Your markdown or pdf report should contain the following:
1.	The Planning motivation for your algorithm and how you would deploy such an algorithm (borrow from your memo).
2.	One page showing four of your more original (as you deem it), yet statistically significant features. Annotate as you see fit. 4 maps on 1 page. This must include at least one watershed feature (even if it’s not significant).
3.	One page with your final logistic regression model summary including your ROC curve, confusion metrics and associated goodness of fit/cross-validation. Annotate briefly. 
4.	One page showing 3 maps – The first shows true positives, true negatives, false negatives and false positives for the training set in Calgary. Second, your inundation predictions for Calgary (entire dataset); Third, predictions for your comparable city.

Training & Validation City:
[Calgary](https://data.calgary.ca/)

Possible cities:
- [Edmonton](https://data.edmonton.ca/)
- [Pittsburgh](https://pittsburghpa.gov/open-data/index.html)
- [Cincinnati](https://data.cincinnati-oh.gov/)
- [St. Louis](https://www.stlouis-mo.gov/data/index.cfm)
- Nashville
- Memphis

Data to collect:
- Elevation (DEM)
- Land Cover (impervious is more important)
  - [National Land Cover Database](https://www.usgs.gov/centers/eros/science/national-land-cover-database)
- Stream / River centerlines
- Hydrology (width, depth, flow rate)
- Building footprints
- Existing floodplain maps
- Soil data - grain size / soil texture


DEM analysis
- slopes 
- streams and tributaries
- assigned weight based on stream order
- distance accumulation from streams

Data Sources:
|City|Feature|DataType|Use|DataLink|
|----|----|----|----|----|
|Calgary|DEM|Raster||[Link](https://data.calgary.ca/Base-Maps/Digital-Elevation-Model-DEM-ASCII-2M/eink-tu9p)|
|Calgary|Elevation|||[Link]()|
|Calgary|Slope|||[Link]()|
|Calgary|SteepSlopes||||
|Calgary|Dist_SteepSlopes||||
|Calgary|LandCover|Vector||[Link](https://data.calgary.ca/resource/as2i-6z3n.json)|
|Calgary|CommercialZones||||
|Calgary|ResidentialZones||||
|Calgary|IndustrialZones||||
