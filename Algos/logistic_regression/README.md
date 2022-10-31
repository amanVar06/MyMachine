# INTRODUCTION <br />

Logistic regression is one of the most popular Machine Learning algorithms, which comes under the Supervised Learning technique. It is used for predicting the categorical dependent variable using a given set of independent variables. It estimates the probability of an event occurring, such as voted or didn’t vote, based on a given dataset of independent variables. Since the outcome is a probability, the dependent variable is bounded between 0 and 1. <br />
The most common logistic regression models a binary outcome; something that can take two values such as true/false, yes/no, and so on. Multinomial logistic regression can model scenarios where there are more than two possible discrete outcomes. <br />

## Type of Logistic Regression: <br />
On the basis of the categories, Logistic Regression can be classified into three types: <br />

- **Binomial:** In binomial Logistic regression, there can be only two possible types of the dependent variables, such as 0 or 1, Pass or Fail, etc. <br />
- **Multinomial:** In multinomial Logistic regression, there can be 3 or more possible unordered types of the dependent variable, such as "cat", "dogs", or "sheep" <br />
- **Ordinal:** In ordinal Logistic regression, there can be 3 or more possible ordered types of dependent variables, such as "low", "Medium", or "High". <br />

## Logistic Function (Sigmoid Function): <br />

Model <br />
Output = 0 or 1 <br />
Hypothesis => Z = WX + B <br />
hΘ(x) = sigmoid (Z) <br />

- The sigmoid function is a mathematical function used to map the predicted values to probabilities. <br />
- It maps any real value into another value within a range of 0 and 1. <br />

![image](https://user-images.githubusercontent.com/98205162/199023198-c5b5d82b-6b60-4e7b-b89c-d185a0895ec7.png) <br />

If ‘Z’ goes to infinity, Y(predicted) will become 1 and if ‘Z’ goes to negative infinity, Y(predicted) will become 0. <br />

## Decision Boundary <br />
To predict which class a data belongs, a threshold can be set. Based upon this threshold, the obtained estimated probability is classified into classes. <br />

Say, if predicted_value ≥ 0.5, then classify email as spam else as not spam. <br />

Decision boundary can be linear or non-linear. Polynomial order can be increased to get complex decision boundary.<br />

## Cost function <br />

![image](https://user-images.githubusercontent.com/98205162/199024611-a9d3d0df-c9b8-420f-b36c-1dc21b2c17b4.png) <br /> <br />

 **Simplified cost function** <br />
![image](https://user-images.githubusercontent.com/98205162/199023666-5d3d9371-6c26-4fcb-b13e-420ecfbbeb18.png) <br />

## Assumptions for Logistic Regression: <br />

- The dependent variable must be categorical in nature. <br />
- The independent variable should not have multi-collinearity. <br />

## Linear regression vs logistic regression <br />
Linear regression models are used to identify the relationship between a continuous dependent variable and one or more independent variables. When there is only one independent variable and one dependent variable, it is known as simple linear regression, but as the number of independent variables increases, it is referred to as multiple linear regression. For each type of linear regression, it seeks to plot a line of best fit through a set of data points, which is typically calculated using the least squares method. <br />

Similar to linear regression, logistic regression is also used to estimate the relationship between a dependent variable and one or more independent variables, but it is used to make a prediction about a categorical variable versus a continuous one. A categorical variable can be true or false, yes or no, 1 or 0, etc. The unit of measure also differs from linear regression as it produces a probability, but the logit function transforms the S-curve into straight line.  <br />

## Conclusion <br />
Logistic regression is a useful analysis method for classification problems, where you are trying to determine if a new sample fits best into a category. As aspects of cyber security are classification problems, such as attack detection, logistic regression is a useful analytic technique. <br />
Logistic Regression is a significant machine learning algorithm because it has the ability to provide probabilities and classify new data using continuous and discrete datasets. <br />
Logistic Regression can be used to classify the observations using different types of data and can easily determine the most effective variables used for the classification. <br />
