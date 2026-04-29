# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 29/04/2026

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
df = pd.read_excel("/content/Google_Stock_Price_Test.csv.xlsx")
df["Date"] = pd.to_datetime(df["Date"])
df.set_index("Date", inplace=True)
df = df.sort_index()
plt.figure(figsize=(12, 6)
plt.plot(df.index, df["Volume"], linewidth=2, label="Volume")
plt.title("Google Stock Volume Over Time")
plt.xlabel("Date")
plt.ylabel("Volume")
plt.grid(True)
plt.legend()
plt.xticks(rotation=45)  
plt.tight_layout()
plt.show()
```

# OUTPUT:

<img width="1113" height="552" alt="image" src="https://github.com/user-attachments/assets/4216fa24-a149-4d07-8189-9b5d58253b94" />

# RESULT:
Thus we have created the python code for plotting the time series of given data.
