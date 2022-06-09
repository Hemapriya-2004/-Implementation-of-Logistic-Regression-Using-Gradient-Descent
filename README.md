# Implementation-of-Logistic-Regression-Using-Gradient-Descent

## AIM:
To write a program to implement the the Logistic Regression Using Gradient Descent.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
## STEP 1:
Use the standard libraries in python for finding linear regression.

## STEP 2:
Set variables for assigning dataset values

## STEP 3:
Import linear regression from sklearn.

## STEP 4:
Predict the values of array

## STEP 5:
Calculate the accuracy, confusion and classification report by importing the required modules from sklearn.

## STEP 6:
Obtain the graph.
## Program:
```
/*
Program to implement the the Logistic Regression Using Gradient Descent.
Developed by: R Hemapriya
RegisterNumber: 212221230036

import numpy as np
import matplotlib.pyplot as plt
import pandas as pd
datasets=pd.read_csv('/content/Social_Network_Ads (1).csv')
x=datasets.iloc[:,[2,3]].values
y=datasets.iloc[:,4].values
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.25,random_state=0)
from sklearn.preprocessing import StandardScaler
sc_x=StandardScaler()
sc_x
StandardScaler()
x_train=sc_x.fit_transform(x_train)
x_Test=sc_x.transform(x_test)
from sklearn.linear_model import LogisticRegression
classifier=LogisticRegression(random_state=0)
classifier.fit(x_train,y_train)
y_pred=classifier.predict(x_test)
y_pred
from sklearn.metrics import confusion_matrix
cm = confusion_matrix(y_test,y_pred)
cm
from sklearn import metrics
accuracy =metrics.accuracy_score(y_test,y_pred)
accuracy
recall_sensitivity=metrics.recall_score(y_test,y_pred,pos_label=1)
recall_specificity=metrics.recall_score(y_test,y_pred,pos_label=0)
recall_sensitivity,recall_specificity
from matplotlib.colors import ListedColormap
x_Set,y_Set=x_train,y_train
x1,x2=np.meshgrid(np.arange(start=x_Set[:,0].min()-1,stop=x_Set[:,0].max()+1,step=0.01),np.arange(start=x_Set[:,1].min()-1,stop=x_Set[:,1].max()+1,step=0.01))
plt.contourf(x1,x2,classifier.predict(np.array([x1.ravel(),x2.ravel()]).T).reshape(x1.shape),alpha=0.75,cmap=ListedColormap(('red','green')))
plt.xlim(x1.min(),x2.max())
plt.ylim(x2.min(),x2.max())
for i,j in enumerate(np.unique(y_Set)):
  plt.scatter(x_Set[y_Set==j,0],x_Set[y_Set==j,1],c=ListedColormap(('red','green'))(i),label=j)
  plt.title('LogisticRegression(Trainingset)')
  plt.xlabel('Age')
  plt.ylabel('Estimated Salary')
  plt.legend()
  plt.show()

*/
```

## Output:
![output](https://github.com/Hemapriya-2004/-Implementation-of-Logistic-Regression-Using-Gradient-Descent/blob/50250231d14ba02b6907946d70c0e289f3060679/lr.PNG)


## Result:
Thus the program to implement the the Logistic Regression Using Gradient Descent is written and verified using python programming.

