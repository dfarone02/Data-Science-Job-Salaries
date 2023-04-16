In this section, I will create the training and testing datasets. Process found in this notebook:
https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/notebooks/TrainTestSplit.ipynb

Using the interim data created in the prior section so I can process training and testing data:
https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/interim/ds_salaries_interim.csv

#### For the purposes of the logistic regression model:

Data Analyst: <br>
 - Created "X" dataset from all variables except "Data Analyst"
 - Created "y" dataset from "Data Analyst"
 - Used sklearn train-test-split for 80% of the data as training and 20% remaining of random sample as testing data
 - https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/processed/Data%20Analyst/DataAnalyst_X_Test.csv
 - https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/processed/Data%20Analyst/DataAnalyst_X_Train.csv
 - https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/processed/Data%20Analyst/DataAnalyst_y_Test.csv
 - https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/processed/Data%20Analyst/DataAnalyst_y_Train.csv

Data Engineer: <br>
 - Created "X" dataset from all variables except "Data Engineer"
 - Created "y" dataset from "Data Engineer"
 - Used sklearn train-test-split for 80% of the data as training and 20% remaining of random sample as testing data
 - https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/processed/Data%20Engineer/DataEngineer_X_Test.csv
 - https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/processed/Data%20Engineer/DataEngineer_X_Train.csv
 - https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/processed/Data%20Engineer/DataEngineer_y_Test.csv
 - https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/processed/Data%20Engineer/DataEngineer_y_Train.csv

Data Scientist: <br>
 - Created "X" dataset from all variables except "Data Scientist"
 - Created "y" dataset from "Data Scientist"
 - Used sklearn train-test-split for 80% of the data as training and 20% remaining of random sample as testing data
 - https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/processed/Data%20Scientist/DataScientist_X_Test.csv
 - https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/processed/Data%20Scientist/DataScientist_X_Train.csv
 - https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/processed/Data%20Scientist/DataScientist_y_Test.csv
 - https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/processed/Data%20Scientist/DataScientist_y_Train.csv

Machine Learning Engineer: <br>
 - Created "X" dataset from all variables except "Machine Learning Engineer"
 - Created "y" dataset from "Machine Learning Engineer"
 - Used sklearn train-test-split for 80% of the data as training and 20% remaining of random sample as testing data
 - https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/processed/Machine%20Learning%20Engineer/Machine_Learning_Engineer_X_Test.csv
 - https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/processed/Machine%20Learning%20Engineer/Machine_Learning_Engineer_X_Train.csv
 -  https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/processed/Machine%20Learning%20Engineer/Machine_Learning_Engineer_y_Test.csv
-  https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/processed/Machine%20Learning%20Engineer/Machine_Learning_Engineer_y_Train.csv

#### For the purposes of the MultiOuput MultiClassification using Random Forests
 - Created "X" dataset from all variables except "Data Analyst", "Data Engineer", "Data Scientist", "Machine Learning Engineer"
 - Created "y" dataset from "Data Analyst", "Data Engineer", "Data Scientist", "Machine Learning Engineer"
 - Used sklearn train-test-split for 80% of the data as training and 20% remaining of random sample as testing data
 - https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/processed/All%20Fields/X_Test.csv
 - https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/processed/All%20Fields/X_Train.csv
 - https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/processed/All%20Fields/y_Test.csv
 - https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/processed/All%20Fields/y_Train.csv

### Back to Main Page: <br>
https://github.com/dfarone02/Data-Science-Job-Salaries/tree/2cdde691b82e1463ec560e61b672dae4931790c4#readme
