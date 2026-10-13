DAX Measures

This document contains the DAX measures used in the Power BI dashboard.

1. total customers = DISTINCTCOUNT(Customers[CustomerID])
2. churned customer = CALCULATE(DISTINCTCOUNT(Customers[CustomerID]),Customers[Churn]=1)
3. churn rate = DIVIDE(Customers[churned customer],Customers[total customers])
4. Average Tenure = CALCULATE(AVERAGE(Customers[Tenure]),Customers[Churn]=1)
5. Tenure Group = 
SWITCH(
    TRUE(),
    Customers[Tenure] <= 12, "0-12 Months",
    Customers[Tenure] <= 24, "13-24 Months",
    Customers[Tenure] <= 36, "25-36 Months",
    Customers[Tenure] <= 48, "37-48 Months",
    "49+ Months"
)
6. Age Group = 
SWITCH(
    TRUE(),
    Customers[Age] < 25, "18-24",
    Customers[Age] < 35, "25-34",
    Customers[Age] < 45, "35-44",
    Customers[Age] < 55, "45-54",
    "55+"
)
7. Complaints from Churned Customers = 
CALCULATE(
    SUM(Feedback[Complaints]),
    Customers[Churn] = 1
)
8. Call Usage Group = 
SWITCH(
    TRUE(),
    Usage[CallMinutes] < 200, "Low",
    Usage[CallMinutes] < 500, "Medium",
    Usage[CallMinutes] < 800, "High",
    "Very High"
)
9. Data Usage Group = 
SWITCH(
    TRUE(),
    Usage[DataUsage] < 20, "Low",
    Usage[DataUsage] < 50, "Medium",
    Usage[DataUsage] < 80, "High",
    "Very High"
)
10. Message Usage Group = 
SWITCH(
    TRUE(),
    Usage[MessagesSent] < 100, "Low",
    Usage[MessagesSent] < 300, "Medium",
    Usage[MessagesSent] < 500, "High",
    "Very High"
)
11. Usage Pattern = 
Usage[Call Usage Group]
    & " Calls / "
    & Usage[Data Usage Group]
    & " Data / "
    & Usage[Message Usage Group]
    &" Message"
