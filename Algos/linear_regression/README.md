# INTRODUCTION <br />
Linear regression is one of the easiest and most popular Machine Learning algorithms. It is a statistical method that is used to predict the value of a variable based on the value of another variable. The variable you want to predict is called the dependent variable. The variable you are using to predict the other variable's value is called the independent variable. <br />

Linear regression algorithm shows a linear relationship between a dependent (y) and one or more independent (y) variables, hence called as linear regression. <br />

The linear regression model provides a sloped straight line representing the relationship between the variables. <br />
![image](https://user-images.githubusercontent.com/98205162/198998660-af28252f-ed6f-47fc-9374-e5cfc153337e.png) <br />

Mathematically, we can represent a linear regression as: <br />
y= a0 + a1*x+ ε <br />

Here, <br />

y= Dependent Variable (Target Variable) <br />
x= Independent Variable (predictor Variable) <br />
a0= intercept of the line (Gives an additional degree of freedom) <br />
a1 = Linear regression coefficient (scale factor to each input value). <br />
ε = random error <br />

The values for x and y variables are training datasets for Linear Regression model representation. <br />

## Types of Linear Regression <br />

**Simple regression**: <br />
Simple linear regression uses traditional slope-intercept form, where m and b are the variables our algorithm will try to “learn” to produce the most accurate predictions. x represents our input data and y represents our prediction. <br />

y=mx+b <br />

**Multivariable regression**: <br />
A more complex, multi-variable linear equation might look like this, where w represents the coefficients, or weights, our model will try to learn. <br />

f(x,y,z)=w1x+w2y+w3z <br />

The variables x,y,z represent the attributes, or distinct pieces of information, we have about each observation. For sales predictions, these attributes might include a company’s advertising spend on radio, TV, and newspapers. <br />

Sales=w1Radio+w2TV+w3News <br />

## Finding the best fit line:

When working with linear regression, our main goal is to find the best fit line that means the error between predicted values and actual values should be minimized. The best fit line will have the least error. <br />
The different values for weights or the coefficient of lines (a0, a1) gives a different line of regression, so we need to calculate the best values for a0 and a1 to find the best fit line, so to calculate this we use cost function. <br />

For Linear Regression, we use the Mean Squared Error (MSE) cost function, which is the average of squared error occurred between the predicted values and actual values. It can be written as: <br />

![image](https://user-images.githubusercontent.com/98205162/199014517-5e759b2e-f415-455b-9fd8-ae6a6c083dac.png) <br />

Where, <br />
N = Total number of observation <br />
Yi = Actual value <br />
(a1xi+a0)= Predicted value. <br />

**Residuals:** The distance between the actual value and predicted values is called residual. If the observed points are far from the regression line, then the residual will be high, and so cost function will high. If the scatter points are close to the regression line, then the residual will be small and hence the cost function. <br />

## Gradient descent  <br />

To minimize MSE we use Gradient Descent to calculate the gradient of our cost function. Gradient descent consists of looking at the error that our weight currently gives us, using the derivative of the cost function to find the gradient (The slope of the cost function using our current weight), and then changing our weight to move in the direction opposite of the gradient. We need to move in the opposite direction of the gradient since the gradient points up the slope instead of down it, so we move in the opposite direction to try to decrease our error.  <br />

## Key assumptions of effective linear regression <br />

Assumptions to be considered for success with linear-regression analysis:

- **For each variable**: Consider the number of valid cases, mean and standard deviation. 
- **For each model**: Consider regression coefficients, correlation matrix, part and partial correlations, multiple R, R2, adjusted R2, change in R2, standard error of the     estimate, analysis-of-variance table, predicted values and residuals. Also, consider 95-percent-confidence intervals for each regression coefficient, variance -    covariance matrix, variance inflation factor, tolerance, Durbin-Watson test, distance measures (Mahalanobis, Cook and leverage values), DfBeta, DfFit, prediction       intervals and case-wise diagnostic information. 
- **Plots**: Consider scatterplots, partial plots, histograms and normal probability plots.
- **Data**: Dependent and independent variables should be quantitative. Categorical variables, such as religion, major field of study or region of residence, need to be       recoded to binary (dummy) variables or other types of contrast variables.  
- **Other assumptions**: For each value of the independent variable, the distribution of the dependent variable must be normal. The variance of the distribution of the         dependent variable should be constant for all values of the independent variable. The relationship between the dependent variable and each independent variable should   be linear and all observations should be independent.

## Conclusion <br />


Linear-regression models are relatively simple and provide an easy-to-interpret mathematical formula that can generate predictions. Linear regression can be applied to various areas in business and academic study. <br />

You’ll find that linear regression is used in everything from biological, behavioral, environmental and social sciences to business. Linear-regression models have become a proven way to scientifically and reliably predict the future. Because linear regression is a long-established statistical procedure, the properties of linear-regression models are well understood and can be trained very quickly.  <br />
