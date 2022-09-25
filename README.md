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


## T-Tests on Suspension Coils

Using our knowledge of R, perform t-tests to determine if all manufacturing lots and each lot individually are statistically different from the population mean of 1,500 pounds per square inch.

**Technical Analysis**

a)	Write an RScript using the t.test() function to determine if the PSI across all manufacturing lots is statistically different from the population mean of 1,500 pounds per square inch.

![image](https://user-images.githubusercontent.com/106939511/192158845-60941288-c07f-413e-a502-81c2951577a0.png)

b)	Write three more RScripts in your MechaCarChallenge.RScript using the t.test() function and its subset() argument to determine if the PSI for each manufacturing lot is statistically different from the population mean of 1,500 pounds per square inch.

Lot 1:

![image](https://user-images.githubusercontent.com/106939511/192158879-e9e465fb-a3eb-4a6f-99df-303ccf8b85d5.png)

Lot 2:

![image](https://user-images.githubusercontent.com/106939511/192158899-5cb04659-fe2a-4724-a7cb-504b8c942eef.png)

Lot 3:

![image](https://user-images.githubusercontent.com/106939511/192158918-30beac39-cf51-4a59-800a-e819deaf2f33.png)

c)	Statistical Summary 

## Study Design: MechaCar vs Competition







