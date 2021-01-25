## Ames, IOWA housing Project
Given an Ames Housing Dataset design a Regression Model to accurately predict the sale price of houses in Ames, Iowa

•	Ames Housing Dataset containing 78 features of buyer are interested in knowing about before purchasing a home/house, which was used to train and test my Models
•	Test Dataset which was used to evaluate my Model’s performance

The data and explored it there alongside the extended data dictionary give. The following approach was then taken using a test size of 10%:
•	Design a Model based on the features I will look for in a house

•	Fill all the null values with 0 (assumption here is that these where all 0 because the where applicable). Then design a Model based on the features with abs|corr()| > .4
•	Submit both results and use the one with the better Kaggle results as my starting point, adding features and checking their coefficient to see if they should be removed to kept to design the perfect Linear Regression Model

## Data Cleansing:
•	Null values were taken to mean that the feature was not applicable to that specific house:
•	Since there were over 75 columns to consider I only clean columns that I was interested in using in my model, adding to a function I created so that at the end it will contain all necessary fields
•	For ‘Central Air’ I changed that column to 1’s and 0’s since this was a binary column
•	I also deleted the rows where ‘Gr Liv Area’ was greater than 4000
•	To cater for the columns attributes that did not exist in both tables I merged both tables together, adding a ‘SalePrice’ of 0 to the test dataset and split the data after running get_dummies().

A Linear model was then generated a model containing the following fields and submitted to Kaggle:
•	"lot_area", "street", "lot_shape", "1st_flr_sf", "2nd_flr_sf", "yr_sold", "condition_1", "neighborhood", "overall_cond", 'garage_area', 'year_remod/add', 'full_bath', 'totrms_abvgrd'

I then created some visualization to view the data to evaluate the model this model performed worst then my previous model on Kaggle, so I then add some more feature based on the coefficient of my model. This model performed worst on Kaggle, so I did a few more models with all the features and removed a few based on the performance of my model.

After a few submissions on Kaggle I was finally able to get a model that scored 33,122.74

## Conclusion

 My model is in no way the ideal Model but my attempt to produce a better scoring model using Lasso or Ridge was unsuccessful at this time. Although I was not happy with my unscaled version it produced the best results, therefore it will be the model I am going to Productionize today.
In the further I will spend less time on my Linear Regression Model and let Lasso and Ridge do the work for me.
