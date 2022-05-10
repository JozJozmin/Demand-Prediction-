# Demand-Prediction
Developing a machine learning approach in order to forecast the demand for car rentals on an hourly basis.

## Problem Statement
ABC is a car rental company based out of Bangalore. It rents cars for both in and out stations at affordable prices. The users can rent different types of cars like Sedans, Hatchbacks, SUVs and MUVs, Minivans and so on.

In recent times, the demand for cars is on the rise. As a result, the company would like to tackle the problem of supply and demand. The ultimate goal of the company is to strike the balance between the supply and demand inorder to meet the user expectations. 

The company has collected the details of each rental. Based on the past data, the company would like to forecast the demand of car rentals on an hourly basis. 

## Objective
The main objective of the problem is to develop the machine learning approach to forecast the demand of car rentals on an hourly basis.

## Evaluation metric
RMSE score
# Approach
## Data analysis and interpretation:
### About the Data provided : 
The train dataset contains the Date, hour and demand column and the test data includes both the date and the demand column. Apart from that the dataset doesn’t contains any null values count. 
### Feature Engineering:
In order to improve the quality of results from ML, I am extracting more features like year, month, day, dayofyear, weekofyear, day_no_week	and quarter from the date columns. And also applying univariate analysis on each feature with distribution of demand. 
Following are the results obtained:

![image](https://user-images.githubusercontent.com/87713648/167316213-f7269ff2-5500-413d-88ac-25ad8f1f5002.png)
![image](https://user-images.githubusercontent.com/87713648/167316230-dc426eec-204f-461b-93c6-29939e2084e5.png)
![image](https://user-images.githubusercontent.com/87713648/167316240-e050dcc6-33b3-4170-b81b-2ec92742b82e.png)
![image](https://user-images.githubusercontent.com/87713648/167316288-614da056-b577-4db3-ae20-68d2264d1d83.png)
![image](https://user-images.githubusercontent.com/87713648/167316319-0bb39980-ce57-4494-8a78-6713de01c85c.png)

<br />•	The average demand of cars high in between 12 pm to 5 pm and showing very less compared to other time in early morning in between 5 am and 6 am.
<br />•	The average demand of cars is showing peak in November followed by June and in each year.
<br />•	The end day of the month and the beginning days of a month are showing higher average demand for the cars. This may be due to towards 
<br />the end of the month; dealers will be looking to fill up their monthly quotas of sales and will be eager to make you a sale, and thus will likely offer a good price for the new car which increases the car demand on these days.
<br />•	The fourth quarter is showing higher demand of cars compared to other quarters due to in end quarter; the showrooms are often flooded with outgoing models of cars and have received a variety of new models. Therefore, the outgoing models are available at attractive with good offers will increase the demand.
<br />•	The demands of cars are seeing increasing in each year compared to previous year may be due to increasing GDP.

### Correlation of Features:
![image](https://user-images.githubusercontent.com/87713648/167316573-675c29d4-da85-4d94-b27d-6f1f86a90cdc.png)

The highly correlated features are linearly dependent and hence have same effect on the dependent variable. So I dropped one of the two features which are highly correlated.  In this dataset I have dropped {'dayofyear', 'quarter', 'weekofyear'}

## Modeling 
I have tried various ML models such as Linear Regression, Decision Tree Regressor, Random Forest Regressor, XG boost and LGBM Regressor through hyper parameter tuning through GridSearchCV and found out LGBM is giving RMSE value of 32.09503388599971 which is least compared to other models.








