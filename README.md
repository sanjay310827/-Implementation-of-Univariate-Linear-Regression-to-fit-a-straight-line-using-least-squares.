# Implementation-of-Univariate-Linear-Regression-to-fit-a-straight-line-using-least-squares.
# AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

# Equipments Required:
 1. Hardware – PCs
 2. Anaconda – Python 3.7 Installation / Jupyter notebook
  
# Algorithm
 1. Get the independent variable X and dependent variable Y.
 2. Calculate the mean of the X -values and the mean of the Y -values.
 3. Find the slope m of the line of best fit using the formula:
  
   <img width="313" height="149" alt="image" src="https://github.com/user-attachments/assets/e8fe0aea-5fd0-42cb-90a1-3cd22acccace" />
   
   4. Compute the y -intercept of the line by using the formula:
      
   <img width="207" height="61" alt="image" src="https://github.com/user-attachments/assets/c8a46773-55a1-47b4-980e-a5883a88f763" />
   
   5. Use the slope m and the y -intercept to form the equation of the line. 6. Obtain the straight line equation Y=mX+b and plot the                scatterplot.
   6. Use the slope m and the y -intercept to form the equation of the line. 6. Obtain the straight line equation Y=mX+b and plot the              scatterplot.

# program
```python
import numpy as np
import matplotlib.pyplot as plt

x = np.array(eval(input()))
y = np.array(eval(input()))
```

<img width="307" height="43" alt="image" src="https://github.com/user-attachments/assets/6ceda505-25e6-428d-a62a-2d700c1e62a4" />


```python
x_mean = np.mean(x)
y_mean = np.mean(y)
num = 0 
denom = 0
for i in range(len(x)):
    num += (x[i] - x_mean) * (y[i] - y_mean)
    denom += (x[i] - x_mean) ** 2
m = num / denom    
b = y_mean - m * x_mean
print(m, b)
```

<img width="431" height="20" alt="image" src="https://github.com/user-attachments/assets/a34e4730-666c-43aa-b4d9-99434f938b13" />


```python
y_predicted = m * x + b
print(y_predicted)
<img width="773" height="80" alt="image" src="https://github.com/user-attachments/assets/63a43b90-a165-4cc8-af4e-0e4152fd586c" />
plt.scatter(x, y)
plt.plot(x, y_predicted, color='red')
plt.show()
```


<img width="781" height="587" alt="image" src="https://github.com/user-attachments/assets/0cd2f3ff-274e-49a7-ba6e-af0da1bf2fff" />








 
 
  



 
