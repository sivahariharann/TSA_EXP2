# Ex.No: 02 LINEAR AND POLYNOMIAL TREND ESTIMATION
Date:19-02-2026
### AIM:
To Implement Linear and Polynomial Trend Estiamtion Using Python.

### ALGORITHM:
Import necessary libraries (NumPy, Matplotlib)

Load the dataset

Calculate the linear trend values using least square method

Calculate the polynomial trend values using least square method

End the program
### PROGRAM:
 LINEAR TREND ESTIMATION & POLYNOMIAL TREND ESTIMATION
  ```
import numpy as np
import matplotlib.pyplot as plt
import pandas as pd
data = pd.read_csv('BMW_Data.csv')

data['Date'] = pd.to_datetime(data['Date'])
data = data.sort_values('Date')

x = np.arange(len(data))   # numeric values for least squares
y = data['Volume'].values
linear_coeff = np.polyfit(x, y, 1)
linear_trend = np.polyval(linear_coeff, x)
poly_coeff = np.polyfit(x, y, 2)
poly_trend = np.polyval(poly_coeff, x)
plt.figure()
plt.plot(data['Date'], y)
plt.plot(data['Date'], linear_trend)
plt.plot(data['Date'], poly_trend)
plt.xlabel('Date')
plt.ylabel('Volume')
plt.title('Linear and Polynomial Trend using Least Squares Method')
plt.show()
```

### OUTPUT
 LINEAR TREND ESTIMATION & POLYNOMIAL TREND ESTIMATION
<img width="567" height="470" alt="TSA ex2" src="https://github.com/user-attachments/assets/9c8c8102-eea4-49eb-85a6-140e75c32c87" />


### RESULT:
Thus the python program for linear and Polynomial Trend Estiamtion has been executed successfully.
