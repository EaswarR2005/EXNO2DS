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

```


# RESULT
        <<INCLUDE YOUR RESULT HERE>>
