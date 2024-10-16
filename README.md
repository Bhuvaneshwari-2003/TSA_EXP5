# Ex.No: 05  IMPLEMENTATION OF TIME SERIES ANALYSIS AND DECOMPOSITION
### Date: 


### AIM:
To Illustrates how to perform time series analysis and decomposition on the monthly average temperature of a city/country and for airline passengers.

### ALGORITHM:
1. Import the required packages like pandas and numpy
2. Read the data using the pandas
3. Perform the decomposition process for the required data.
4. Plot the data according to need, either seasonal_decomposition or trend plot.
5. Display the overall results.

### PROGRAM:
```

!pip install pandas

import pandas as pd
import matplotlib.pyplot as plt
from statsmodels.tsa.seasonal import seasonal_decompose

# Load dataset (replace with your data)
data = pd.read_csv('/content/Temperature.csv')

# Convert 'date' column to datetime format and set as index
data['Month'] = pd.to_datetime(data['Month'])
data.set_index('Month', inplace=True)

# Specify the period for decomposition
period = 12  # Change this to the appropriate period for your data

# Perform decomposition
result = seasonal_decompose(data, model='multiplicative', period=period)

# Plot the decomposition
result.plot()
plt.show()
```



### OUTPUT:
FIRST FIVE ROWS:
 
![image](https://github.com/user-attachments/assets/827e53eb-d819-4b10-abbf-068fe2555288)



PLOTTING THE DATA:
![image](https://github.com/user-attachments/assets/54356834-0230-4e4d-b3c4-e60f913b8b47)

SEASONAL PLOT REPRESENTATION :
![image](https://github.com/user-attachments/assets/60b54555-216d-4e70-8a9e-7efd76d770df)



TREND PLOT REPRESENTATION :
![image](https://github.com/user-attachments/assets/790ce3c4-cf1e-4a30-9736-56f79b4159b6)

OVERAL REPRESENTATION:
![image](https://github.com/user-attachments/assets/b384ef3f-580b-4a13-99fe-1df737c85fad)



### RESULT:
Thus we have created the python code for the time series analysis and decomposition.
