# Predicting House Prices in King County

This project has been forked from the git repository of Nadine Amersi-Belton a.k.a. [nadinezab](https://github.com/nadinezab/kc-house-prices-prediction/blob/master/kc-house-prices.ipynb) to be re-tuned, while the original project offered only a Multi-Linear regression as a solution this current projects applied several models to address.

I is worth mentioning that the regression model selection was greatly influenced by [this Keggle notebook](https://www.kaggle.com/code/junkal/selecting-the-best-regression-model)

Another key difference is that the original project did a train/test split prior to the exploratory analysis and outlier removal which is a poor practice, as it should be done [just before modeling](https://datascience.stackexchange.com/questions/75702/when-should-you-remove-outliers)

## Problem statement

 Investigating house sales in the King County area and building a model to predict sale price. Key executives are keen to launch an advertising campaign directed towards home owners in that area who might consider selling their house, focusing on hcoigher-end residential properties.

## Components

* **Jupyter Notebook**

The [Jupyter Notebook](https://github.com/DimitriyDashinov/kc-house-prices-prediction/blob/master/kc-house-prices.ipynb) is our key deliverable and contains details of our approach and methodology, data cleaning, exploratory data analysis and model building and validation.

* **Data**

The dataset can be found in the file *"kc_house_data.csv"* in the Data folder, in this repository. It was originally provided in the following [repository](https://github.com/learn-co-students/dsc-mod-2-project-v2-1-onl01-dtsc-pt-012120). 

* **Misc**

We found a GEOJSON file with zip code borders, which was used as part of data exploration. It is included in the repository.

