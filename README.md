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
```
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
df=pd.read_csv("titanic_dataset.csv")
df.head()
```
![op](https://github.com/user-attachments/assets/a36befd3-0bbf-4da7-bd73-8f7df84273e7)
## 1.Line Plot
```
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```
![op 1](https://github.com/user-attachments/assets/3147d767-eaeb-4015-aeb2-f38961870384)
## 2.Multi Line Plot
```
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi Line Plot')
```
![op 2](https://github.com/user-attachments/assets/1e657588-f7ac-415f-840f-509639591b84)
# TO VISUALISE RELATIONSHIPS
## 1.Bar Chart
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```
![op 3](https://github.com/user-attachments/assets/53b1e2f4-5871-469b-bae1-7d1082238653)
## 2.Scatter Plot
```
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```
![op 4](https://github.com/user-attachments/assets/159fb940-8709-4d77-bc1b-ef34cbfa5372)
## 3.Bubble Chart
```
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```
![op 5](https://github.com/user-attachments/assets/137f684c-2d1e-41ea-90d5-ce41e05eeaed)
# TO CAPTURE DISTRIBUTIONS
## 1.Histogram
```
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
![op 6](https://github.com/user-attachments/assets/46ea7fbc-6a28-42ef-9536-cee2fb52968d)

## 2.Box Plot
```
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```
![op 7](https://github.com/user-attachments/assets/ea485351-2dee-46a8-bf6d-953a0b147f0f)

## 3.Violin Plot
```
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```
![op 8](https://github.com/user-attachments/assets/6e645314-7a14-4ad9-b1aa-349434b4cb5d)

## 4.Density Plot
```
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```
![op 9](https://github.com/user-attachments/assets/22761fcf-5b5f-4aac-8ebd-dd6cd861e106)

## 5.Heatmap
```
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```
![op 10](https://github.com/user-attachments/assets/cb0b1727-0898-4dee-85d2-4eb381d12a59)

# Result:
Thus, the Data Visualization using seaborn python library for the given data is implemented successfully
