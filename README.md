# Ex.No: 01 PLOT A TIME SERIES DATA
###  Date: 22/08/2024

# AIM:
To Develop a python program to Plot a time series data (Electric_Production).
# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.
# PROGRAM:
```py
import pandas as pd
import matplotlib.pyplot as plt

file_path = '/content/survey lung cancer.csv'
data = pd.read_csv(file_path)

print(data.head())
print(data.columns)

plt.figure(figsize=(12, 6))
plt.plot(data.index, data['AGE'], label='AGE', color='blue')  # Adjust 'Open' to your actual column name
plt.title('Survey Lung Cancer - Lung Cancer Over Time')
plt.xlabel('NUMBER OF PATIENTS')
plt.ylabel('AGE OF PATIENTS')
plt.legend()
plt.grid(True)
plt.show()
```
# OUTPUT:
![image](https://github.com/user-attachments/assets/273bb79f-fba6-4d35-bc7a-20b177937af5)
![image](https://github.com/user-attachments/assets/23907f62-dc62-48fb-8df9-5e830a575b3c)

# RESULT:
Thus we have created the python code for plotting the time series of given data.
