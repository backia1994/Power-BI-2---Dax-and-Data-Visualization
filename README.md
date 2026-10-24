 Power-BI-2---Dax-and-Data-Visualization
 DAX and Data Visualization – Sales Analysis
Project Overview
This Power BI mini project analyzes retail sales, profit, quantity, product sub-categories, monthly sales, category targets, and geographical performance. It uses DAX calculations and interactive visualizations to turn the supplied CSV data into business insights.
Tools Used
•	Microsoft Power BI
•	DAX (Data Analysis Expressions)
•	Power Query for data preparation
•	CSV datasets
Datasets
This report uses the three supplied datasets:
1.	Order Details(1).csv — Order ID, Amount, Profit, Quantity, Category, Sub-Category.
2.	List of Orders.csv — Order ID, Order Date, CustomerName, State, City.
3.	Sales target(1).csv — Month of Order Date, Category, Target.
Report Pages and Visualizations
The uploaded Dax and Data Visualization.pbix contains the following report pages:
•	Calculations — DAX calculations and measures.
•	Sales Target by Category — compares category targets.
•	Max Profit by Sub Category — highlights sub-categories by profit.
•	Monthly Sales — shows sales across months.
•	Profit, Quantity by Sub Category — compares profit and quantity by sub-category.
•	Sales Compare to Category — compares sales across categories.
•	Comparison Values — presents comparative metrics.
•	Map — geographic sales analysis.
•	Sub Category Tree Map — visualizes sub-category contribution.
•	State Funnel Map — explores performance by state.
Example DAX Measures
The following are common measures suitable for this dataset. If equivalent measures already exist in the PBIX, keep the existing measure names or adapt these formulas to avoid duplicates.
Total Sales =
SUM('Order Details'[Amount])

Total Profit =
SUM('Order Details'[Profit])

Total Quantity =
SUM('Order Details'[Quantity])

Total Orders =
DISTINCTCOUNT('List of Orders'[Order ID])

Profit Margin % =
DIVIDE([Total Profit], [Total Sales], 0)

Sales Target =
SUM('Sales target'[Target])

Sales vs Target =
[Total Sales] - [Sales Target]

Target Achievement % =
DIVIDE([Total Sales], [Sales Target], 0)
Format Profit Margin % and Target Achievement % as percentages. The target measures are valid only when date/month and category filtering correctly matches actual sales with the corresponding target rows.
Data Preparation and Model Checks
•	Set Amount, Profit, and Target to numeric/currency types, Quantity to a whole number, and Order Date to Date.
•	Standardize category, sub-category, state, and city text.
•	Check blank order dates and duplicate or repeated Order IDs before analysis.
•	Convert Month of Order Date values such as Apr-18 into a proper month/date field for time-based analysis.
•	Validate relationships between order details, order information, calendar dates, and sales targets. Avoid many-to-many or duplicate-key relationships unless intentionally designed.
•	Confirm that target totals are not duplicated when shown with actual sales.
Analysis Objectives
•	Measure total sales, profit, and quantity.
•	Compare sales and profit by category and sub-category.
•	Track monthly sales and category targets.
•	Identify high-profit and loss-making sub-categories.
•	Explore geographical differences across states and cities.
•	Present results in a report that supports data-driven decisions.
Conclusion
The Power BI report combines DAX calculations with charts, maps, and category/sub-category comparisons to examine retail sales performance. Monthly trends help track changes over time, profit and quantity visuals compare product sub-categories, and geographic visuals explore differences by location. The sales target page supports target monitoring by category. Before drawing final business conclusions, validate the model relationships, missing dates, repeated order IDs, and the alignment between monthly targets and actual sales.
Files in This Project
•	Dax and Data Visualization.pbix — Power BI report.
•	Order Details(1).csv — line-item sales and profit data.
•	List of Orders.csv — order dates and geographical/customer information.
•	Sales target(1).csv — monthly category sales targets.
