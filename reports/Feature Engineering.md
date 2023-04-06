In this section of the project, we are going to conduct Feature Engineering from this notebook:
https://github.com/dfarone02/Data-Science-Job-Salaries/blob/200620f4b7e4a4064750887776d182f0ef495b19/notebooks/Feature%20Engineering.ipynb

Using the external data like the last section:
https://github.com/dfarone02/Data-Science-Job-Salaries/blob/78ce310390192d267cf8469faeeae15fcad014bc/data/external/ds_salaries_external.csv

To begin this process, I first looked at the unique values for each variable in the dataset to examine the ease of creating dummy variables for categorical columns. Taking that information into account, I created dummy varibales for: <br>
    - Experience Level: (Entry Experience, Expert Experience, Mid Experience, Senior Experience) <br>
    - Employment Type: (Full-Time OR Not Full-Time)<br>
    - (Obviously) Job Title: (Data Analyst, Data Engineer, Data Scientist, Machine Learning Engineer)<br>
    - Salary Currency: (Dollar, Euro, Pound, Rupee, or Other)<br>
    - Employee Residence: (US OR Not US)<br>
    - Company Location (US OR Not US)<br>
    - Company Size: (Large Company, Midsize Company, Small Company)<br>
    - Salary_in_USD: Numerical, so no changes made<br>
    
 That is about all the Feature Engineering needed, so this new data:
 https://github.com/dfarone02/Data-Science-Job-Salaries/blob/78ce310390192d267cf8469faeeae15fcad014bc/data/interim/ds_salaries_interim.csv
 
 Will be used to create the training and testing datasets to build the 2 classification models in this project.
    
### Back to Main Page: <br>
https://github.com/dfarone02/Data-Science-Job-Salaries/tree/2cdde691b82e1463ec560e61b672dae4931790c4#readme
