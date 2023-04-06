data/external/ds_salaries_external.csv
https://github.com/dfarone02/Data-Science-Job-Salaries/blob/200620f4b7e4a4064750887776d182f0ef495b19/notebooks/EDA.ipynb
https://raw.githubusercontent.com/dfarone02/Data-Science-Job-Salaries/main/reports/output.html (need to right click, save as, and open in file location)

The 2020-2022 dataset consists of 606 different individuals with 11 variables and no missing values at any position. 9 variables are categorical and 2 are numeric, so a classification model is definitely preferrable to a regression model here. All of the categorical variables (except for location) have 4 or less categories, so we will be converting many of these to dummy variables for the predictive model will not be difficult, but I am obviously going to get rid of location. Of the remaining categorical variables, none are evenly distributed except for "job title", which I will be trying to predict. Looking at the correlation matrix the only variables with a strong correlation have to do with location. When I do my feature engineering, I will probably have to make location work in this model now. The only variables that have any covariance are salary and salry_in_usd. To make it easy, I am just going to drop that column and keep salary_currency because I want to see if location has any impact on one's job title. After conducting this EDA, the next steps are to convert categorical variables to dummy and binary variables to build the models.


### Back to Main Page: <br>
https://github.com/dfarone02/Data-Science-Job-Salaries/tree/2cdde691b82e1463ec560e61b672dae4931790c4#readme
