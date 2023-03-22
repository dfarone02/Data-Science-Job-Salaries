Data Science Job Salaries Analysis
==============================
Problem
-------------------
In the Spring of 2023, I spent most of my final semester as an undergraudate on LinkedIn, Indeed, and other job boards searching for careers for my Data Science degree. Data Science is such an ambiguous term and there are countless titles in the area. So how do these job boards give accurate postings when I type "Data Scientist Jobs" in the search bar? How do these networking sites decide what is a Data Scientist or Data Analyst or Data Engineer or Machine Learning Engineer? 

Solution
---------------------
The answer is through classification models that are much more advanced than I have examined in this repository. This project features a dataset consisting of 700 individuals in 4 career fields of Data Science:( Data Scientist, Data Analyst, Machine Learning Engineer, Data Engineer). The dataset contains features such as the individual's degree, work experience, company, geographic location, age, and of course, job title and salary. After performing some Exploratory Data Analysis, Feature Engineering, and Testing and Training Data Splits, this project produced 2 models. The first, a Decision Tree for each job title (Data Analyst, Data Engineer, Data Scientist, and Machine Learning Engineer) to deterime if an individual is in that job position or not. The second set of models is a Boosted Decision Tree Classifier model, which is a more advanced method of classification, but looks to achieve the same objective as the logistic regression model. Both of these models will be evaluated and explained in further detail. The title of Data Scientist is generally the most desired title of these 4 job areas. It also appears the most in the dataset of any job title. I have the goal of the Data Scientist field being the best classified of the four job titles.

Logistic Regression
--------------------
Logistic regression estimates the probability of an event occurring (like Data Scientist OR NOT). Since the outcome is a probability, the dependent variable is bounded between 0 (Values below 0.5 are NOT a Data Scientist) and 1 (Values equal or greater than 0.5 ARE a Data Scientist). Logistic regression takes the best combination of predictor variables to maximize the best parameter estimate (Data Scientist/NOT). 

![image](https://user-images.githubusercontent.com/97635420/222556592-36500ddd-0d5e-4164-aebe-8eeaeccc6c3d.png)

The above image is the representation of the logistic regression where the natural log of the probability that an individual is a Data Scientist is divided by the probability they are not is set equal to the model intercept and the rate of change for an increase of 1 for a given parameter.

![image](https://user-images.githubusercontent.com/97635420/222558372-cc5bfbb8-747b-450a-b55c-6634ebffeda8.png)

Alternatively, the model can be represented in a way that is just like the Ordinary Least Squares Regression. The only difference is that the values of the model intercept and the rate of change for an increase of 1 for a given parameter are used to estimate the probability of an observation belonging to a class (Data Scientist Y/N) instead of a value for that observation.

Gradient Boosted Decision Tree
------------------------------
A decision tree is built upon a series of questions to classify observations in a dataset. While it cannot be represented in the form of a linear equation, it is very useful in a visual representation in a tree-shaped image like the one below as an example:

![image](https://user-images.githubusercontent.com/97635420/222566572-c6ba908a-b55c-4683-a8fe-f9b7a18a9cb3.png)

One decision tree is prone to overfitting, so methods like gradient boosting combines a set of decision trees for a better fit. As opposed to a bootstrapped method of modeling, each new tree is fit on the residuals of the previous tree, and thus seeks to minimize the errors each go using a logarithmic loss function. The final tree takes the best elements fo each tree to produce the strongest results each step. The model performs quite slowly, but a model that takes more time to learn produces better findings. It is worth noting that slower performance requires more trees to optimize, but as a user adds more trees to the model, unlike a decision tree, a user should be careful with overfitting in the model and the sensitivity to outliers. Despite that the gradient boosting decision tree is more efficient and accurate than most classification and regression models and can handle mixed types of features without any preprocessing.
    
<b> YOU AIN'T DONE YET</b>

References
---------
https://www.ibm.com/topics/logistic-regression
https://towardsdatascience.com/gradient-boosted-decision-trees-explained-9259bd8205af

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

