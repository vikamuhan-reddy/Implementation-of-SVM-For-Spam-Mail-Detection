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
data = pd.read_csv("C:/Users/marco/OneDrive/Desktop/study materials/spam.csv",encoding = 'Windows-1252')
data

data.head()
data.tail()
data.isnull().sum()

x = data['v1'].values
y = data['v2'].values
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test = train_test_split(x,y,test_size= 0.2,random_state = 0)
from sklearn.feature_extraction.text import CountVectorizer
cv = CountVectorizer()
x_train = cv.fit_transform(x_train)
x_test = cv.transform(x_test)
```

## Output:
### Using Count vectorizer and SVM:

![image](https://github.com/vikamuhan-reddy/Implementation-of-SVM-For-Spam-Mail-Detection/assets/144928933/c41b5258-7c8b-4aa9-a224-b359d2c1e660)

### Accuracy:

![image](https://github.com/vikamuhan-reddy/Implementation-of-SVM-For-Spam-Mail-Detection/assets/144928933/45afeffe-19b8-4539-8416-d51a62a9e75b)

## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
