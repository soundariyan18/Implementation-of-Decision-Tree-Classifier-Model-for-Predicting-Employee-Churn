# EX:6 Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## Date: 12.10.23

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm

1. Prepare your data

2.Define your model

3.Define your cost function

4.Define your learning rate

5.Train your model

6.Evaluate your model

7.Tune hyperparameters

8.Deploy your model
 

## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

Developed by: soundariyan

RegisterNumber:  212222230146

import pandas as pd
data=pd.read_csv("Employee.csv")
data.head()

data.info()'

data.isnull().sum()

data["left"].value_counts()

from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()

data['salary']=le.fit_transform(data['salary'])
data.head()

x=data[["satisfaction_level","last_evaluation","number_project","average_montly_hours",	"time_spend_company",	"Work_accident",	"promotion_last_5years",	"salary"]]
x.head()

y=data["left"]

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test,=train_test_split(x,y,test_size=0.2,random_state=100)

from sklearn.tree import DecisionTreeClassifier
dt=DecisionTreeClassifier(criterion="entropy")
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)

from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy

dt.predict([[0.5,0.8,9,260,6,0,1,2]])
*/
```

## Output:

Initial data set:

![MODEL](https://github.com/soundariyan18/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/blob/main/Screenshot%202023-10-14%20160244.png)

Data info:

![MODEL](https://github.com/soundariyan18/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/blob/main/Screenshot%202023-10-14%20160351.png)

Optimization of null values:

![MODEL](https://github.com/soundariyan18/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/blob/main/Screenshot%202023-10-14%20160413.png)

Assignment of x and y values:

![MODEL](https://github.com/soundariyan18/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/blob/main/Screenshot%202023-10-14%20160428.png)


![MODEL](https://github.com/soundariyan18/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/blob/main/Screenshot%202023-10-14%20160444.png)

Converting string literals to numerical values using label encoder:

![MODEL](https://github.com/soundariyan18/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/blob/main/Screenshot%202023-10-14%20160458.png)

Accuracy:

![MODEL](https://github.com/soundariyan18/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/blob/main/Screenshot%202023-10-14%20160514.png)

Prediction:

![MODEL](https://github.com/soundariyan18/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/blob/main/Screenshot%202023-10-14%20160530.png)



## Result:

Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
