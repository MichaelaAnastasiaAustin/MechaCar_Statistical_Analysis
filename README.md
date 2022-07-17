# MechaCar_Statistical_Analysis

## Overview

AutosRUs’ newest prototype, the MechaCar, is suffering from production troubles that are blocking the manufacturing team’s progress. AutosRUs’ upper management has tasked us with reviewing the production data for insights that may help the manufacturing team. Specifically, we will:

- Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes
- Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots
- Run t-tests to determine if the manufacturing lots are statistically different from the mean population
- Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. For each statistical analysis, you’ll write a summary interpretation of the findings.


## Results

## Linear Regression to Predict MPG

![Deliverable_1_Screenshot](https://github.com/MichaelaAnastasiaAustin/MechaCar_Statistical_Analysis/blob/main/images/Deliverable_1_IMG.png)

- Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?

According to our results, vehicle length and ground clearance are the variables/coefficients that provided a non-random amount of variance to the mpg values in the data set. Furthermore, vehicle length and ground clearance have a significant impact on on mpg. Meanwhile, vehicle weight, spoiler angle, and AWD do not have a significant impact on mpg. 

- Is the slope of the linear model considered to be zero? Why or why not?

The p-value for this model is 5.35e-11, a value much smaller than our assumed =significance level of 0.05%. Therefore, we can state that there is sufficient evidence to reject our null hypothesis, which means that the slope of our linear model is not zero.

- Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?

The linear model has an r^2 value of 0.7149, meaning the model can predict approximately 71.5% mpgs of MechaCar prototypes. Furthermore, the model does predict mpg of MechaCar prototypes effectively. 

## Summary Statistics on Suspension Coils

- The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?

For all manufacturing lots, the variance of the suspension coils is 62.29, which satisfies the design specification.

![total_summary](https://github.com/MichaelaAnastasiaAustin/MechaCar_Statistical_Analysis/blob/main/images/total_summary.png)

Lot 1 and Lot 2 also satisfy the suspension coil design specification with variances of 0.98 and 7.47. Lot 3 has a much larger variance-- 170.29-- which does not satisfy the rule of exceeding 100 pounds per square inch. This breakdown highlights that Lot 3's  disproportionately large variance greatly impacted the variance for all manufacturing lots. 

![lot_summary](https://github.com/MichaelaAnastasiaAustin/MechaCar_Statistical_Analysis/blob/main/images/lot_summary.png)

## T-Tests on Suspension Coils

The first t-test compares all manufacturing lots against mean PSI of the population:

![ttest](https://github.com/MichaelaAnastasiaAustin/MechaCar_Statistical_Analysis/blob/main/images/t_test.png)

As first shown in the summary statistics above, this t-test indicates that the mean of the sample is 1498.78. The t-test indicates that the p-value is 0.06, which is higher than the assumed significance level of 0.05, therefore, we do *not* have sufficient evidence to reject the null hypothesis. Further, the mean of all manufacturing lots is statistically similar to the population mean of 1,500 pounds per square inch.


The next three t-tests compare each manufacturing lot against mean PSI of the population:

Lot1
![t_test_lot1](https://github.com/MichaelaAnastasiaAustin/MechaCar_Statistical_Analysis/blob/main/images/t_test_lot1.png)

Lot 1 has a sample mean of 1500, as first shown in the summary statistics above. The t-test indicates that the p-value is 1 which is much higher than the assumed significance level of 0.05, meaning we do *not* have sufficient evidence to reject the null hypothesis. Furthermore, the mean of Lot 1 is statistically similar to the population mean of 1,500 pounds per square inch.

Lot2
![t_test_lot2](https://github.com/MichaelaAnastasiaAustin/MechaCar_Statistical_Analysis/blob/main/images/t_test_lot2.png)

Similar to Lot 1, the sample mean of Lot 2 is 1500.2. The p-value is 0.6072 which is higher than the assumed significance level of 0.05, meaning we do *not* have sufficient evidence to reject the null hypothesis. The mean of Lot 2 is statistically similar to the population mean of 1,500 pounds per square inch.

Lot 3
![t_test_lot3](https://github.com/MichaelaAnastasiaAustin/MechaCar_Statistical_Analysis/blob/main/images/t_test_lot3.png)
The final t-test indicates that Lot 3 has a sample mean of 1496.14. The p-value is 0.04, which is lower than the assumed significance level of 0.05. Furthermore, we have sufficient evidence to reject the null hypothesis. The mean of Lot 3 is statistically different than the population mean of 1,500 pounds per square inch.

## Study Design: MechaCar vs Competition
There are several factors that must be considered when assessing a car's performance. To support AutosRUs’ newest prototype, we will design one final study assessing MechaCar versus competition.  

### What metric or metrics are you going to test?
We will be testing one of the leading metrics that consumers take into consideration when purchasing a car: cost.

### What is the null hypothesis or alternative hypothesis?

- H0 : The means of cost of all vehicles in this class are equal.

- Ha : At least one of the vehicles in this class has a different mean of cost than the other vehicles.

What statistical test would you use to test the hypothesis? And why?

To test the hypothesis, we will use the analysis of variance (ANOVA) test. ANOVA tests are used to compare the means of a continuous numerical variable across a number of groups. Specifically, we will use a one-way ANOVA test to test the means of a single dependent variable across a single independent variable with multiple groups. For this study, we will be testing the mean cost of MechaCar against several other competitors' vehicles.

What data is needed to run the statistical test?
The data we will need is the cost of MechaCars as well as the cost of competitors' vehicles. Additionally, ANOVA tests have assumptions about the input data that must be validated prior to using the statistical test:

- The dependent variable is numerical and continuous, and the independent variables are categorical.
- The dependent variable is considered to be normally distributed.
- The variance among each group should be very similar.

