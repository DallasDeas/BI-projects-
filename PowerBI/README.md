# Analyzing the Factors Behind Sales Performance

### [[Project File]](/PowerBI/Content/Sales_Analytics_Dashboard.pbix)      

### [[Back to Portfolio]](https://github.com/DallasDeas/Portfolio)


## *PowerBI Dashboard Preview*
![Dashboard Preview](/PowerBI/Images/SalesDashboard/SalesDashboard.png)

## Goal
- The goal of this dashboard is to provide a overview of **sales performance** by analyzing key metrics such as *revenue*, *customer trends*, and *product profitability*. It enables **data-driven decision-making by visualizing insights** on sales trends, world performance, and KPIs to **optimize business growth**.
## Description
- This Sales Analytics Dashboard was built using Power BI to track business metrics such as revenue, sales trends, customer behavior, and product performance. This project was customized with imported interactive visualizations, **key performance indicators (KPIs)**, and drill-down capabilities to support data-driven decision-making.
  
- By incorporating **DAX calculations**, **Power Query transformations**, and interactive charts, the dashboard enables businesses to **analyze sales growth over time**, **regional sales distribution**, and **product profitability**. It also provides insights into customer purchasing patterns, helping business strategies.
  
- This project demonstrates my ability to work with **data visualization**, **business intelligence tools**, and **performance analysis** to create meaningful reports that drive informed business decisions.
## Analysis
![Dashboard Preview](/PowerBI/Images/SalesDashboard/Sales_for_the_last_week.png)
```DAX
Profit for the last week = 
CALCULATE(
    SUM(Orders[Profit]), 
    Orders[Order Date] >= MAX('Orders'[Order Date]) - 7
)

Sales for the last day = 
CALCULATE(
    SUM(Orders[Sales]), 
    Orders[Order Date] = MAX('Orders'[Order Date])
)

Sales for the last week = 
CALCULATE(
    SUM(Orders[Sales]), 
    Orders[Order Date] >= MAX('Orders'[Order Date]) - 7
)

Shipping for the last week = 
CALCULATE(
    SUM(Orders[Shipping Cost]), 
    Orders[Order Date] >= MAX('Orders'[Order Date]) - 7
)
```
- These ***DAX formulas*** automatically analyze sales data by using the ***CALCULATE*** function to filter results based on the most recent date in the dataset. Using the ***MAX(Order Date)*** function ensures the calculations always reference the latest available data, while ***>=*** (greater than or equal to) creates rolling timeframes for the past day or week. This process enables real-time tracking of profit, sales, and shipping costs, ensuring the dashboard stays up-to-date without manual adjustments.
##
![Dashboard Preview](/PowerBI/Images/SalesDashboard/Profit_and_Sales_by_Month.png)
- This Profit and Sales by Month chart provides a clear breakdown of ***monthly revenue and profitability trends***. Sales show a steady increase throughout the year, ***peaking in November ($555K) and December ($503K)***, indicating strong year-end performance. However, ***profit remains significantly lower than sales***, with the ***highest profit recorded in November ($63K) and December ($47K)***, suggesting high operational costs or discounts impacting margins.  
##

![Dashboard Preview](/PowerBI/Images/SalesDashboard/Sales_Order_List.png)
- This Order List highlights key insights into ***profitability***, ***shipping costs***, and ***sales trends*** across different product categories. Many orders show ***negative profit***, especially in Technology and Office Supplies, which may be due to high costs, discounts, or pricing issues. Some orders also have high shipping costs that further ***reduce profit margins***.  Additionally, some Order IDs repeat in different categories, suggesting bundled purchases or split transactions. To display this table, I used an ***imported Power BI visual***, allowing for better organization and readability.
##
![Dashboard Preview](/PowerBI/Images/SalesDashboard/Sales_Revenue_charting.png)
- This Revenue Breakdown section provides insights into ***top-selling products***, ***country-wise revenue trends***, and ***category contributions***. The Top Products by Revenue table highlights that smartphones drive the highest sales, with Apple, Cisco, and Motorola models leading. The Countries by Revenue table uses ***conditional formatting*** to visually indicate revenue changes, with green arrows representing growth and red arrows highlighting declines. This formatting makes it easier to quickly ***identify positive trends*** in Australia, France, and Germany, while spotting ***revenue drops*** in Mexico and the U.S.. The Revenue by Category donut chart further breaks down sales performance, showing that Phones, Copiers, and Chairs generate the most revenue, while labels and fasteners contribute the least. 

## Skills
- ***Data Modeling***
- ***Data Visualization***
- ***Dashboard Creation***
- ***Data Analysis***
## Technology
- ***Power Query***
- ***PowerBI***
- ***Dax***
- ***M***
