# Ex.No: 10 Learning – Use Supervised Learning  
### DATE:                                                                             
### REGISTER NUMBER : 212221040187
### AIM: 
To write a program to train the classifier for heart disease.
###  Algorithm:

### Program:
```
import numpy as np
import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LogisticRegression
from sklearn.metrics import accuracy_score
```

```
# loading the csv data to a Pandas DataFrame
heart_data = pd.read_csv('/content/data.csv')

# print first 5 rows of the dataset
heart_data.head()
```
![image](https://github.com/yuvaraj-csk/AI_Lab_2023-24/assets/134052574/626476c1-9147-4e5f-b823-8fdc0ac9814e)

### heart_data.info()
```
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 303 entries, 0 to 302
Data columns (total 14 columns):
 #   Column    Non-Null Count  Dtype  
---  ------    --------------  -----  
 0   age       303 non-null    int64  
 1   sex       303 non-null    int64  
 2   cp        303 non-null    int64  
 3   trestbps  303 non-null    int64  
 4   chol      303 non-null    int64  
 5   fbs       303 non-null    int64  
 6   restecg   303 non-null    int64  
 7   thalach   303 non-null    int64  
 8   exang     303 non-null    int64  
 9   oldpeak   303 non-null    float64
 10  slope     303 non-null    int64  
 11  ca        303 non-null    int64  
 12  thal      303 non-null    int64  
 13  target    303 non-null    int64  
dtypes: float64(1), int64(13)
memory usage: 33.3 KB
```
### heart_data.describe()
![image](https://github.com/yuvaraj-csk/AI_Lab_2023-24/assets/134052574/f5d44b94-f9d0-4be8-a244-38601f53ce1a)

### Splitting the Features and Target
```
X = heart_data.drop(columns='target', axis=1)
Y = heart_data['target']
print(X)
print(Y)
```
![image](https://github.com/yuvaraj-csk/AI_Lab_2023-24/assets/134052574/b39778e7-35c6-466e-ad86-8b3ebbf3ab66)
### Model Evaluation and Accuracy Score
```
# accuracy on training data
X_train_prediction = model.predict(X_train)
training_data_accuracy = accuracy_score(X_train_prediction, Y_train)

print('Accuracy on Training data : ', training_data_accuracy)
Accuracy on Training data :  0.8512396694214877
```
### Building a Predictive System
```
input_data = (62,0,0,140,268,0,0,160,0,3.6,0,2,2)

# change the input data to a numpy array
input_data_as_numpy_array= np.asarray(input_data)

# reshape the numpy array as we are predicting for only on instance
input_data_reshaped = input_data_as_numpy_array.reshape(1,-1)

prediction = model.predict(input_data_reshaped)
print(prediction)

if (prediction[0]== 0):
  print('The Person does not have a Heart Disease')
else:
  print('The Person has Heart Disease')
```


### Output:
```


if (prediction[0]== 0):
  print('The Person does not have a Heart Disease')
else:
  print('The Person has Heart Disease')

[0]
The Person does not have a Heart Disease
```

### Result:
Thus the system was trained successfully and the prediction was carried out.
