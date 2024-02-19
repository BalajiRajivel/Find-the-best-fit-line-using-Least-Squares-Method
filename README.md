# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula. 
<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">
4. Compute the y -intercept of the line by using the formula:
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">
5. Use the slope m and the y -intercept to form the equation of the line.
6. Obtain the straight line equation Y=mX+b and plot the scatterplot.

## Program:
```
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: BALAJI R
RegisterNumber:  212222040023
*/

# Preprocessing Input data

X=np.array(eval(input()))
Y=np.array(eval(input()))

# Mean
Xmean=np.mean(X)
Ymean=np.mean(Y)
num=0 #for slope
den=0 #for slope

#to find sum of (xi-x') & (yi-y') & (xi-x')^2
for i in range(len(X)):
  num+=(X[i]-Xmean)*(Y[i]-Ymean)
  den+=(X[i]-Xmean)**2

#calculate slope
m=num/den

#claculate intercept
b=Ymean-m*Xmean
print(m,b)
#Line equation
Y_pred=m*X+b
print(Y_pred)

#to plot grap
plt.scatter(X,Y)
plt.plot(X,Y_pred,color="red")
plt.show()

```

## Output:

3.6,4.8,7.2,6.9,10.7,6.1,7.9,9.5,5.4
9.3,10.12,11.5,12,18.6,13.2,10.8,22.7,12.7
1.5414525691699603 2.79953282828283
[ 8.34876208 10.19850516 13.89799133 13.43555556 19.29307532 12.2023935
 14.97700812 17.44333224 11.1233767 ]
![BALAJI](https://github.com/BalajiRajivel/Find-the-best-fit-line-using-Least-Squares-Method/assets/103949835/20cd2529-54c5-43ea-8f7d-97fb923bf771)


## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
