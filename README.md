# MechaCar_Statistical_Analysis

## Linear Regression to Predict MPG

* The variables/coefficients which provided a non-random amount of variance to the mpg values in the dataset are vehicle length and ground clearance. We see this reflected in the p-value scores for each variable as they’re both below the significance level of .05. Conversely, we see vehicle weight, spoiler angle, and AWD (all wheel drive) all have p-values above .05, which indicates they’ve provided random amounts of variance to the dataset. 

* The slope of the linear model is not considered to be zero, as the p-value of 5.35x10-11 is lower than even an extreme level of significance. Thus the null hypothesis must be rejected. This means that the relationship between our variables and the miles per gallon is subject to more than random chance.

* This linear model has an r-squared value of 0.7149, which means that approximately 71% of all mpg predictions will be determined by this model. Relatively speaking, this multiple regression model does predict mpg of MechaCar prototypes effectively. 
