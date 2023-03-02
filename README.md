Data Science Job Salaries Analysis
==============================

This project features a dataset consisting of 700 individuals in 4 career fields of Data Science:( Data Scientist, Data Analyst, Machine Learning Engineer, Data Engineer). The dataset contains features such as the individual's degree, work experience, company, geographic location, age, and of course, job title and salary. After performing some Exploratory Data Analysis, Feature Engineering, and Testing and Training Data Splits, this project produced 2 models. The first, a Decision Tree for each job title (Data Analyst, Data Engineer, Data Scientist, and Machine Learning Engineer) to deterime if an individual is in that job position or not. The second set of models is a Boosted Decision Tree Classifier model, which is a more advanced method of classification, but looks to achieve the same objective as the logistic regression model. Both of these models will be evaluated and explained in further detail. The title of Data Scientist is generally the most desired title of these 4 job areas. It also appears the most in the dataset of any job title. I have the goal of the Data Scientist field being the best classified of the four job titles.

Logistic Regression
--------------------
Logistic regression estimates the probability of an event occurring (like if an individual IS a Data Scientist OR NOT). Since the outcome is a probability, the dependent variable is bounded between 0 (Values below 0.5 are NOT a Data Scientist) and 1 (Values equal or greater than 0.5 ARE a Data Scientist). Logistic regression takes the best combination of predictor variables to maximize the best parameter estimate (Data Scientist/NOT). 
![image](https://user-images.githubusercontent.com/97635420/222556592-36500ddd-0d5e-4164-aebe-8eeaeccc6c3d.png)
The above image is the representation of the logistic regression where the natural log of the probability that an individual is a Data Scientist is divided by the probability they are not is set equal to the model intercept and the rate of change for an increase of 1 for a given parameter.
![image](https://user-images.githubusercontent.com/97635420/222558372-cc5bfbb8-747b-450a-b55c-6634ebffeda8.png)
Alternatively, the model can be represented in a way that is just like the Ordinary Least Squares Regression. The only difference is that the values of the model intercept and the rate of change for an increase of 1 for a given parameter are used to estimate the probability of an observation belonging to a class (Data Scientist Y/N) instead of a value for that observation.



Project Organization
------------

![Uploading image.png…]()    ├── Makefile           <- Makefile with commands like `make data` or `make train`
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
