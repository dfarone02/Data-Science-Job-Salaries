Data Science Job Salaries Analysis
==============================
Problem
-------------------
In the Spring of 2023, I spent most of my final semester as an undergraudate on LinkedIn, Indeed, and other job boards searching for careers for my Data Science degree. Data Science is such an ambiguous term and there are countless titles in the area. So how do these job boards give accurate postings when I type "Data Scientist Jobs" in the search bar? How do these networking sites decide what is a Data Scientist or Data Analyst or Data Engineer or Machine Learning Engineer? 

Solution
---------------------
The answer is through classification models that are much more advanced than I have examined in this repository. This project features a dataset consisting of 700 individuals in 4 career fields of Data Science:( Data Scientist, Data Analyst, Machine Learning Engineer, Data Engineer). The dataset contains features such as the individual's degree, work experience, company, geographic location, age, and of course, job title and salary. After performing some Exploratory Data Analysis, Feature Engineering, and Testing and Training Data Splits, this project produced 2 models. The first, a Decision Tree for each job title (Data Analyst, Data Engineer, Data Scientist, and Machine Learning Engineer) to deterime if an individual is in that job position or not. The second set of models is a Mutlti-Label Multi-Output Classifier (using Random Forest Classifier) model, which is a more advanced method of classification, but looks to achieve the same objective as the logistic regression model, but all in one model instead of 4 different iterations of logistic regression. Both of these models will be evaluated and explained in further detail. The title of Data Scientist is generally the most desired title of these 4 job areas. It also appears the most in the dataset of any job title. I have the goal of the Data Scientist field being the best classified of the four job titles.

What is Logistic Regression?
----------------------------
Logistic regression estimates the probability of an event occurring (like Data Scientist OR NOT). Since the outcome is a probability, the dependent variable is bounded between 0 (Values below 0.5 are NOT a Data Scientist) and 1 (Values equal or greater than 0.5 ARE a Data Scientist). Logistic regression takes the best combination of predictor variables to maximize the best parameter estimate (Data Scientist/NOT). 

![image](https://user-images.githubusercontent.com/97635420/222556592-36500ddd-0d5e-4164-aebe-8eeaeccc6c3d.png)

The above image is the representation of the logistic regression where the natural log of the probability that an individual is a Data Scientist is divided by the probability they are not is set equal to the model intercept and the rate of change for an increase of 1 for a given parameter.

![image](https://user-images.githubusercontent.com/97635420/222558372-cc5bfbb8-747b-450a-b55c-6634ebffeda8.png)

Alternatively, the model can be represented in a way that is just like the Ordinary Least Squares Regression. The only difference is that the values of the model intercept and the rate of change for an increase of 1 for a given parameter are used to estimate the probability of an observation belonging to a class (Data Scientist Y/N) instead of a value for that observation.

What are Random Forests?
--------------------------
A decision tree is built upon a series of questions to classify observations in a dataset. While it cannot be represented in the form of a linear equation, it is very useful in a visual representation in a tree-shaped image like the one below as an example:

![image](https://user-images.githubusercontent.com/97635420/222566572-c6ba908a-b55c-4683-a8fe-f9b7a18a9cb3.png)

One decision tree is prone to overfitting, so we compute a large number of decision trees which operate as a collective of trees (aka a Forest). Each tree spits out its own prediction, and the individual tree in the Random Forest with the best scores becomes THE prediction for the Random Forest Model. A Random Forest almost always out performs a single Decision Tree because multiple uncorrelated models can work together to produce aggregate predictions that are more accuracte than any individual prediction. The trees in the Forest essentially protect each other from individual errors through a process called bagging. The bagging process allows each tree to train on random and different sets of data, but each tree in the random forest has a different set of features for its decision making criteria.

What on Earth is Multi-Output Mutlti-Level Classification (using Random Forest)?
---------------------------------------------------------------------------------
This approach to classification is based off a Random Forest model, and functions almost exactly like a Random Forest model like this one: 

![image](https://user-images.githubusercontent.com/97635420/228935501-d3c6897f-939a-488d-a93f-f5567aea787f.png)

Except, we are looking for more than 1 target variable, which all must be binary. In the context of this problem, there are 4 targer variables in this classifier for Data Analyst, Data Engineer, Data Scientist, and Machine Learning Engineer. There are only a handfull of packages that can handle multiplke output target variables, and the one we are using for this probelm is the MultiOutputClassifier from scikit learnm which fits one binary classifier per each career field variable. Like a random forest, model scores, plots, and confusion matrices can be generated, but it is considerably more tedious and computationally more expensive to separate the target classes and iterate through the predictions to analyze not only the entire model's predictive power, but also the predicitve power of each sub-model for each of our 4 job title classes.

Exploratory Data Analysis
---------------------------
data/external/ds_salaries_external.csv

Feature Engineering
---------------------------


Training and Testing Data Sets
--------------------------------


Implementing Logistic Regression
---------------------------------


Implementing Multi-Output Multi-Level Random Forest Classification
-------------------------------------------------------------------


References
---------
https://www.ibm.com/topics/logistic-regression <br>
https://towardsdatascience.com/understanding-random-forest-58381e0602d2
https://towardsdatascience.com/essential-guide-to-multi-class-and-multi-output-algorithms-in-python-3041fea55214

Project Organization 
----------------------------

    ├── Makefile           <- Makefile with commands like `make data` or `make train`
    ├── README.md          <- The top-level README for developers using this project.
    ├── data
    │   ├── external       <- Data from third party sources.
    │   ├── interim        <- Intermediate data that has been transformed.
    │   ├── processed      <- The final, canonical data sets for modeling.
    │   └── raw            <- The original, immutable data dump.
    │
    ├── docs               <- A default Sphinx project; see sphinx-doc.org for details
    │
    ├── models             <- Trained and serialized models, model predictions, or model summaries
    │
    ├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
    │                         the creator's initials, and a short `-` delimited description, e.g.
    │                         `1.0-jqp-initial-data-exploration`.
    │
    ├── references         <- Data dictionaries, manuals, and all other explanatory materials.
    │
    ├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
    │   └── figures        <- Generated graphics and figures to be used in reporting
    │
    ├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
    │                         generated with `pip freeze > requirements.txt`
    │
    ├── setup.py           <- makes project pip installable (pip install -e .) so src can be imported
    ├── src                <- Source code for use in this project.
    │   ├── __init__.py    <- Makes src a Python module
    │   │
    │   ├── data           <- Scripts to download or generate data
    │   │   └── make_dataset.py
    │   │
    │   ├── features       <- Scripts to turn raw data into features for modeling
    │   │   └── build_features.py
    │   │
    │   ├── models         <- Scripts to train models and then use trained models to make
    │   │   │                 predictions
    │   │   ├── predict_model.py
    │   │   └── train_model.py
    │   │
    │   └── visualization  <- Scripts to create exploratory and results oriented visualizations
    │       └── visualize.py
    │
    └── tox.ini            <- tox file with settings for running tox; see tox.readthedocs.io


--------

<p><small>Project based on the <a target="_blank" href="https://drivendata.github.io/cookiecutter-data-science/">cookiecutter data science project template</a>. #cookiecutterdatascience</small></p>

