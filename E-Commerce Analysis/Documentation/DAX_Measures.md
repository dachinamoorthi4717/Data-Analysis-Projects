DAX Measures

This document contains the DAX measures used in the Power BI dashboard.

1. Total Sales
Total Sales= SUM('Order Details'[Amount])

      It calculates the total of amount

2. Total Profit
Total Profit= SUM('Order Details'[Profit])

     It calculates the total profit

3. Total Quantity
Total Quantity= SUM('Order Details'[Quantity])

      It calculates the total quantity

4. Sales Target
Sales Target= SUM('Sales target'[Target])

     It calculates the sales target

5. Target Shortfall
Target Shortfall=[Total Sales] - [Sales Target]

      It Calculates the difference between the Total Sales and Sales Target 


7. Target Status
Target Status = IF('Order Details'[Total Sales]>='Sales target'[Sales Target],"Achived","not achived")

   It Calculates whether the target is achived or not achived   


