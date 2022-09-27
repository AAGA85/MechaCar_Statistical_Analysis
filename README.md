# MechaCar_Statistical_Analysis

# SUMMARY
A few weeks after starting his new role, Jeremy is approached by upper management about a special project. AutosRUs’ newest prototype, the MechaCar, is suffering from production troubles that are blocking the manufacturing team’s progress. AutosRUs’ upper management has called on Jeremy and the data analytics team to review the production data for insights that may help the manufacturing team.

In this challenge, we’ll help Jeremy and the data analytics team do the following:
•	Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes
•	Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots
•	Run t-tests to determine if the manufacturing lots are statistically different from the mean population
•	Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. For each statistical analysis, we’ll write a summary interpretation of the findings.

# RESULTS
## Linear Regression to Predict MPG

The MechaCar_mpg.csv dataset contains mpg test results for 50 prototype MechaCars (see image below). The MechaCar prototypes were produced using multiple design specifications to identify ideal vehicle performance. Multiple metrics, such as vehicle length, vehicle weight, spoiler angle, drivetrain, and ground clearance, were collected for each vehicle.

![del1 tab1](https://user-images.githubusercontent.com/106939511/192154950-9e803662-6faa-42fe-a30f-9f2972403f70.png)


**Technical Analysis**

Using the R knowledge, we will design a linear model that predicts the mpg of MechaCar prototypes using several variables from the MechaCar_mpg.cvs file.
a)	Resulting model:
Mpg = (6.267) vehicle_legth + (0.00124)vehicle_weight + (0.0687)spoiler_angle + (3.546)ground_clearance + (-3.411)AWD – 104.0


![del1 form1](https://user-images.githubusercontent.com/106939511/192154967-d036e6f3-8840-4955-873c-d239ceea2cfb.png)


b)	P-values and R-squared value for the linear regression model:

![del1 form2](https://user-images.githubusercontent.com/106939511/192155047-d544c602-a8fb-4206-9ed7-f3a095712b6d.png)


c)	Statistical Summary:

•	Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset? According to the linear regression in R the **Pr(>|t|)** column represents the p-value associated with the value in the t value colum, so here how to interpret the values in the Pr(>|t|):

1) The p-value for the predictor variable **vehicle_length** is < than our significance level 0.05, then it has a **statistical significan relationship** with the response variable in the model (MPG).

2) The p-value for the predictor variable vehicle_weight is 0.07 > than our significance level 0.05, then it has not  a statistical significan relationship with the response variable in the model (MPG).

3) The p-value for the predictor variable spoiler_angle is 0.30 > than our significance level 0.05, then it has not  a statistical significan relationship with the response variable in the model (MPG).

4) The p-value for the predictor variable **ground_clearance** is < than our significance level 0.05, then it has a **statistical significan relationship** with the response variable in the model (MPG).

•	Is the slope of the linear model considered to be zero? Why or why not? To answer this questions we can test **the null hypothesis H0: a=0**, that is , the case where the slope is zero. The multiple linear regression that we run finds a coefficient of 5.35e-11. This coefficient is very much significantly different from zero, in other words, **the probability that the H0 is zero is very small**. 

•	Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not? According to the statistics in the multiple analysis regression, **the R square** tell us that the 71% of the predictions of the MPG can be explained by this model, that means this model has **71% of efFiciency to calculate the MPG of MechaCar prototypes**.




## Summary Statistics on Suspension Coils

The MechaCar Suspension_Coil.csv dataset contains the results from multiple production lots (see image below). In this dataset, the weight capacities of multiple suspension coils were tested to determine if the manufacturing process is consistent across production lots.

![image](https://user-images.githubusercontent.com/106939511/192158733-53936eec-603a-447a-87d8-e2f6032004b3.png)


**Technical Analysis**

Using our knowledge of R, you’ll create a summary statistics table to show:

a)	The suspension coil’s PSI continuous variable across all manufacturing lots (total_summary dataframe)

![image](https://user-images.githubusercontent.com/106939511/192158760-78e3e392-fc4a-475b-b835-ee05bfc9956a.png)

b)	The following PSI metrics for each lot: mean, median, variance, and standard deviation (lot_summary dataframe)

![image](https://user-images.githubusercontent.com/106939511/192158777-750c4f88-ef8c-4dbe-af9a-15b189f5ab4b.png)

c)	Statistical Summary 

The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?

Using screenshots from our total_summary and lot_summary dataframes, we can conclude that the Variance of the entire population (62.29 PSI) does not exceed the design specification.

