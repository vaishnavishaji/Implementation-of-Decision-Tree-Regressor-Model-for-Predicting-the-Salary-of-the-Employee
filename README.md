# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the required libraries.
2.Upload and read the dataset.
3.Gather information and presence of null in the dataset.
4.From sklearn.tree import DecisionTreeRegressor and fir the model. 5.Find the mean square error and r squared score value of the model.
5.Check the trained model.

## Program:
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
```
Developed by: Vaishnavi S.A
RegisterNumber:212223220119

import pandas as pd
data = pd.read_csv("Salary.csv")
data.head()
data.info()
data.isnull().sum()
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()
x= data[["Position","Level"]]
y=data["Salary"]
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test = train_test_split(x,y,test_size = 0.2,random_state = 2)
from sklearn.tree import DecisionTreeRegressor
dt = DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred = dt.predict(x_test)
from sklearn import metrics
mse = metrics.mean_squared_error(y_test,y_pred)
mse
r2= metrics.r2_score(y_test,y_pred)
r2
dt.predict([[5,6]])


```





## Output:

## Initial Dataset :

![173230536-7245e0ea-a021-4411-957c-7bee1e78dd1c](https://github.com/vaishnavishaji/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/151444759/a67c761e-8061-402e-9c62-71dfd3272dd8)

## Dataset Information :

![173230601-87c26093-c70a-4dad-ab83-792fb21cbb5e](https://github.com/vaishnavishaji/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/151444759/64a73ce0-04ae-46f1-899d-4ad24349a8d0)

## Null Dataset:

![173230704-2d0d9052-ed13-4427-8b71-eb211e232fce](https://github.com/vaishnavishaji/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/151444759/32a0e10c-acd7-47cc-b25c-08127442dc12)

## Encoded Dataset:

![173230794-f1c456d8-134a-4180-a887-a93ad3fc1deb](https://github.com/vaishnavishaji/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/151444759/90eabc58-8795-4e5f-be82-d52280ca8543)

## Mean Square Error Value:

![173230842-5c93b33e-f752-4132-b8ff-a933e255247c](https://github.com/vaishnavishaji/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/151444759/671936a1-bedd-456c-8a03-ea5ee7d485d9)

## R squared score:

![173230869-6e4bd2e6-b940-4301-b6e5-10ce651d6b9f](https://github.com/vaishnavishaji/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/151444759/003dff4e-e0c0-4ccb-bff6-829979db2518)

## Predictted Value:

![173230932-e7c8269c-1ceb-43aa-8f11-290102dd98d4](https://github.com/vaishnavishaji/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/151444759/28d4aba6-a92f-4ff8-b1a5-f2156666fed8)

## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
