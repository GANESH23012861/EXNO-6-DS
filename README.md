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
```python
import pandas as pd
df=pd.read_csv("/content/titanic_dataset.csv")
df.head()
import seaborn as sns
import matplotlib.pyplot as plt
```
![327065662-47a2e1f8-e225-45cb-a7c9-5845074d3aad](https://github.com/GANESH23012861/EXNO-6-DS/assets/147139861/81f3032b-0e46-4aa8-bd6c-7dda82c58aa7)

### 1.Line Plot
```python
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```
![327065703-f4661ac2-18df-48dc-a7ca-7a114a814982](https://github.com/GANESH23012861/EXNO-6-DS/assets/147139861/30634b6c-0ed0-4556-bc18-25bb36958206)

### 2.Multiline Plot
```python
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi Line Plot')
```
![327065749-db486ae1-6a73-42ce-91ca-6735e21385e2](https://github.com/GANESH23012861/EXNO-6-DS/assets/147139861/31eb712e-5aea-4abe-881e-303323bbada9)

## To Visualize Relationships
### 1.Bar Chart
```python
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```
![327065820-2c03d7a2-8ff7-439d-a4fc-96b9f13b37e9](https://github.com/GANESH23012861/EXNO-6-DS/assets/147139861/b2748bed-145e-4960-b680-73b05064a42b)

### 2.Scatter Plot
```python
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```
![327065846-053d3744-0f30-4bb2-81cf-b4e6df636fd7](https://github.com/GANESH23012861/EXNO-6-DS/assets/147139861/124c948c-40c6-4102-8daf-075abbc8d355)


### 3.Bubble Chart
```python
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```
![327065859-b99f15e3-035f-4aaa-896a-9def7b615466](https://github.com/GANESH23012861/EXNO-6-DS/assets/147139861/2a74af56-9b77-4170-83b5-9163737d9c13)

## To Capture Distributions
### 1.Histogram
```python
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
![327065889-ede434fc-8f91-49d3-bc11-0a52f8e02bde](https://github.com/GANESH23012861/EXNO-6-DS/assets/147139861/72c3c70a-15ab-4082-879e-8cbae7d3d9b9)

### 2.Box Plot
```python
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```
![327065915-edb99c5d-6ff1-41ad-8b6b-5da4534b2e02](https://github.com/GANESH23012861/EXNO-6-DS/assets/147139861/6b377b4e-f693-4a8d-8597-73948e8f008e)

### 3.Violin Plot
``` python
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```
![327066031-c929293c-f666-4c12-a55a-ea9ea52015bc](https://github.com/GANESH23012861/EXNO-6-DS/assets/147139861/cc1eeb1a-08d2-4b6e-81d8-5a595064b7da)

### 4.Density Plot
``` python
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```
![327066050-31881338-ee40-462c-bf3c-bac603598c9a](https://github.com/GANESH23012861/EXNO-6-DS/assets/147139861/d80f9859-b882-4bf2-9945-2b45b06028a5)

### 5.Heatmap
``` python
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```
![327066078-9636642e-b953-43ec-afc8-fc58883c158b](https://github.com/GANESH23012861/EXNO-6-DS/assets/147139861/be8ba8f8-2178-4371-932e-e8e42a49681d)

# Result:
Thus, the Data Visualization using seaborn python library for the given data is implemented successfull
