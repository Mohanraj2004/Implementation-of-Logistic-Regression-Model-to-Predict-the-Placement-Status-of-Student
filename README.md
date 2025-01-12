# Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student

## AIM:
To write a program to implement the the Logistic Regression Model to Predict the Placement Status of Student.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the standard libraries.
2. Upload the dataset and check for any null or duplicated values using .isnull() and .duplicated() function respectively.
3. Import LabelEncoder and encode the dataset.
4. Import LogisticRegression from sklearn and apply the model on the dataset.
5. Predict the values of array.
6. Calculate the accuracy, confusion and classification report by importing the required modules from sklearn.
7. Apply new unknown values

## Program:
```
/*
Program to implement the the Logistic Regression Model to Predict the Placement Status of Student.
Developed by: MOHAN RAJ S
RegisterNumber: 212221230065

import pandas as pd
data = pd.read_csv('Placement_Data.csv')
data.head()

data1= data.copy()
data1 = data1.drop(["sl_no","salary"],axis=1)
data1.head()

data1.isnull().sum()

data1.duplicated().sum()

from sklearn.preprocessing import LabelEncoder
le = LabelEncoder()
data1["gender"] = le.fit_transform(data1["gender"])
data1["ssc_b"] = le.fit_transform(data1["ssc_b"])
data1["hsc_b"] = le.fit_transform(data1["hsc_b"])
data1["hsc_s"] = le.fit_transform(data1["hsc_s"])
data1["degree_t"] = le.fit_transform(data1["degree_t"])
data1["workex"] = le.fit_transform(data1["workex"])
data1["specialisation"] = le.fit_transform(data1["specialisation"])
data1["status"] = le.fit_transform(data1["status"])
data1

x=data1.iloc[:,:-1]
x

y=data1["status"]
y

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test = train_test_split(x,y,test_size=0.2,random_state=0)

from sklearn.linear_model import LogisticRegression
lr = LogisticRegression(solver="liblinear")
lr.fit(x_train,y_train)
y_pred = lr.predict(x_test)
y_pred

from sklearn.metrics import accuracy_score 
accuracy = accuracy_score(y_test,y_pred) 
accuracy 

from sklearn.metrics import confusion_matrix 
confusion = confusion_matrix(y_test,y_pred) 
confusion

from sklearn.metrics import classification_report 
classification_report1 = classification_report(y_test,y_pred) 
print(classification_report1)

lr.predict([[1,80,1,90,1,1,90,1,0,85,1,85]])

*/
```

## Output:

### 1.Placement data 
![ex4](https://user-images.githubusercontent.com/119390329/235430538-8fb3b534-dcf0-4aed-a3c3-64788743e597.png)

### 2.Salary data
![ex41](https://user-images.githubusercontent.com/119390329/236657368-47f1c662-187a-4d0b-838c-f12b10fec979.png)

### 3.Checking the null() function
![ex42](https://user-images.githubusercontent.com/119390329/236657390-79bf5814-5ccb-402c-984d-2c78e6498b1c.png)

### 4.Data Duplicate
![ex42(1](https://user-images.githubusercontent.com/119390329/236657402-df27f33b-8406-41b9-8d5a-515aceada451.png)

### 5.Print data
![ex43](https://user-images.githubusercontent.com/119390329/236657441-bcff15bc-336f-4f20-8456-53e4c6685b48.png)

### 6.Data-status
![exp4](https://user-images.githubusercontent.com/119390329/236657555-13e6583b-a44d-4ff5-86a3-d96197b28f41.jpg)
![ex44](https://user-images.githubusercontent.com/119390329/236657563-f0a93c69-3749-422b-baaf-bfeba423b809.png)

### 7.y_prediction array
![e4](https://user-images.githubusercontent.com/119390329/236657624-35463ac6-3bd7-4126-a50b-fbbfe14b2f5c.jpg)

### 8.Accuracy value
![x4](https://user-images.githubusercontent.com/119390329/236657632-bdb36a4d-ea31-4a31-af04-684b99803a24.jpg)

### 9.Confusion array
![p4](https://user-images.githubusercontent.com/119390329/236660391-d2f41df9-78ac-4337-a8ec-ff5ad8cb9a05.jpg)

### 10.Classification report
![pp4](https://user-images.githubusercontent.com/119390329/236660439-1c73a739-a015-4716-b95b-b03bf39b73f6.jpg)

### 11.Prediction of LR
![xx4](https://user-images.githubusercontent.com/119390329/236660482-64427857-0cf0-448b-9eb7-57aab5816a8b.jpg)

## Result:
Thus the program to implement the the Logistic Regression Model to Predict the Placement Status of Student is written and verified using python programming.
