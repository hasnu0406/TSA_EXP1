# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 11-03-25
### REG.NO:212223240052
# AIM:
To Develop a python program to Plot a time series data (population/ market price of a commodity
/temperature.
# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.
# PROGRAM:
```
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
data=pd.read_csv("Chocolate Sales.csv")
data.head()
data.tail()
data['Date'] = pd.to_datetime(data['Date'])
data.set_index('Date', inplace=True)
data
numeric_cols = ['Amount', 'Boxes Shipped']
categorical_cols = ['Sales Person', 'Country', 'Product']
for col in numeric_cols:
    plt.figure(figsize=(8, 4))
    sns.histplot(data[col], kde=True)
    plt.title(f'Distribution of {col}')
    plt.xlabel(col)
    plt.ylabel('Frequency')
    plt.tight_layout()
    plt.show()
for col in categorical_cols:
    plt.figure(figsize=(10, 4))
    sns.countplot(data=data, x=col, order=data[col].value_counts().index)
    plt.title(f'Count Plot of {col}')
    plt.xlabel(col)
    plt.ylabel('Count')
    plt.xticks(rotation=45)
    plt.tight_layout()
    plt.show()


```







# OUTPUT:
![image](https://github.com/user-attachments/assets/2f784b89-4135-406a-9d67-a237ebb130ab)
![image](https://github.com/user-attachments/assets/c4a0535e-cde1-4619-a99f-6977ec8ae5df)
![image](https://github.com/user-attachments/assets/fb9a5bf0-6f0c-4548-ba3e-fb070c8ec2e9)
![image](https://github.com/user-attachments/assets/4c8ebea3-0ce2-4222-a35f-d192d20dad44)
![image](https://github.com/user-attachments/assets/67f5938b-0105-48e1-873f-120bc014b86e)
![image](https://github.com/user-attachments/assets/6dfcd2c9-df66-49e4-9c76-6b3751be97dd)
![image](https://github.com/user-attachments/assets/fc0c56d9-9dec-4e33-955c-2d746a3bc3e4)
![image](https://github.com/user-attachments/assets/8e54a5ce-ed21-4978-ad6b-81767c1c2d5d)







# RESULT:
Thus we have created the python code for plotting the time series of given data.
