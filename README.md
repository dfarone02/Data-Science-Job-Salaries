Problem
-------------------
In the Spring of 2023, I spent most of my final semester as an undergraduate on LinkedIn, Indeed, and other job boards searching for careers for my Data Science degree. Data Science is such an ambiguous term and there are countless titles in the area. So how do these job boards give accurate postings when I type "Data Scientist Jobs" in the search bar? How do these networking sites decide what is a Data Scientist or Data Analyst or Data Engineer or Machine Learning Engineer? 

Solution
---------------------
The answer is through classification models that are much more advanced than I have examined in this repository. This project features a dataset consisting of 700 individuals in 4 career fields of Data Science:( Data Scientist, Data Analyst, Machine Learning Engineer, Data Engineer). The dataset contains the below features:

![image](https://user-images.githubusercontent.com/97635420/232322604-5fd7d759-fdfb-4d67-b118-88f7833c756d.png)

After performing some Exploratory Data Analysis, Feature Engineering, and Testing and Training Data Splits, this project produced 2 models. First, a Decision Tree for each job title (Data Analyst, Data Engineer, Data Scientist, and Machine Learning Engineer) to determine if an individual is in that job position or not. The second set of models is a Mutlti-Label Multi-Output Classifier (using Random Forest Classifier) model, which is a more advanced method of classification, but looks to achieve the same objective as the logistic regression model, but all in one model instead of 4 different iterations of logistic regression. Both of these models will be evaluated and explained in further detail. The title of Data Scientist is generally the most desired title of these 4 job areas. It also appears the most in the dataset of any job title. I have the goal of the Data Scientist field being the best classified of the four job titles.

### What is Logistic Regression?
Logistic regression estimates the probability of an event occurring (like Data Scientist OR NOT). Since the outcome is a probability, the dependent variable is bounded between 0 (Values below 0.5 are NOT a Data Scientist) and 1 (Values equal or greater than 0.5 ARE a Data Scientist). Logistic regression takes the best combination of predictor variables to maximize the best parameter estimate (Data Scientist/NOT). 

![image](https://user-images.githubusercontent.com/97635420/222556592-36500ddd-0d5e-4164-aebe-8eeaeccc6c3d.png)

The above image is the representation of the logistic regression where the natural log of the probability that an individual is a Data Scientist is divided by the probability, they are not is set equal to the model intercept and the rate of change for an increase of 1 for a given parameter.

![image](https://user-images.githubusercontent.com/97635420/222558372-cc5bfbb8-747b-450a-b55c-6634ebffeda8.png)

Alternatively, the model can be represented in a way that is just like the Ordinary Least Squares Regression. The only difference is that the values of the model intercept and the rate of change for an increase of 1 for a given parameter are used to estimate the probability of an observation belonging to a class (Data Scientist Y/N) instead of a value for that observation.

### What are Random Forests?
A decision tree is built upon a series of questions to classify observations in a dataset. While it cannot be represented in the form of a linear equation, it is very useful in a visual representation in a tree-shaped image like the one below as an example:

![image](https://user-images.githubusercontent.com/97635420/222566572-c6ba908a-b55c-4683-a8fe-f9b7a18a9cb3.png)

One decision tree is prone to overfitting, so we compute a large number of decision trees which operate as a collective of trees (aka a Forest). Each tree spits out its own prediction, and the individual tree in the Random Forest with the best scores becomes THE prediction for the Random Forest Model. A Random Forest almost always outperforms a single Decision Tree because multiple uncorrelated models can work together to produce aggregate predictions that are more accurate than any individual prediction. The trees in the Forest essentially protect each other from individual errors through a process called bagging. The bagging process allows each tree to train on random and different sets of data, but each tree in the random forest has a different set of features for its decision-making criteria.

### What on Earth is Multi-Output Mutlti-Level Classification (using Random Forest)?
This approach to classification is based off a Random Forest model, and functions almost exactly like a Random Forest model like this one: 

![image](https://user-images.githubusercontent.com/97635420/228935501-d3c6897f-939a-488d-a93f-f5567aea787f.png)

Except, we are looking for more than 1 target variable, which all must be binary. In the context of this problem, there are 4 target variables in this classifier for Data Analyst, Data Engineer, Data Scientist, and Machine Learning Engineer. There are only a handful of packages that can handle multiple output target variables, and the one we are using for this problem is the MultiOutputClassifier from scikit learn which fits one binary classifier per each career field variable. Like a random forest, model scores, plots, and confusion matrices can be generated, but it is considerably more tedious and computationally more expensive to separate the target classes and iterate through the predictions to analyze not only the entire model's predictive power, but also the predictive power of each sub-model for each of our 4 job title classes.

### Let's Take a Look at What a Confusion Matrix is

A confusion matrix is essentially a graphical depiction of the results of a classification model like the one shown below:

![image](https://user-images.githubusercontent.com/97635420/232326526-a09d5fb6-b839-470e-9796-543fb51de6a4.png)

Let's explain this in terms of my job title classification using data scientist as an example: <br>
    True Positive (Top Left): The predicted value = Data Scientist and the actual value = Data Scientist <br>
    False Positive (Top Right): The predicted value = Data Scientist and the actual values = Not Data Scientist <br>
    False Negative (Bottom Left): The predicted value = Not Data Scientist and the actual value = Data Scientist <br>
    True Negative (Bottom Right): The predicted value = Not Data Scientist and the actual value = Not Data Scientist <br>
 
### Let's Understand What Measures Evaluate Classification Models

Accuracy: measure of how many observations are predicted correctly <br>
![image](https://user-images.githubusercontent.com/97635420/232326894-d6595737-ac3d-4633-a743-611a7fe73996.png) <br>

Sensitivity: How many Data Scientists were predicted correctly <br>
![image](https://user-images.githubusercontent.com/97635420/232326975-95c3fa17-0cb1-4f55-9489-55cfa2efadba.png)<br>

Specificity: How many Data Scientists are actually Data Scientists <br>
![image](https://user-images.githubusercontent.com/97635420/232327047-3a6f5426-a675-48e9-84d0-168a68d3a7b8.png) <br>

AUC: How efficient the model is at distinguishing between a Data Scientist and Not Data Scientist<br>
Calculation comes from integral using True Positives and False Positives from the predicted model and is not worth showing<br>

***Classification models will not classify observations as negative if the model cannot distinguish between Data Scientist or Not*** <br>
***This means that Specificity and Sensitivity will be ZERO or close to it without any negatives in the confusion matrix***

Job Title Classification Implementation
---------------------------------------
To run the notebooks for implementation, make sure you save this document to your working directory:
https://raw.githubusercontent.com/dfarone02/Data-Science-Job-Salaries/main/src/required_libraries.py
Each of the below implementation sections will have you click a link to view a description and summary for that section for the sake of saving space on this README.md file.

### Exploratory Data Analysis
https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/reports/Exploratory%20Data%20Analysis.md

### Feature Engineering
https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/reports/Feature%20Engineering.md

### Training and Testing Data Sets
https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/reports/Training%20and%20Testing%20Sets.md

### Logistic Regression
https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/reports/Logistic%20Regression.md

### Multi-Output Multi-Level Random Forest Classification
https://github.com/dfarone02/Data-Science-Job-Salaries/blob/main/reports/Multi%20Classification.md

The Big Takeaways
-------------------
I decided to first use a Logistic Regression model to classify individuals as a Data Analyst, Data Engineer, Data Scientist, or Machine Learning Engineer. I chose that model format because it is the simplest classification model, and EASIEST to understand by far, since it is in linear regression form. The specificity, sensitivity, and AUC scores for the Data Analyst, Data Engineer, Data Scientist, and Machine Learning Engineer models were practically useless as these models struggled to classify a job as the specific field. That being said, these models were very accurate...at predicting that an individual did not belong in that specific career field, which was not the accuracy measure I had hoped for by any means. But, this could definitely still be useful for a site like LinkedIn as they could filter out job titles that did not match an individual's search.<br>

I was curious to see if I could classify all 4 career fields at once using ONE model. Thanks to MultiOuput MultiClassifcation using Random Forest, I was able to accomplish this. Unfortunately, taking 4 variables at once when models usually only take one is about as difficult as you would expect. Accuracy, Sensitivity, and Specificity were all below 50%. That is pretty awful. But other than accuracy, it is much better than any of the logistic regression models. In breaking down the MultiClassification model to look at each career field. Data Analyst, Data Engineer, Data Scientist, and Machine Learning Engineer outperformed their Logistic Regression counterpart. <br>

This is an instance where just because a model is more interpretable (Logistic Regression) does not make it a better performing one (MultiClassification)<br>

I wanted Data Scientist to be the best classified position of the 4, which it easily was in the Logistic Regression. However, it would be much safer to look into the MultiClassification model's performance. In that case, Data Analyst is very reliable to look at. I think that Data Analyst being the best classified position would be most beneficial to a Job Board like Indeed.com because that is considered the entry position in Data Science and what the most individuals are going to look for. <br>

If anything, this project shows just how similar careers in Data Science are and how arbitrary the job title is. So... the next time you are on a Job Board complaining about how bad your matches and suggested jobs are...cut them some slack because it is surprisingly difficult to distinguish between job titles.

References
---------
https://www.ibm.com/topics/logistic-regression <br>
https://towardsdatascience.com/understanding-random-forest-58381e0602d2
https://towardsdatascience.com/essential-guide-to-multi-class-and-multi-output-algorithms-in-python-3041fea55214
https://towardsdatascience.com/understanding-confusion-matrix-a9ad42dcfd62
https://towardsdatascience.com/how-to-calculate-use-the-auc-score-1fc85c9a8430