When we look at the values of the variance per lot of production, the story seems a little bit different. Lot 1 and Lot 2 with a variance of 0.98 PSI and 7.47 PSI accordingly, which means that both are meeting the design specification. Nevertheless the Lot 3 is out of the specification becuase its variance is 170 PSI.

## T-Tests on Suspension Coils

Using our knowledge of R, perform t-tests to determine if all manufacturing lots and each lot individually are statistically different from the population mean of 1,500 pounds per square inch.

**Technical Analysis**

a)	Write an RScript using the t.test() function to determine if the PSI across all manufacturing lots is statistically different from the population mean of 1,500 pounds per square inch.

![image](https://user-images.githubusercontent.com/106939511/192421680-37cce579-295e-41f3-b0a7-9994f7259fa4.png)


b)	Write three more RScripts in your MechaCarChallenge.RScript using the t.test() function and its subset() argument to determine if the PSI for each manufacturing lot is statistically different from the population mean of 1,500 pounds per square inch.


![image](https://user-images.githubusercontent.com/106939511/192421295-637fdd1e-a5f4-4b1a-af1a-3a09fb4b4556.png)



c)	Statistical Summary 

As we learned in this module the t-test is one of the most popular statistical test and in this deliverable it will help us to determine whether is a statistical difference between means of a sample dataset and a hypothesized population dataset as follows:

H0 : Our sample mean is equal to its presumed population mean.
Ha : Our sample mean is not equal to our presumed population mean.

According to the t-test run over the entire population, the real mean is 1498.78, based on the results of the image below. The p-value of 0.06 which is > than our sigificance level of 0.05, therefore, we do not have sufficient evidence to reject the null hypothesis, and we would state that the sample is equal to its presumed population mean (1500).

![image](https://user-images.githubusercontent.com/106939511/192158845-60941288-c07f-413e-a502-81c2951577a0.png)


But now we will study every lot separately:

Lot 1: According to the t-test run over the entire population, the real mean is 1500 based on the results showed in the image below. The p-value of 1 which is > than our sigificance level of 0.05, therefore, we do not have sufficient evidence to reject the null hypothesis, and we would state that the sample is equal to its presumed population mean (1500).

![image](https://user-images.githubusercontent.com/106939511/192158879-e9e465fb-a3eb-4a6f-99df-303ccf8b85d5.png)

Lot 2: According to the t-test run over the entire population, the real mean is 1500.02 based on the results showed in the image below. The p-value of 0.06 which is > than our sigificance level of 0.05, therefore, we do not have sufficient evidence to reject the null hypothesis, and we would state that the sample is equal to its presumed population mean (1500).

![image](https://user-images.githubusercontent.com/106939511/192158899-5cb04659-fe2a-4724-a7cb-504b8c942eef.png)

Lot 3: According to the t-test run over the entire population, the real mean is 1496.14 based on the results showed in the image below. The p-value of 0.04 which is < than our sigificance level of 0.05, therefore, we have sufficient evidence to reject the null hypothesis, and we would state that the sample is not equal to its presumed population mean (1500).

![image](https://user-images.githubusercontent.com/106939511/192158918-30beac39-cf51-4a59-800a-e819deaf2f33.png)

## Study Design: MechaCar vs Competition

The most important factor to determine the success of any product must be the voice of the customer. In the recent years, more and more industries are trying to develop way to have a clear understanding of the customer needs, expectations and product improvement. If AutoRU’s focuses to improve the product MechaCar using the customer experience with real customer insights to develop a model to predict the owner satisfaction, there will be more propabilities to have a success launch. 
As with any vehicle, reliability is always a top consideration because the vehicle cannot be a good for the customer if it is always in the shop right?

**Metrics and Data**
Our statistical study will be focused on develop a model that contains information of the top 3 competitors and the AutosRUs historical data with similar products to MechaCar type, including significant variables that our team of data analytics could collect of the latest 2 or 3 model years of those cars:
a) Frequency of failures reported the first 1 year 
b) Average cost of repair 
c) Number of recalls 

**Hypothesis: Null and alternative**

•	Null Hypothesis: The reliability of the car is dependable of the metrics defined. 

•	Alternative Hypothesis: The reliability of the car is not based on the performance of the variables

**Statistical Test**

For this case we will use a multiple linear regression because this statistical test will help us to determine if the metrics in the model have a high correlation with the reliability of the vehicle. With this information AutoRUs will be able to measure the reliability of similar cars and with that,  predict the reliability that could have this new lunch. 






