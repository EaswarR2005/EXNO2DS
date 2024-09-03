# EXNO2DS
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

## CODING AND OUTPUT:
```
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
df=pd.read_csv("/content/titanic_dataset.csv")
df
```
![image](https://github.com/user-attachments/assets/4991394c-5d9e-499e-ad37-aa83b269379f)

```
df.info()
```
![image](https://github.com/user-attachments/assets/2c69e058-85b5-4146-bb61-570a48649115)

```
df.shape
```
![image](https://github.com/user-attachments/assets/aeaa657f-1d20-4b44-9ccc-167817f98859)
```
df.nunique()
```

![image](https://github.com/user-attachments/assets/32d6170d-da8d-4239-adee-8b31a3587705)
```
df["Survived"].value_counts()
```

![image](https://github.com/user-attachments/assets/7e89bb1e-60ae-44d3-a52b-85e17de32d8f)
```
per=(df["Survived"].value_counts()/dt.shape[0]*100).round(2)
per
```

![image](https://github.com/user-attachments/assets/da947b19-65a5-477c-9b32-fbf79257e187)
```
df.describe()
```
![image](https://github.com/user-attachments/assets/7f0baafe-9faa-4971-a9f5-97ebdd06a33e)

```
sns.countplot(data=df,x="Survived")
```
![image](https://github.com/user-attachments/assets/1f03c123-1189-4979-b51e-eb2b1f671a19)

```
df.Pclass.unique()
```
![image](https://github.com/user-attachments/assets/21531458-eca3-4981-a4ee-411428ca8bae)

```
df.rename(columns = {'sex': 'Gender'},inplace = True)
df
```
![image](https://github.com/user-attachments/assets/3a15901a-0560-4954-8cbe-42571b01c1ef)

```
sns.catplot(x="Gender",col="Survived",kind="count",data=df,height=5,aspect=.7)
```
![image](https://github.com/user-attachments/assets/9a5264af-3d8d-49a3-b86d-10f5d640dc9f)
```
sns.catplot(x='Survived',hue="Gender",data=df,kind="count")
```
![image](https://github.com/user-attachments/assets/0d2943d4-18de-4fd7-ad42-fa93d85321a1)

```
df.boxplot(column="Age",by="Survived")
```
![image](https://github.com/user-attachments/assets/88864778-988a-4a7b-9b7b-e4d7b29dc60e)

```
sns.scatterplot(x=df["Age"],y=df["Fare"])
```
![image](https://github.com/user-attachments/assets/901bfcc3-b35f-483d-ba60-4a197d691a1f)

```
sns.jointplot(x="Age",y="Fare",data=df)
```
![image](https://github.com/user-attachments/assets/4a6cc90f-a12f-41b2-9551-08f3f944574b)

```
fig,ax1 = plt.subplots(figsize=(8,5))
pt = sns.boxplot(ax=ax1,x='Pclass',y='Age',hue='Gender',data=df)
```
![image](https://github.com/user-attachments/assets/9097d508-96c2-4e76-94f0-5f14285b8610)
```
sns.catplot(data=df,col="Survived",x="Gender",hue="Pclass",kind="count")
```
![image](https://github.com/user-attachments/assets/604554dc-9112-4545-b212-abf01aef7ddf)

```
import seaborn as sns
corr=df.corr()
sns.heatmap(corr,annot=True)
```
```
sns.pairplot(df)
```
![image](https://github.com/user-attachments/assets/4dd5dee9-f124-4b48-a70a-b3ff7a06cfb5)


# RESULT:
    Thus the data analysis has been implemented succesfully.
