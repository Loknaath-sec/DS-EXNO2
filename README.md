# EXPNO2-Exploratory Data Analysis
# AIM:
To perform Exploratory Data Analysis on the given data set.
      
# EXPLANATION:
The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis.

  
# ALGORITHM:
STEP 1: Import the required packages to perform Data Cleansing,Removing Outliers and Exploratory Data Analysis.

STEP 2: Replace the null value using any one of the method from mode,median and mean based on the dataset available.

STEP 3: Use boxplot method to analyze the outliers of the given dataset.

STEP 4: Remove the outliers using Inter Quantile Range method.

STEP 5: Use Countplot method to analyze in a graphical method for categorical data.

STEP 6: Use displot method to represent the univariate distribution of data.

STEP 7: Use cross tabulation method to quantitatively analyze the relationship between multiple variables.

STEP 8: Use heatmap method of representation to show relationships between two variables, one plotted on each axis.

## CODING AND OUTPUT
```
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
df=pd.read_csv("titanic_dataset.csv")
df
```
![image](https://github.com/user-attachments/assets/f9931b1d-d430-4358-b9cb-61173d4b22b2)

```
df.info()
```
![image](https://github.com/user-attachments/assets/15da0e7d-59d7-4ec7-a50f-9fbd26e1702b)

```
df.shape
```
![image](https://github.com/user-attachments/assets/e6bf28a4-436e-4d43-ba9c-8f9e449bb908)

```
df.set_index("PassengerId",inplace=True)
df.describe()
```
![image](https://github.com/user-attachments/assets/4c55d5f1-6b39-421c-aec3-ca9f916fdc84)

```
df.shape
```
![image](https://github.com/user-attachments/assets/00ab997e-0c91-4217-a472-6a9b4e3e1c0d)

```
df.nunique()
```
![image](https://github.com/user-attachments/assets/276c4a5a-2c99-4ac7-a009-dd736ce89dc6)

```
df["Survived"].value_counts()
```


# RESULT
We have performed Exploratory Data Analysis on the given data set successfully.
