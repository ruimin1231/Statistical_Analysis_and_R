# **Written Report on the Statistical Analysis of Mecha Car - R**


---
## 1. Linear Regression to Predict MPG

Did variables or coefficients provide a non-random amount of variance to the mpg values in the dataset? Looking at the Pr(>|t|) column we want to find which will indicate a non-random amount of variance to the mpg. 

Is the slope of the linear model considered to be zero? Why or why not?
The p-value is 5.35e-11 which smaller than the 0.05% significance level so it is no zero.

Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?
The linear model does predict the mpg because the R-squared number is 0.7149 so 71.49% of the predictions can be made with these models.

![Screen Shot 2022-02-06 at 11 29 32 PM](https://github.com/ruimin1231/Statistical_Analysis_and_R/blob/main/images/Screen%20Shot%202022-02-06%20at%2011.29.32%20PM.png)

---
## 2. Summary Statistics on Suspension Coils

First we look at all of the suspension coils manufactured and can see the following stats:
![Screen Shot 2022-02-06 at 11 29 32 PM](https://github.com/ruimin1231/Statistical_Analysis_and_R/blob/main/images/Total_summary.png)

Second we break it down and group the coils by the manufacturing lot and see:
![Screen Shot 2022-02-06 at 11 29 32 PM](https://github.com/ruimin1231/Statistical_Analysis_and_R/blob/main/images/lot_summary.png)

The AutosRU provides regulations that the PSI variance cannot exceed 100psi. As a whole the coils would pass, but in manufacturing things are looked at on a lot level. With this in mind only lot1 and lot2 pass, lot3 does not pass.


---
## 3. T-Tests on Suspension Coils

- To determin wheter there is a statistical difference between the mean of this dataset and the hypothesized dataset we have to conduct a t-test with a population mean of 1500. 

This is the summary of the t-test for all of the lots manufactured.
![T Test_All](https://github.com/ruimin1231/Statistical_Analysis_and_R/blob/main/images/T.Test_All.png)

- The p value is 0.06 which is higher than 0.05 which means there is not enough evidence to regject the null hypotheseis.

- When we look at the lots individually we see for lot1:

![t test_lot1](https://github.com/ruimin1231/Statistical_Analysis_and_R/blob/main/images/t.test_lot1.png)
*lot1 has a pvalue of 1 so we cannot reject the null hypothesis.*


![t test_lot2](https://github.com/ruimin1231/Statistical_Analysis_and_R/blob/main/images/t.test_lot2.png)
*lot2 has a pvalue of 0.6072 so we cannot rejeect the null hypothesis.*


![t test_lot3](https://github.com/ruimin1231/Statistical_Analysis_and_R/blob/main/images/t.test_lot3.png)
*lot3 has a pvalue of 0.04168 which is lower than 0.05 so the PSI for lot3 is statisticall different than the population mean.*


## 4.Study Design: MechaCar vs Competition


To compare the MechaCar's performance against it's competitors, I would need to first find it's competitors. To do this I would find other cars in it's price range then compare the acceleration, fuel/electricity efficiency, size, safety rating. I would then compare it amongst other cars in its class against the same metrics: price, acceleration, fuel efficiency, saftey. 

*What is the null hypothesis or alternative hypothesis?*

The null hypothesis would be: MechaCar is a good value based on its performance on the metrics mentioned above. The Alternattive hypothesis would be: MechaCar is not a good value based on its performance on the metrics mentioned above.

*What statistical test would you use to test the hypothesis? And why?*
I would use the ANOVA testing because I would be able to do head-to-head testing to compare different metrics I am evaluating.

*What data is needed to run the statistical test?*
I would need the performance data from other car manufacturers. This data is usually published on the car manufacturers sites.







