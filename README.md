# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1
Import the required libraries and load the car emission dataset.
### Step2
Select Weight and Volume as input features and CO2 as the target variable.
### Step3
Create and train the Linear Regression model using the dataset
### Step4
Provide new values for Weight and Volume and use the model to predict CO₂ emission.
### Step5
Display the regression coefficients, intercept, and predicted CO₂ value.

## Program:
```
Name: Mohan rahul S
reg no : 26018134


import pandas as pd

url = "https://raw.githubusercontent.com/arunpradeep-sec/Linear-Algebra-Lab/main/carsemission.csv"

df = pd.read_csv(url)

df.to_csv("carsemission.csv", index=False)

print("Dataset loaded successfully.")

import pandas as pd

from sklearn import linear_model

df = pd.read_csv("carsemission.csv")

X = df[['Weight', 'Volume']]

y = df['CO2']

regr = linear_model.LinearRegression()

regr.fit(X, y)
print('Coefficients:', regr.coef_)

print('Intercept:', regr.intercept_)

input_data = pd.DataFrame({'Weight': [3300], 'Volume': [1300]})

predictedCO2 = regr.predict(input_data)

print('Predicted CO2 for the corresponding weight and volume:', predictedCO2)





```
## Output:

### Insert your output

<img width="733" height="92" alt="image" src="https://github.com/user-attachments/assets/be92cea9-2242-4f98-8754-ec76f687026c" />


## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
