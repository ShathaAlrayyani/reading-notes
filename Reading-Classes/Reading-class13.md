## What Is Regression?
Regression searches for relationships among variables. 
For example, you can observe several employees of some company and try to understand how their salaries 
depend on their features, such as experience, education level, role, city of employment, and so on.

This is a regression problem where data related to each employee represents one observation. 
The presumption is that the experience, education, role, and city are the independent features, 
while the salary depends on them.

Similarly, you can try to establish the mathematical dependence of housing prices on area, number of bedrooms, 
distance to the city center, and so on.

Generally, in regression analysis, you consider some phenomenon of interest and have a number of observations. 
Each observation has two or more features. Following the assumption that 
at least one of the features depends on the others, you try to establish a relation among them.

## When Do You Need Regression?
Typically, you need regression to answer whether and how some phenomenon influences the other or how several variables 
are related. For example, you can use it to determine if and to what extent experience or gender impacts salaries.

Regression is also useful when you want to forecast a response using a new set of predictors. 
For example, you could try to predict electricity consumption of a household for the next hour 
given the outdoor temperature, time of day, and number of residents in that household.

Regression is used in many different fields, including economics, computer science, and the social sciences. 
Its importance rises every day with the availability of large amounts of data and increased awareness of the 
practical value of data.

## Linear Regression
Linear regression is probably one of the most important and widely used regression techniques.
It’s among the simplest regression methods. One of its main advantages is the ease of interpreting results.

## Scikit-learn

Scikit-learn is a powerful Python module for machine learning. 
It contains function for regression, classification, clustering, 
model selection and dimensionality reduction. 
Today, I will explore the sklearn.
linear_model module which contains “methods intended for regression in 
which the target value is expected to be a linear combination of the input variables”.

In this post, I will use Boston Housing data set, the data set contains information about the housing values 
in suburbs of Boston. This dataset was originally taken from the StatLib library which is maintained at 
Carnegie Mellon University and is now available on the UCI Machine Learning Repository. 
UCI machine learning repository contains many interesting data sets, I encourage you to go through it.

So come on lets have fun with linear regression,

Exploring Boston Housing Data Set

The first step is to import the required Python libraries into Ipython Notebook.

This data set is available in sklearn Python module, so I will access it using scikitlearn. 
I am going to import Boston data set into Ipython notebook and store it in a variable called boston.