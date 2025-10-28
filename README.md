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
Name:S Dhanush

Reg.no:25005353

```
import pandas as pd
 import seaborn as sns
 import matplotlib.pyplot as plt
 df=pd.read_csv("titanic_dataset.csv")
 df.head()
```
<img width="1460" height="259" alt="Screenshot 2025-10-28 155013" src="https://github.com/user-attachments/assets/d2908f17-37a7-4efc-ad74-ad6b1bf5d6a0" />

# 1.Line Plot
```
 x=[1,2,3,4,5]
 y=[3,6,2,7,1]
 sns.lineplot(x=x,y=y)
 plt.title('Line Plot')
```
<img width="785" height="569" alt="Screenshot 2025-10-28 155028" src="https://github.com/user-attachments/assets/7d815e9f-c581-4ef2-b8ae-e375d40e9347" />

# 2.Multi Line Plot
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
<img width="771" height="570" alt="Screenshot 2025-10-28 155041" src="https://github.com/user-attachments/assets/f79aa001-4b0f-43fa-bbcc-cec7d1601f3f" />

# To visualize relationships
# 1.Bar Chart
```
plt.figure(figsize=(8,5))
 sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
 plt.title("Fare Of Passenger By Embarked Town")
```
<img width="976" height="578" alt="Screenshot 2025-10-28 155054" src="https://github.com/user-attachments/assets/20465423-4753-4c39-b0a5-bb340f6287da" />

# 2.Scatter Plot
```
sns.scatterplot(x="Age", y="Fare", data=df)
 plt.title('Scatterplot of Age vs Fare')
 plt.show()
```
<img width="895" height="568" alt="Screenshot 2025-10-28 155106" src="https://github.com/user-attachments/assets/93027065-85f1-409f-a68e-2e7a94fef78b" />

# 3.Bubble Chart
```
 sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
 plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
 plt.show()
```
<img width="857" height="571" alt="Screenshot 2025-10-28 155120" src="https://github.com/user-attachments/assets/b1238a8e-1383-40cf-99be-c46f33bf57a0" />

# To capture distributions
# 1.Histogram
```
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
<img width="816" height="572" alt="Screenshot 2025-10-28 155134" src="https://github.com/user-attachments/assets/59b44e62-5417-4c87-b257-5e1116f17dae" />

# 2.Box plot
```
 sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
 plt.title("Age By Passenger Class")
```
<img width="899" height="555" alt="Screenshot 2025-10-28 155203" src="https://github.com/user-attachments/assets/a0306a54-af3f-4260-a6b4-7aa9c2a3bf67" />

# 3.Violin plot
```
sns.violinplot(x="Pclass", y="Fare", data=df)
 plt.title('Violin Plot of Fare by Passenger Class')
 plt.show()
```
<img width="847" height="567" alt="Screenshot 2025-10-28 155215" src="https://github.com/user-attachments/assets/1420771a-a3e9-4a7e-98e2-8947b0191587" />

# 4.Density plot
```
sns.kdeplot(data=df['Age'], shade=True)
 plt.title('Density Plot of Passenger Ages')
 plt.show()
```
<img width="839" height="561" alt="Screenshot 2025-10-28 155230" src="https://github.com/user-attachments/assets/dd0e5582-e891-4a64-81fc-54b7ed979bf0" />

# 5.Heatmap
```
numeric_df = df.select_dtypes(include=['float64', 'int64'])
 corr_matrix = numeric_df.corr()
 sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
 plt.title('Heatmap of Titanic Dataset')
 plt.show()
```
<img width="876" height="641" alt="Screenshot 2025-10-28 155248" src="https://github.com/user-attachments/assets/0126bfce-75c4-48b1-abb0-49721eaf0d57" />

# Result:
Thus,the data visualization using seaborn python library for the given data is implemented successfully.




