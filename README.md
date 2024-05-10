# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
STEP 1 : Start
STEP 2 : Preprocessing the data
STEP 3 : Feature Extraction
STEP 4 : Training the SVM model
STEP 5 : Model Evalutaion
STEP 6 : Stop

## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: Vikamuhan.n
RegisterNumber:  212223240181
*/


import pandas as pd
data=pd.read_csv("C:/Users/Shoba/Downloads/spam.csv",encoding='Windows-1252')
from sklearn.model_selection import train_test_split
data
data.shape
x=data['v2'].values
y=data['v1'].values
y.shape
x.shape
x_train,x_test,y_train,y_test = train_test_split(x,y,test_size= 0.35,random_state = 0)
x_train
x_train.shape
from sklearn.feature_extraction.text import CountVectorizer
cv=CountVectorizer()
x_train=cv.fit_transform(x_train)
x_test=cv.transform(x_test)
from sklearn.svm import SVC
svc=SVC()
svc.fit(x_train,y_train)
from sklearn.svm import SVC
svc=SVC()
svc.fit(x_train,y_train)
y_pred=svc.predict(x_test)
y_pred
from sklearn.metrics import accuracy_score,confusion_matrix,classification_report
acc=accuracy_score(y_test,y_pred)
acc
con=confusion_matrix(y_test,y_pred)
con
c1=classification_report(y_test,y_pred)
c1

```

## Output:
### Using Count vectorizer and SVM ,Accuracy and Classification:

![WhatsApp Image 2024-05-10 at 16 32 49_05628607](https://github.com/vikamuhan-reddy/Implementation-of-SVM-For-Spam-Mail-Detection/assets/144928933/4639d0f1-52f9-4442-bff1-310b3cdfa5c4)

## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
