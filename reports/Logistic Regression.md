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
![image](https://user-images.githubusercontent.com/97635420/232331018-922c7aae-7194-4da8-ac21-813adbba93e7.png)<br>
As you can see, the model did not classify any Data Analysts, so the predictor variables were too hard to distinguish among Data Analyst or other job fields, so our Sensitivity and Specificity measures were 0.0. Dpesite that, we had an accuracy rate of 77.05%, which is quite good all things considered. <br>
None of the variables were very influential in determining in one was a Data Analyst or not, but work_year had the highest negative impact on the model meaning the more recent the year, the more likely one is to be a Data Analyst. <br>
Conversely, remote_ratio had the highest positive impact on the model. So, the more remote a postition was, the less likely one is to be a Data Analyst

Data Engineer
--------------
Training and Testing Data Sets found at the links below:<br>
https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/processed/Data%20Engineer/DataEngineer_X_Test.csv <br>
https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/processed/Data%20Engineer/DataEngineer_y_Test.csv <br>
https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/processed/Data%20Engineer/DataEngineer_X_Train.csv <br>
https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/processed/Data%20Engineer/DataEngineer_y_Train.csv <br>
After running a logistic regression with 1000 iterations, the resulting confusion matrix is below:<br>
![image](https://user-images.githubusercontent.com/97635420/232331152-83d361de-5320-45b8-a4e3-09ceb3357730.png)<br>
As you can see, the model did not classify any Data Engineers, so the predictor variables were too hard to distinguish among Data Engineer or other job fields, so our Sensitivity and Specificity measures were 0.0. Despite that, we had an accuracy rate of 65.57%, which is worse than the Data Engineer by a significant margin, but still better than a random guess at one's jon title. <br>
None of the variables were very influential in determining in one was a Data Engineer or not, but work_year again had the highest negative impact on the model at -5.988797e-04 meaning the more recent the year, the more likely one is to be a Data Engineer. <br>
Conversely, remote_ratio, again, had the highest positive impact at 3.114093e-03 on the model. So, the less remote a postition was, the more likely one is to be a Data Engineer, barely.

Data Scientist
----------------
Training and Testing Data Sets found at the links below:<br>
https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/processed/Data%20Scientist/DataScientist_X_Test.csv <br>
https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/processed/Data%20Scientist/DataScientist_y_Test.csv <br>
https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/processed/Data%20Scientist/DataScientist_X_Train.csv <br>
https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/processed/Data%20Scientist/DataScientist_y_Train.csv <br>
After running a logistic regression with 1000 iterations, the resulting confusion matrix is below:<br>
![image](https://user-images.githubusercontent.com/97635420/232331263-bd76ca31-0920-4b04-be8e-5e05dc750487.png)<br>
This logisitic regression finally classified some Data Scientists, very few, but there are Data Scientists regardless. This model was actually able to distinguish some observations as NOT Data Scientist. Granted the sensitivity is very poor at just 9% and the specificity is quite bad at 37.5%, but this is quite the improvement from the previous 2 job title classifications. The resulting accuracy rate was 72.13%, so this model is slightly worse than the Data Analyst model, but much better than the Data Engineer model. <br>
None of the variables were very influential in determining in one was a Data Scientist or not, but work_year had the highest negative impact on the model at -0.005280  meaning the more recent the year, the more likely one is to be a Data Scientist. <br>
We finally had a different highest positive impact variable of Large_company at .000056. Very little, but this means that the Larger the company, the less likely to be a Data Scientist.

Machine Learning Engineer
-------------------------
Training and Testing Data Sets found at the links below:<br>
https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/processed/Machine%20Learning%20Engineer/Machine_Learning_Engineer_X_Test.csv <br>
https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/processed/Machine%20Learning%20Engineer/Machine_Learning_Engineer_y_Test.csv <br>
https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/processed/Machine%20Learning%20Engineer/Machine_Learning_Engineer_y_Train.csv <br>
https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/processed/Machine%20Learning%20Engineer/Machine_Learning_Engineerr_X_Train.csv <br>
After running a logistic regression with 1000 iterations, the resulting confusion matrix is below:<br>
![image](https://user-images.githubusercontent.com/97635420/232331355-40c9b6a1-3120-4f71-b2d1-2cd768bac33c.png)<br>
As you can see, the model did not classify any Machine Learning Engineers, so the predictor variables were too hard to distinguish among Machine Learning Engineer or other job fields, so our Sensitivity and Specificity measures were 0.0. Despite that, we had an accuracy rate of 83.61%, which is quite good all things considered. <br>
None of the variables were very influential in determining in one was a Machine Learning Engineer or not, but remote_ratio had the highest negative impact on the model at -1.967842e-03 meaning the more remote a position, the more likely one is to be a Machine Learning Engineer. <br>
Conversely, small_company had the highest positive impact on the model at 1.025060e-04. So, at smaller companies, one is less likely one is to be a Machine Learning Engineer. This suggests that Machine Learning Engineer is a much older field than Data Analyst, Data Engineer, or Data Scientist.

Comparing All 4 Logisitc Regression Models
------------------------------------------
The figure below shows the ROC curves for each of the 4 Logistic Regression models:<br>
![image](https://user-images.githubusercontent.com/97635420/232331792-da2a811c-ff3e-4b20-add3-b54a4908c9ea.png)<br>
A perfectly diagonal curve means that a model cannot distinguish between 2 classes well at all, which is exactly what happened with the Data Analyst, Data Engineer, and Machine Learning Engineer. <br>
A classifier that perfectly dsitinguishes between classes would look like an upside down "L," the data scientist curve is nowhere close to that, but there is some angle to it. <br>
Below is a summary of all of the scores for each of the 4 Logistic Regression Models: <br>
![image](https://user-images.githubusercontent.com/97635420/232332004-b8afca66-9ea3-47eb-9e40-fb8e4faa30e7.png),br>
While, every model is convincingly accurate, this is more for determining if an individual is not the specified career field in each case. This is explained better as all models have a very poor ROC AUC score, showing us that the model struggled to distinguish between career fields. Regardless, Data Scientist was easily the best predicted Career Field using Logistic Regression since it was the only model that actually classifed individuals as Data Scientists.


### Back to Main Page: <br>
https://github.com/dfarone02/Data-Science-Job-Salaries#multi-output-multi-level-random-forest-classification <br>
