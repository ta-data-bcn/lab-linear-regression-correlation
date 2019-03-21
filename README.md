![Ironhack logo](https://i.imgur.com/1QgrNNw.png)

# Lab | Linear regression and correlation
This lab will be done in a Zeppelin notebook. You can deliver yout json through a PR.

## Challenge 1
I am suspicious about my employees. I think the younger they are, the more they don't come to work. In order to prove my hypothesis, I get some data:

| EmployeeID | Age | Absences |
|--------|-----|------------|
| 1      | 27  | 15         |
| 2      | 61  | 6          |
| 3      | 37  | 10         |
| 4      | 23  | 18         |
| 5      | 46  |  9         |
| 6      | 58  |  7         |
| 7      | 29  | 14         |
| 8      | 36  | 11         |
| 9      | 64  |  5         |
| 10     | 40  |  8         |

Connect to Ironhack's database. Retrieve this data from the "absences" table in the "employees" database. 

* Draw the dispersion diagram. What do you see here?
* Define a function to calculate the parameters of the regression line. No methods allowed!
* Calculate the regression line and do some comments.
* Define a function to calculate the covariance and the correlation (you can use the methods you defined for the standard deviation)
* Calculate the covariance and the correlation. Compare them.
* Interprete the results and give some conclusions. Can I say that the age is an indicator of absentisme?

## Challenge 2

I am suspicious about my last parties. It looks like the more people I invite, the more people can't come, so I have decided to do an analysis. 

X is the number of people that I invited to one party and Y is the number of people that actually came.

| X | Y |
|---|---|
| 1 | 1 |
| 3 | 2 |
| 4 | 4 |
| 6 | 4 |
| 8 | 5 |
| 9 | 7 |
| 11 |8 |
| 14 | 9 |

Use this command to create a dataframe with the data about my parties. 
~~~~
party_data = pd.DataFrame({'X': [1,3,4,6,8,9,11,14], 'Y': [1,2,4,4,5,7,8,9]})
~~~~

* Calculate the covariance and the correlation. What do you think?
* Draw the dispersion diagram. Any comments?
* Calculate the regression line. What do you think?
* Can you give some conclusions?

## Bonus challenge: Errors analysis

We are doing an analysis in order to see if two RVs fit into a linear regression or not. So we will be able to reach the following conclusions:
* The regression is / is not linear
* The linear regression model fits all the observations except a certain number of points.

We define an error as the difference between the expected value of an observation (the value that the regression line gives to us) and the actual value. 

Continuing with the Challenge 2, you are asked here to do an error analysis.
* First do a table with the expected Y value for each X

| x | y | expected y |
|---|---|---|
| 1 | 1 ||
| 3 | 2 ||
| 4 | 4 ||
| 6 | 4 ||
| 8 | 5 ||
| 9 | 7 ||
| 11 |8 ||
| 14 | 9 ||

You get the expected Y just evaluating the regression line for each X.

* Draw the dispersion diagram. You will drax X vs expected Y.
* The more the points are close to zero, the best the points will fit to the linear regression. What do you see here? Which points are painful?
* Recalculate the regression line removing the painful point. 
* Calculate the correlation. What is happening? What do you think?
