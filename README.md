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
Developed by: AHALYA S
RegisterNumber: 212223230006
*/
```

```

import pandas as pd
data=pd.read_csv("Salary.csv")
data.head()

data.info

data.isnull().sum()

from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()

x=data[["Position","Level"]]
y=data[["Salary"]]

from sklearn.model_selection import train_test_split
x_train, x_test, y_train, y_test=train_test_split(x,y,test_size=0.2,random_state=2)

from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)

from sklearn import metrics
mse=metrics.mean_squared_error(y_test, y_pred)
mse

r2=metrics.r2_score(y_test,y_pred)
r2

dt.predict([[5,6]])
```

## OUTPUT:

# DATA HEAD:
![image](https://github.com/user-attachments/assets/9f8f40f4-1820-4e6f-b466-66cc348f6e10)

# DATA INFO:
![image](https://github.com/user-attachments/assets/89d6d491-f6fb-43ac-af48-2dcce0d1b804)

# ISNULL() AND SUM():
![image](https://github.com/user-attachments/assets/14f5e325-2173-4de5-9946-5eb6dce1e1b9)

# DATA HEAD FOR SALARY:
![image](https://github.com/user-attachments/assets/68c70b4e-ba90-4f6b-99f3-ad6a7575cfe4)

# MEAN SQUARED ERROR:
![image](https://github.com/user-attachments/assets/18e941c6-e5c5-47c8-823e-4b4b098a7ecc)

# R2 VALUE:
![image](https://github.com/user-attachments/assets/fad1beac-5fd7-4a72-a258-0ad1fe1e9975)

# DATA PREDICTION:
![image](https://github.com/user-attachments/assets/716baa61-c729-4a4c-8d21-85196472224b)



## RESULT
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
































```

## Output:
![Decision Tree Regressor Model for Predicting the Salary of the Employee](sam.png)


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
