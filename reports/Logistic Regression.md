To run the Logisitc Regression Models for Data Analyst, Data Engineer, Data Scientist, and Machine Learning Engineer follow this link:

https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/notebooks/Logistic%20Regression.ipynb

Data Analyst
-------------
Training and Testing Data Sets found at the links below: <br>
https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/processed/Data%20Analyst/DataAnalyst_X_Test.csv <br>
https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/processed/Data%20Analyst/DataAnalyst_X_Train.csv <br>
https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/processed/Data%20Analyst/DataAnalyst_y_Test.csv <br>
https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/processed/Data%20Analyst/DataAnalyst_y_Train.csv <br>

After running a logistic regression with 1000 iterations, the resulting confusion matrix is below:<br>
![image](https://user-images.githubusercontent.com/97635420/232327499-1de27883-842a-47f4-932b-a448ab8ad6a7.png)<br>
As you can see, the model did not classify any negatives, so the predictor variables were too hard to distinguish among Data Analyst or other job fields, so our Sensitivity and Specificity measures were 0.0. Dpesite that, we had an accuracy rate of 77.05%, which is quite good all things considered. <br>
None of the variables were very influential in determining in one was a Data Analyst or not, but work_year had the highest negative impact on the model meaning the more recent the year, the less likely one is to be a Data Analyst. <br>
Conversely, remote_ratio had the highest positive impact on the model. So, the more remote a postition was, the more likely one is to be a Data Analyst

Data Engineer
--------------
Training and Testing Data Sets found at the links below:<br>
https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/processed/Data%20Engineer/DataEngineer_X_Test.csv <br>
https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/processed/Data%20Engineer/DataEngineer_y_Test.csv <br>
https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/processed/Data%20Engineer/DataEngineer_X_Train.csv <br>
https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/processed/Data%20Engineer/DataEngineer_y_Train.csv <br>

Data Scientist
----------------
Training and Testing Data Sets found at the links below:<br>
https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/processed/Data%20Scientist/DataScientist_X_Test.csv <br>
https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/processed/Data%20Scientist/DataScientist_y_Test.csv <br>
https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/processed/Data%20Scientist/DataScientist_X_Train.csv <br>
https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/processed/Data%20Scientist/DataScientist_y_Train.csv <br>

Machine Learning Engineer
-------------------------
Training and Testing Data Sets found at the links below:<br>
https://github.com/dfarone02/Data-Science-JobSalaries/blob/main/data/processed/Machine%20Learning%20Engineer/Machine_Learning_Engineer_X_Test.csv <br>
https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/processed/Machine%20Learning%20Engineer/Machine_Learning_Engineer_y_Test.csv <br>
https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/processed/Machine%20Learning%20Engineer/Machine_Learning_Engineer_y_Train.csv <br>
https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/processed/Machine%20Learning%20Engineer/Machine_Learning_Engineerr_X_Train.csv <br>

### Back to Main Page: <br>
https://github.com/dfarone02/Data-Science-Job-Salaries#multi-output-multi-level-random-forest-classification

