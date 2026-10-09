Business Questions – Adidas Sales Analysis

What is the total sales revenue?
What is the total profit?
What is the total number of units sold?
What is the average profit margin?
What is the average price per unit?
How do total sales vary by month?
How do total sales vary by state?
How do total sales vary by region?
Which products generate the highest sales?
Which retailers generate the highest sales?

This document contains the DAX measures used in the Power BI dashboard.

1. Total Sales
Sum Of Sales= SUM('Data Sales Adidas'[Total Sales])

Calculates the total sales amount.

2. Total Profit
Sum Of Profit = SUM('Data Sales Adidas'[Operating Profit])

Calculates the overall profit.

3. Total Units
Sum Of Units = SUM('Order Details'[Units Sold])

Calculates the total units sold.

4. Average Margin
Average of Margin = AVERAGE('Data Sales Adidas'[Operating Margin])

Calculates the average of operating margin

5.Average Price Per Unit
Average of Price per unit = AVERAGE('Data Sales Adidas'[Price per Unit])

Calculates the average of price per unit
