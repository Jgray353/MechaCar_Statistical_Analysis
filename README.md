# MechaCar_Statistical_Analysis

## Linear Regression to Predict MPG

The purpose of this analysis is use linear regression in R to determine which variables/coeffiecients have the biggest non random impact on fuel efficiency (MPG) for the MechaCar.

* The variables/coefficients which provided a non-random amount of variance to the MPG values in the dataset are vehicle length and ground clearance. We see this reflected in the p-value scores for each variable as they’re both below the significance level of .05. Conversely, we see vehicle weight, spoiler angle, and AWD (all wheel drive) all have p-values above .05, which indicates they’ve provided random amounts of variance to the dataset. 

* The slope of the linear model is not considered to be zero, as the p-value of 5.35x10-11 is lower than even an extreme level of significance. Thus the null hypothesis must be rejected. This means the relationship between our variables and the fuel efficiency is subject to more than random chance.

* Relatively speaking, this linear regression model does predict MPG of MechaCar prototypes effectively. This linear model has an r-squared value of 0.7149, which means that approximately 71% of all mpg predictions will be determined by this model. 


<img width="550" alt="Deliverable_1_Challenge15" src="https://user-images.githubusercontent.com/90881705/150242138-38252e5b-185e-46af-88a4-f3a48a24f7cc.png">


## Summary Statistics on Suspension Coils

The purpose of this analysis is to view the mean, median and variance of the PSI for the suspension coils used in the MechaCar. Since ground clearance is a variable which provides non random variance to fuel efficency, we want to ensure the total production run of coils and each lot are within the variance of 100 PSI. Which is per the MechaCar design specifications. In the screen shots for the total summary, we see the variance is 62.29 PSI, well within the variance limit set forth in the design specs. 


<img width="499" alt="Deliverable_2_SS1_Challlenge15" src="https://user-images.githubusercontent.com/90881705/150242772-6f370a94-f5e0-4c9b-8825-8a25fe214660.png">


However, in the lot summary screenshot we see that lot 3 has a variance of 170.29 PSI, well over the variance of 100 PSI. Lots 1 and 2 both have low levels of variance, with .98 PSI for lot 1 and 7.47 for lot 2. So while the total variance is within spec, we see in the lot breakdown that there is some inconsistency in the manufacturing or quality assurance process. Perhaps lot 3 came from a specific facility. 


<img width="647" alt="Deliverable_2_SS2_Challenge15" src="https://user-images.githubusercontent.com/90881705/150242849-13a50aa3-32b4-4a43-afc4-bdd8a8df8b7f.png">


## T-Tests on Suspension Coils

From here we can see the true mean of the sample is 1498.78, which we also saw in the summary statistics above. With a p-Value of 0.06, which is higher than the common significance level of 0.05, there is not enough evidence to support rejecting the null hypothesis. That is to say, the mean of all three of these manufacturing lots is statistically similar to the presumed population mean of 1500.


<img width="417" alt="Deliverable_3_TTestTotal" src="https://user-images.githubusercontent.com/90881705/150245265-0286d66a-67e8-42dd-beb2-90d9ef950d86.png">


And the following is a breakdown of each lot: 

Lot 1 sample actually has the true sample mean of 1500, again as we saw in the summary statistics above. With a p-Value of 1, we cannot reject (i.e. accept) the null hypothesis that there is no statistical difference between the observed sample mean and the presumed population mean (1500). A quick glance at the 50 units in lot 1 shows little variance as every PSI is within 2 pounds of 1500. 


<img width="418" alt="Deliverable_3_TTestLot1" src="https://user-images.githubusercontent.com/90881705/150245868-bd20f01c-d4a8-4a7a-9e6f-6f2fe65e4dd8.png">


Lot 2 has close to the same outcome with a sample mean of 1500.02, a p-Value of 0.61; the null hypothesis cannot be rejected, and the sample mean and the population mean of 1500 are statistically similar. Similar to lot 1, there is little variance from 1500 PSI, with everything being with 5 pounds. 


<img width="419" alt="Deliverable_3_TTest2" src="https://user-images.githubusercontent.com/90881705/150245912-4d93273e-a082-47a9-91b3-f96a9fcc1233.png">



However, Lot 3, not surprisingly is a different scenario. Here the sample mean is 1496.14 and the p-Value is 0.04, which is lower than the common significance level of 0.05. All indicating to reject the null hypothesis that this sample mean and the presumed population mean are not statistically different. The lot breakdown shows several totals which are 15+ PSI under 1500.


<img width="423" alt="Deliverable_3_TTest3" src="https://user-images.githubusercontent.com/90881705/150245920-ba5974d9-0e28-421c-bcba-318b3bca08b4.png">


## Study Design: MechaCar vs Competition

A statistical study can be done to see how MechaCar performs against the competition. We would want to focus on the most important aspects buyers consider when purchasing a vehicle. Some of those aspects - but not limited to -  would be price, cost of ownership, fuel efficiency, resale value, and safety ratings. These are consistently among the top factors for car buyers.

Our study hypotheses are defined as follows:

H0: There is NO statistical significant difference on defined metrics between MechaCar and the competition.
Ha: There IS statistical significant difference on defined metrics between MecharCar and the competition.

The significance value defined for the study is 0.05. In order to perform the analysis, we would need to collect the data for each aspect listed above. And we would be collecting competitor data for cars in the same class as MechaCar. All the competitor data is grouped together for our analysis. Then we would perform t-tests on each metrics for MechaCar against the same metric from the collective competitor data. If the p-value for each of the t-tests is less than 0.05, then we will reject our NULL hypothesis.

