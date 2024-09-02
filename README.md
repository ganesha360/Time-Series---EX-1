### Developed by : GANESH R
### Reg No : 212222240029
### Date :

# Ex.No: 01 PLOT A TIME SERIES DATA
# AIM:
To Develop a python program to Plot a time series data of Amazon stock price.
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

# Load the data from the CSV file
file_path = '/content/Amazon.csv'
data = pd.read_csv(file_path)

# Display the first few rows of the dataset to understand its structure
print(data.head())

# Convert the 'Date' column to datetime format
data['Date'] = pd.to_datetime(data['Date'])

# Set the 'Date' column as the index
data.set_index('Date', inplace=True)

# Plot the time series data for 'Open' stock prices
plt.figure(figsize=(10, 6))
plt.plot(data.index, data['Open'], label='Open Price')
plt.title('Netflix stock price(Open)')
plt.xlabel('Date')
plt.ylabel('Price')
plt.grid(True)
plt.legend()
plt.show()
```
# OUTPUT:

![image](https://github.com/user-attachments/assets/f5c5dd0d-d6d3-45f4-b4eb-36f4163203bd)

# RESULT:
Thus we have created the python code for plotting the time series of Amazon stock data.
