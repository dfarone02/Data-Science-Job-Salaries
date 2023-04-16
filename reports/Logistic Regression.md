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
After running a logistic regression with 1000 iterations, the resulting confusion matrix is below:<br>
![image](https://user-images.githubusercontent.com/97635420/232327913-12b45370-86f0-4de6-97a2-f7ac24476e91.png)<br>
As you can see, the model did not classify any negatives, so the predictor variables were too hard to distinguish among Data Engineer or other job fields, so our Sensitivity and Specificity measures were 0.0. Despite that, we had an accuracy rate of 65.57%, which is worse than the Data Engineer by a significant margin, but still better than a random guess at one's jon title. <br>
None of the variables were very influential in determining in one was a Data Engineer or not, but work_year again had the highest negative impact on the model at -5.988797e-04 meaning the more recent the year, the less likely one is to be a Data Engineer. <br>
Conversely, remote_ratio, again, had the highest positive impact at 3.114093e-03 on the model. So, the more remote a postition was, the more likely one is to be a Data Analyst, barely.

Data Scientist
----------------
Training and Testing Data Sets found at the links below:<br>
https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/processed/Data%20Scientist/DataScientist_X_Test.csv <br>
https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/processed/Data%20Scientist/DataScientist_y_Test.csv <br>
https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/processed/Data%20Scientist/DataScientist_X_Train.csv <br>
https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/processed/Data%20Scientist/DataScientist_y_Train.csv <br>
After running a logistic regression with 1000 iterations, the resulting confusion matrix is below:<br>
![image](https://user-images.githubusercontent.com/97635420/232327939-18c32558-c63b-4a30-b673-d8fba440d5d2.png)<br>
This logisitic regression finally classified some negative values, very few, but there are negative values regardless. This model was actually able to distinguish some observations as NOT Data Scientist. Granted the sensitivity is very poor at just 9% and the specificity is quite bad at 37.5%, but this is quite the improvement from the previous 2 job title classifications. The resulting accuracy rate was 72.13%, so this model is slightly worse than the Data Analyst model, but much better than the Data Engineer model. <br>
None of the variables were very influential in determining in one was a Data Scientist or not, but work_year had the highest negative impact on the model at -0.005280  meaning the more recent the year, the less likely one is to be a Data Scientist. <br>
We finally had a different highest positive impact variable of Large_company at .000056. Very little, but this means that the Larger the company, the more likely to be a Data Scientist.

Machine Learning Engineer
-------------------------
Training and Testing Data Sets found at the links below:<br>
https://github.com/dfarone02/Data-Science-JobSalaries/blob/main/data/processed/Machine%20Learning%20Engineer/Machine_Learning_Engineer_X_Test.csv <br>
https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/processed/Machine%20Learning%20Engineer/Machine_Learning_Engineer_y_Test.csv <br>
https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/processed/Machine%20Learning%20Engineer/Machine_Learning_Engineer_y_Train.csv <br>
https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/processed/Machine%20Learning%20Engineer/Machine_Learning_Engineerr_X_Train.csv <br>
After running a logistic regression with 1000 iterations, the resulting confusion matrix is below:<br>
![image](https://user-images.githubusercontent.com/97635420/232327967-b91b3574-5ec0-4851-8fef-ec9f16706118.png)<br>
As you can see, the model did not classify any negatives, so the predictor variables were too hard to distinguish among Machine Learning Engineer or other job fields, so our Sensitivity and Specificity measures were 0.0. Despite that, we had an accuracy rate of 83.61%, which is quite good all things considered. <br>
None of the variables were very influential in determining in one was a Machine Learning Engineer or not, but remote_ratio had the highest negative impact on the model at -1.967842e-03 meaning the more remote a position, the less likely one is to be a Machine Learning Engineer. <br>
Conversely, small_company had the highest positive impact on the model at 1.025060e-04. So, at smaller companies, one is more likely one is to be a Machine Learning Engineer.

### Back to Main Page: <br>
https://github.com/dfarone02/Data-Science-Job-Salaries#multi-output-multi-level-random-forest-classification

