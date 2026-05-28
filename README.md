# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

# Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
 
```py
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
df=pd.read_csv("titanic_dataset.csv")
df.head()
```

![image](https://github.com/aadithyan22000618/EXNO-6-DS/assets/113586376/79f4819c-dfc3-4906-84c0-9e03ce115c32)



### 1.Line Plot
```py
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```
![image](https://github.com/aadithyan22000618/EXNO-6-DS/assets/113586376/68a63045-f6dc-4229-bc53-e4e4e71b14f5)


### 2.Multi Line Plot
```py
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi Line Plot')
```

![image](https://github.com/aadithyan22000618/EXNO-6-DS/assets/113586376/aae1a706-a5b2-41ed-bd91-3bfde2f18fae)


## TO VISUALIZE RELATIONSHIPS
### 1.Bar Chart
```py
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```
![image](https://github.com/aadithyan22000618/EXNO-6-DS/assets/113586376/5b1aa904-42d7-47dc-8ad2-9803d35a864f)


### 2.Scatter Plot
```py
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```
![image](https://github.com/aadithyan22000618/EXNO-6-DS/assets/113586376/c7ad7761-a406-4582-931f-ad1515696c58)

### 3.Bubble Chart
```py
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```
![image](https://github.com/aadithyan22000618/EXNO-6-DS/assets/113586376/a99cc2f3-7b66-408e-89f4-948bf9b80dda)


## TO CAPTURE DISTRIBUTIONS
### 1.Histogram
```py
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
![image](https://github.com/aadithyan22000618/EXNO-6-DS/assets/113586376/a5f69477-e68b-4892-b3cd-965610b7faef)


### 2.Box Plot
```py
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```
![image](https://github.com/aadithyan22000618/EXNO-6-DS/assets/113586376/0caa044f-a411-49e8-b05e-66cf67c49383)


### 3.Violin Plot
```py
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```
![image](https://github.com/aadithyan22000618/EXNO-6-DS/assets/113586376/b725d969-8c14-4cfc-9ef8-80035a388b93)


### 4.Density Plot
```py
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```
![image](https://github.com/aadithyan22000618/EXNO-6-DS/assets/113586376/2da67e4d-d184-4c90-8859-cca668c52057)


### 5.Heatmap
```py
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```
![image](https://github.com/aadithyan22000618/EXNO-6-DS/assets/113586376/5cc6be20-4ef3-4db4-86fd-5eb9f9299a0d)



## Result:
Thus, the Data Visualization using seaborn python library for the given data is implemented successfully
