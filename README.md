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
Developed By: LOKNAATH P
Register No: 212223240080
```
```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
df=pd.read_csv("titanic_dataset.csv")
df
```
![image](https://github.com/user-attachments/assets/f9931b1d-d430-4358-b9cb-61173d4b22b2)

```python
df.info()
```
![image](https://github.com/user-attachments/assets/15da0e7d-59d7-4ec7-a50f-9fbd26e1702b)

```python
df.shape
```
![image](https://github.com/user-attachments/assets/e6bf28a4-436e-4d43-ba9c-8f9e449bb908)

```python
df.set_index("PassengerId",inplace=True)
df.describe()
```
![image](https://github.com/user-attachments/assets/4c55d5f1-6b39-421c-aec3-ca9f916fdc84)

```python
df.shape
```
![image](https://github.com/user-attachments/assets/00ab997e-0c91-4217-a472-6a9b4e3e1c0d)

```python
df.nunique()
```
![image](https://github.com/user-attachments/assets/276c4a5a-2c99-4ac7-a009-dd736ce89dc6)

```python
df["Survived"].value_counts()
```
![image](https://github.com/user-attachments/assets/9c550a37-2616-4a2e-b63c-69fb478d3e2d)

```python
per=(df["Survived"].value_counts()/df.shape[0]*100).round(2)
per
```
![image](https://github.com/user-attachments/assets/3bce9d20-c43b-4d6e-bedc-75382f206f8c)

```python
sns.countplot(data=df,x="Survived")
```
![image](https://github.com/user-attachments/assets/3854929e-7776-4a9b-83e6-53bbe83116eb)

```python
df
```
![image](https://github.com/user-attachments/assets/6249bf5c-aae2-4623-8af2-c139df1c2b8f)

```python
df.Pclass.unique()
```
![image](https://github.com/user-attachments/assets/9c0930c0-9901-409c-9763-d1354e8b98de)


```python
df.rename(columns={'Sex':'Gender'},inplace=True)
df
```
![image](https://github.com/user-attachments/assets/51fc7a32-d273-4d85-af44-ee8c75385688)

```python
sns.catplot(x="Gender",col="Survived",kind="count",data=df,height=5,aspect=.7)
```
![image](https://github.com/user-attachments/assets/25929578-2993-4930-a3e1-2201c7ad6094)

```python
sns.catplot(x="Survived",hue="Gender",data=df,kind="count")
```
![image](https://github.com/user-attachments/assets/33e1989f-a42b-45b5-b6ec-820f48eb8739)

```python
df.boxplot(column="Age",by="Survived")
```
![image](https://github.com/user-attachments/assets/dd050b40-3842-4e12-90b8-4977731633e1)

```python
sns.scatterplot(x=df["Age"],y=df["Fare"])
```
![image](https://github.com/user-attachments/assets/2c742afc-c43e-4f92-9a69-4a77a7770f9c)

```python
sns.jointplot(x="Age",y="Fare",data=df)
```
![image](https://github.com/user-attachments/assets/e447de54-7b40-4bab-a647-c3dac30bf510)

```python
fig, ax1 = plt.subplots(figsize=(8,5))
plt = sns.boxplot(ax=ax1,x='Pclass',y='Age',hue='Gender',data=df)
```
![image](https://github.com/user-attachments/assets/bf2dc696-e091-4c99-9d95-b9d5941f7ef7)

```python
sns.catplot(data=df,col="Survived",x="Gender",hue="Pclass",kind="count")
```
![image](https://github.com/user-attachments/assets/7fdbf60e-3fea-4ee9-baca-dc490731141d)

```python
corr = df.select_dtypes(include=['number']).corr()
sns.heatmap(corr,annot=True)
```
![image](https://github.com/user-attachments/assets/03bd05fc-dc49-45c3-997b-e93ed6266561)

```python
sns.pairplot(df)
```
![image](https://github.com/user-attachments/assets/519e0372-d722-46b5-b2e5-3432090015ee)
![image](https://github.com/user-attachments/assets/d9632232-044e-45b6-967d-d56e84c68f44)




# RESULT
We have performed Exploratory Data Analysis on the given data set successfully.
