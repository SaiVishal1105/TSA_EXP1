# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 

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
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

df=pd.read_csv("/content/car_price_prediction.csv")
df.head()

df['Engine volume'] = df['Engine volume'].str.replace(' Turbo', '', regex=False).astype(float)

# Sort by production year for a proper trend line
df_sorted = df.sort_values(by='Prod. year')

# Plot
plt.figure(figsize=(8,5))
sns.lineplot(data=df_sorted, x='Prod. year', y='Engine volume')
plt.title("Trend Pattern: Engine Volume over Production Year")
plt.xlabel("Production Year")
plt.ylabel("Engine Volume (L)")
plt.show()

```

# OUTPUT:
<img width="1787" height="391" alt="image" src="https://github.com/user-attachments/assets/2d85d47d-d44e-4a56-b9f6-7dce20bf07d1" />
<img width="954" height="607" alt="image" src="https://github.com/user-attachments/assets/389bc22d-b9e8-40ee-85f0-78599114c1b1" />






# RESULT:
Thus we have created the python code for plotting the time series of given data.
