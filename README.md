# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the libraries and read the data frame using pandas.
2. Calculate the null values present in the dataset and apply label encoder.
3. Determine test and training data set and apply decison tree regression in dataset.
4. Calculate Mean square error,data prediction and r2.

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: THRIKESWAR.P
RegisterNumber:  212222230162

import pandas as pd
data=pd.read_csv("/content/Salary.csv")

data.head()

data.info()

data.isnull().sum()

from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()

x=data[["Position","Level"]]
y=data["Salary"]

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)


from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)

from sklearn import metrics
mse=metrics.mean_squared_error(y_test,y_pred)
mse

r2=metrics.r2_score(y_test,y_pred)
r2

dt.predict([[5,6]])
*/
```

## Output:
data.head():

![image](https://github.com/Naveensrinivasan07/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119475891/bf268109-2c11-4344-bd04-34dbc04ae63a)

data.info():

![image](https://github.com/Naveensrinivasan07/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119475891/aec7ab1b-a460-48d0-817d-79b8aecaf5f2)

isnull() and sum():

![image](https://github.com/Naveensrinivasan07/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119475891/98a398f7-16c5-44de-bd7a-a3c1589bb00d)

data.head() for salary:

![image](https://github.com/Naveensrinivasan07/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119475891/fd74a5ce-5d26-4d67-8a09-5ddac083b3b9)

MSE value:

![image](https://github.com/Naveensrinivasan07/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119475891/237f43c9-1073-4355-b7ba-0b0db25966fc)

r2 value:

![image](https://github.com/Naveensrinivasan07/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119475891/cc4a09c5-2f73-45c4-b237-7935dddb6409)

data prediction:

![image](https://github.com/Naveensrinivasan07/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119475891/d3612ae9-97a2-4ba9-9708-97aa30ce02c4)

## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.

