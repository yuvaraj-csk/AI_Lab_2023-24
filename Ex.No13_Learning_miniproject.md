# Ex.No: 10 Learning – Use Supervised Learning  
### DATE:                                                                            
### REGISTER NUMBER : 
### AIM: 
To write a program to train the classifier for -----------------.
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

![image](https://github.com/yuvaraj-csk/AI_Lab_2023-24/assets/134052574/626476c1-9147-4e5f-b823-8fdc0ac9814e)

```

### Output:


### Result:
Thus the system was trained successfully and the prediction was carried out.
