# Mecha Char Statistical Analysis

## Linear Regression To Predict MPG
Using a Multiple Linear Regression analysis, we measured the effects of vehicle length, vehicle weight, spoiler angle, groun clearance, and drivetrain on the mpg achieved by the mechacar throughout it's iterations. from this assessment we found the following:
1. Vehicle lengh and ground clearance provided the most reliable non-random variance in their effect on mpg based on p-values of 5.08e-8 and 5.21e-8 respectively (Fig.2). 
2. Of the variables measured included positive slopes for vechicle length and ground clearance andn a negative slope for drivetrain, but the remaining values appeared to be close to 0 in their slope (Fig.1). 
3. By taking r-squared and p-value into consideration for the whole regression, we see that the multiple r-squared was 0.715 and the p-value was 5.35e-11. This shows that we have a strong correlation with r-squared showing that this prediction is strong and a very low p-value indicating that we can definitely reject the null hypothesis that there is no effect from these varaibles on the mpg of the mechacar. These together show that we can trust the predictions of this model when it says that the values measured are in fact influencing mpg (Fig.2). 

### Fig. 1: Multiple Linear Regression
![Linear Regression](https://github.com/ghynox/mechacar_statistical_analysis/blob/main/angle_coeffs.png)

### Fig. 2: Summary Of Linear Regression
![Summary](https://github.com/ghynox/mechacar_statistical_analysis/blob/main/linear_regression.png)




## Summary Statistics On Suspension Coils
Based on measurements taken from samples of the suspension coils during production, we can see that as a measurement of all lots (1,2, and 3) combined, we have a varaince of 62.3PSI which is within the safe range of <100PSI variabnce, however the outcomes change a bit with clsoer inspection (Fig.3). By calculating each lot individually, we can see coils produced in lots 1 and 2 meet the required standards of having variance of less than 100PSI across the lot with 0.97PSI and 7.46PSI respectively (Fig.4). Unfortunately, lot 3 shows a variance of 170.2PSI which exceeds the allowable variance and fails to meet sarety standards (Fig.4). 

### Fig. 3: Total Summary
![Total Summary](https://github.com/ghynox/mechacar_statistical_analysis/blob/main/total_summary.png)

### Fig 4. Lot Summary
![Lot Summary](https://github.com/ghynox/mechacar_statistical_analysis/blob/main/lot_summary_psi.png)


## T-Tests On Suspension Coils
By performing a one-sample T-Test on the collected data from the suspension coil production lots, we are able to assess whether the mean PSI values are close enough to the expected 1500 PSI of the ideal coils with statistical significance. The T-Test of the full production of coils produced a p-value of 0.06, ranging just outside the 0.05 cutoff required to reject the null hypothesis that the mean PSI of the coils is not equal to the expected mean with statistical significance (Fig.5). In other words, the entire population of coils shows a mean that is close enough to the expected mean. When the population of coils is broken down into the Lot productions, the story changes however. Lot 1 shows a perfect p-value of 1 and t-value of 0 indicating that the measured mean is exactly the same as the expectd mean (Fig.6). These are perfect. Lot 2 shows a p-value of 0.61 indicating that we are still well above the 0.05 level of significance to be confident that the samples are in line iwth the null hypothesis (Fig.7). Lot 3 on the other hand shows a p-value of 0.042. This is below the 0.05 significance level indicating that we can now reject the null hypothesis and state that the mean of the sample is not equal to the mean of the 1500 PSI expected (Fig.8). This batch should be remade. 

### Fig. 5: Total T-Test
![Total T-Test](https://github.com/ghynox/mechacar_statistical_analysis/blob/main/ttest_total.png)

### Fig. 6: T-Test Lot 1
![T-Test Lot 1](https://github.com/ghynox/mechacar_statistical_analysis/blob/main/ttest_lot1.png)

### Fig. 7: T-Test Lot 2
![T-Test Lot 2](https://github.com/ghynox/mechacar_statistical_analysis/blob/main/ttest_lot2.png)

### Fig. 8: T-Test Lot 3
![T-Test Lot 3](https://github.com/ghynox/mechacar_statistical_analysis/blob/main/ttest_lot3.png)

## Study Design: MechaCar vs Competition
Comparing MechaCar against its competitors would require identifying key factors that matter to buyers and then comparing samples of data related to those factors from each of the competitors and MechaCar, measuring for statistical significance in the differences. The ideal test for this would be a one-way ANOVA Test because it allows for the measurement of variances of multiple groups simultaneously. Through this we can see if any of the measured vehicles stands out, followed by further testing to identify the car that is performing exceptionally. If the test returns a p-value greater thatn 0.05, then we know that we cannot reject he null hypothesis that the means are the same for all independent variables, or that the means of the measured samples are not different enough to be statistically significant. If we return a <0.05 p-value, we know that we would have to go tiw ththe alternative hypothesis that there is a difference in means, or that one or more of the cars are performing notably better or worse. After that, we can look at the general statistics of each car and compare them individually to confirm. For data, we would need sufficiently large samples of the desired metrics that we can run mean analysis on. The key values that we should use for this test are: hp, torque, mpg (city and hwy), braking distance, repair/maintenance costs, weight, cylinders, displacement, transmission gearing, and safety ratings. 



