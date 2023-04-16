To run the MultiOuputMultiClassification Model to classify Data Analyst, Data Engineer, Data Scientist, Machine Learning Engineer:

https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/notebooks/AdvancedClassification.ipynb

The training and testing sets for these notbeooks can be found at the below link:

https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/processed/All%20Fields/X_Test.csv <br>
https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/processed/All%20Fields/y_Test.csv <br>
https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/processed/All%20Fields/X_Train.csv <br>
https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/data/processed/All%20Fields/y_Train.csv <br>

Results from the entire model:
------------------------------
To start off, I built a random forest model that had 100 estimators using the training set that included everyhting, but Data Analyst, Data Engineer, Data Scientist, Machine Learning Engineer. Once that model was built, I fit the MultiOutput Classifier on that Random Forest. Resulting in these scores:<br>
![image](https://user-images.githubusercontent.com/97635420/232333096-a0b56f0e-a8ff-4b78-b1f6-1ae2a6f53ce0.png)<br>

I wanted to try and improve these results, so I ran a grid search with 10 cross-validations, which took 4 hours to run, and these were the scores:<br>
![image](https://user-images.githubusercontent.com/97635420/232333357-1ead099d-4013-47fe-93de-50c4eb166aa7.png)<br>
As you can see, this model peforms quite poorly. This is expected, of course, when handling 4 response variables to predict at a time.33.6% of the time, all 4 career fields were correctly classified. The combination of the 4 career fields was correctly predicted as the right field 33.6% of the time as well. Lastly, for each sequence of the 4 career fields, the predictions matched the actual observations only 44.6% of the time.

Breaking Down Results to Each Career Field within the Multi-Classification Model:
----------------------------------------------------------------------------------
Looking at the Variable Importance Graphs for Each of the 4 Career Fields in the Jupyter Notebook, we see that in every case, Salary, Wrok_Year, and Remote Ratio were the 3 most important factors in determining if an individual was a Data Analyst, Data Engineer, Data Scientist, or Machine Learning Engineer. After those the model suggests that: <br>
  Data Analyst - midsize company meaning Data Analysts are more likely found at a midsize company than other titles.<br>
  Data Engineer - GBP- perhaps Data Engineer title is more common in Great Britain than in other countires.<br>
  Data Scientist - Large Company: These titles are found more often at the larger companies than other job titles.<br>
  Machine Learning Engineer - Senior Experience: This position requires greater experience than other titles may.<br>

![image](https://user-images.githubusercontent.com/97635420/232334378-188eebde-2c00-4a4a-9fd3-c20d47a06f93.png)<br>
The above figure shows the ROC curves for each career field within the mult-classification model. Each curve is better than its corresponding one in the logistic regression model. Each one roughly resembles an upside down "L" shape as opposed to a diagonal line. The Multi-Ouput Classification model does a better job at distinguishing between career fields than the Logistic Regression did, and within this model, Data Analyst was the best separated among the 4 titles. <br>

Lastly, I want to examine how the model's metrics compare to one another: <br>
![image](https://user-images.githubusercontent.com/97635420/232334535-6572af9b-ae59-478d-8dd2-8ed63918b571.png)<br>
As shown above, the model is not very accurate, specific, or sensitivev when having to evaluate 4 career fields at once, but when we break it up, we find reported scores much, much, much better than the logistic regression was. Data Analyst, Data Engineer, Data Scientist, and Machine Learning Engineer all have scores for sensitivity and specificity in this model as opposed to logistic regression where only Data Scientist could produce these metrics. Data Scientist and Data Engineer did not report very good scores, which suggests that these titles may be harder to distinguish in the job market.  Machine Learning Engineer was the most accurate, but considering Data Analyst was only 1% less accurate and had significantly better Sensitivity and Specificity than any other career field. Data Analyst is easily the best classified career field of the four, which aligns with this field having the best ROC curve of the 4 choices.

### Back to Main Page: <br>
https://github.com/dfarone02/Data-Science-Job-Salaries#the-big-takeaways
