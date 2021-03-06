# Predicting House Prices in King County

This multiple linear regression project was completed as part of Flatiron School's Data Science Bootcamp (Module 2 Final Project).

## Problem statement

As a junior data scientist at real estate company PropertiesInc., I have been tasked with investigating house sales in the King County area and building a model to predict sale price. Key executives are keen to launch an advertising campaign directed towards home owners in that area who might consider selling their house, focusing on higher-end residential properties.

Before building the model, we will address the following descriptive questions through data exploration:

1. Which locations within the King County area have the highest average house prices?

2. Which house attributes increase sale price?

3. Does time of the year have an impact on house sales?

## Components

* **Jupyter Notebook**

The [Jupyter Notebook](https://github.com/nadinezab/kc-house-prices-prediction/blob/master/kc-house-prices.ipynb) is our key deliverable and contains details of our approach and methodology, data cleaning, exploratory data analysis and model building and validation. The key models have also been saved using Pickle.

I recommend using [nbviewer](https://nbviewer.jupyter.org/) to view the Jupyter Notebook.

* **Presentation**

The [presentation](https://github.com/nadinezab/kc-house-prices-prediction/blob/master/Presentation.pdf) gives a high-level overview of our approach, findings and recommendations for non-technical stakeholders. It is aimed to be between 5 and 10 minutes long.

* **Data**

The dataset can be found in the file *"kc_house_data.csv"* in the Data folder, in this repository. It was originally provided in the following [repository](https://github.com/learn-co-students/dsc-mod-2-project-v2-1-onl01-dtsc-pt-012120). 

* **Misc**

We found a GEOJSON file with zip code borders, which was used as part of data exploration. It is included in the repository.

* **Blog Post**

A [blog post](https://towardsdatascience.com/creating-a-map-of-house-sales-42ba1f2c4e7e?source=friends_link&sk=39a274886a862dc1258f4d97f8392391) was created as part of this project.

## Technologies/ Packages

* Python version: 3.6.9
* Matplotlib version: 3.1.3
* Seaborn version: 0.9.0
* Pandas version: 0.25.1
* Numpy version: 1.16.5
* Statsmodels version: 0.10.1
* Scikit-learn version: 0.21.2  
* Bokeh version: 2.0.2 
* Folium version: 0.9.1 
* Geopandas version: 0.7.0
* Geopy version: 1.21.0 
* Reverse_geocoder version: 1.5.1
* Pickleshare version: 0.7.5 

## To get started

1. Clone this repository - [guidance](https://help.github.com/articles/cloning-a-repository/).
2. Dataset can be found in the file "kc_house_data.csv".
3. Check requirements in Technologies section above and download libraries if necessary.


## Summary of EDA

**Q1 Location**

* Waterfront living is key, with the median house price for a house with a waterfront view being almost double that of one that does not have this feature.
* We recommend focusing the campaign on the following neighbourhoods: Medina, Clyde Hill and Mercer Island (the most expensive neighbourhoods).
* Location within King County is important with a noticeable disparity amongst zipcodes. The median house price ranges from $235,000 in 98002 up to $1,260,000 in 98039.

<img src="/Images/q1map.png" alt="Median House Prices per Zipcode" width = "400">

**Q2 House attributes**

* We recommend targetting the campaign towards houses with a higher bedroom count. However for a given house depending on its square-footage, note that adding an additional bedroom does not necessarily result in a a sale price increase.
* There does not appear to be a clear relationship between the ratio sqft_living/sqft_lot and price. This indicates that there is unlikely to be an idea area to allocate to living space within a plot.
* The median house price increases with grade indicating that these features are positively correlated. We suspect grade will be a good indicator of price.
* For the campaign we would recommend looking at houses with a grade of 10 or above.

![Median Price per Grade](/Images/q2grade.png)

**Q3 Time of the year**

* House prices do not appear to be affected by sale month or quarter, with the median house price being almost constant throughout the year.
* April and May are the most popular months for house sales. In contrast, January and February have the lowest number of sales Q2 alone accounts for 31.3% of house sales.
* We would recommend launching the campaign in March/April, to gather interest with a view of completing the sale in Q2.

![Number of sales per month](/Images/q3salemonth.png)

## Final model details

**Model A**

* 17 features
* Adjusted  R-squared  of 0.701 (70% of variations explained by our model)
* Uses zip code tiers instead of actual zipcodes
* Better for generalising to other areas
* RMSE of 132,444 (mean RMSE with 10-fold cross-validation)

**Model B**

* 87 features
* No interacting terms or polynomials
* Adjusted R-squared  of 0.832 (83% of variations explained by our model)
* RMSE of 99,654 (mean RMSE with 10-fold cross-validation)

**Interpreting Model coefficients**
- A grade 12 house on average is worth USD 52,000 more than grade 11 (model A)
- Being on the waterfront is valued at USD 277,442 (model A)
- For every additional squarefoot of living space, the price inscreases by USD 123.5 (model B)

## Contributors:

|Name     |  GitHub   |
|---------|-----------------|
|Nadine Amersi-Belton |https://github.com/nadinezab|

## Contact

* If you have any questions, you can contact me at nzamersi@gmail.com
