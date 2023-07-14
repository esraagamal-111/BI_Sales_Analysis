# Power_BI_in_Sales_Analysis
Power_BI_in_Sales_Analysis 

![Sales Analysis](cover.jpeg)

## Introduction
This project is to display Sales Analysis using POWER BI. The problem satatement is an imaginary case scenario I thought about after seeing the dataset.

## Problem Statement
A Sales director in an international company in the United States wishes to have a dynamic report clarify the Net Sales and gross margin up to date.

After discussion with him I noticed that he want a dynamic report which answer four main questions:
1. How is Sales Performance going over years.
2. Compare Gross Margin Year over Year.
3. How Many Customers Purchase two different product together.

That's inspire me to create three main dashboards and one detailed dashboard 
1- Sales Performance.
2- Gross Margin YOY.
3- Customers Cross selling
4- Order Detais

## Data Sourcing
 the information was seperated into differnt sheets or tables resulting into 5 tables:
- Customers
- Products
- Date
- Returns
- Sales

Data was then locally extracted from Excel Workbook into Power BI for transformation, analysis and visualization.

## Data Transformation

Data Transformation was performed to can easily apply star schema.
Data cleaning was performed per table.
The table appeared to be clean.
The quality of each column is 100% with no error or nulls.
Below is a preview of the tables:

Customers Table             |           Products Table
:--------------------------:|:------------------------:
![](Customers.png)         |         ![](Products.png)

Date Table              |               Returns Table
:---------------------------:|:----------------------
![](Date.png)                |     ![](Returns.png)


**Sales Table**
![](Sales.png)

For the Returns and Sales Tables, first rows were not headers and so resolved that by applying the "Use First row as header" action.
Sales Tables was used to extract fact table (Customers & Products)
column datatypes were validated appropriately , also removed unnecessary columns.

## Data Model Design
The data required for this analysis are located in various tables.
Therfore, appropriate modelling is required.
A star Schema is designed with the Revenue and Expenses Table representing the fact table containing all redundant data, and to which other dimension tables are modelled or connected to, using the column that is common. Date Table was created using CALENDARAUTO() Dax Function 
Revenue & Expenses Table has been modelled with:
- Revenue Table using the "Revenue Account ID"
- Expenses Table using the "Account ID"
- Date Table using the "Date"
- Product Table using "Product ID"
- Account Tables via "Account ID"
- AccountHeader Tables via "Header ID"

![model](DataModelling.png)


## Data Aanalysis/ Visualization
Analysis was done using simple visuals since the tables have been perfectly modelled together.
Applied some Dax Function to get the required information

## Revenue and Margin

![](Revenue_Margin.png)

#### Company had Operational revenue over than 9M dollars with Gross margin over than 4M dollars represent 42% of Operational revenue.
While the highest revenue and Gross margin achieved on November, January had the highest % gross margin with 42%.
#### Retail Team had the highest Revenue with over than 4M dollars. Can easily notice that Food Category contributed over than 3M dollars.
#### Although Two Brother Mill Supplier had the highest revenue and gross margin with over than 5M and 1M dollars respectively , Kappa Drinks had the 
highest % of gross Margin 56% due to imported wine with gross margin of 70%.

I then had to drill down the Supplier to know the exact Group with the highest % gross margin in Kappa Drinks.

![](Revenue_Margin_2.png)

With further visual analysis, It is interesting to create dynamic income statement in Power BI adding Vertical and Horizontal Analysis.

We can then Right click on "Category, Group, Product, Sales Person, Supervisor, Supplier or Team" to go to Order details
Here I Check  Two Brother Mill Supplier Order details.

![](OrderDetails.png)

## Income Statement
Income statement dashboard appear in Periods due to the largest width, However it's shown in one matrix same dashboard in actual project.

January To April            
:--------------------------:
![](IncomeStatement.png)     

April To July   
:--------------------------:
![](IncomeStatement2.png)  

July To October              
:--------------------------:
![](IncomeStatement3.png)     
 
October To Total
![](IncomeStatement4.png)

Hmmm! Now we can notice that January has the minimum cost of sales which cause the increasing in gross margin % in January than November
We should be careful while checking Month over Month Horizontal analysis "% MOM HA" in Cost of sales & Operating Expenses that the decresing ⬇️ (-) sign means
increasing in Cost of sales & Operating Expenses as they are in negative sign and they cause decreasing gross revenue and gross margin.
For example "% MOM HA" in Cost of sales in February Month equal -121% means that: 
   It increased in February by about 121% than January its goes up from (148,107) to (327,834).

Waterfall chart clear the Operating income by month, September had the highest operating income.

## Financial Simulation
Financial Simulation dashboard appear in Periods due to the largest width, However it's shown in one matrix same dashboard in actual project.

What if? analysis measure and evaluate the change in QTY, Unit Price, Cost and Expenses Factor and the effect on Operating Income.
by only moving the slicer on any factor and evaluate the effect on Operating Income.

January To April            
:--------------------------:
![](FinancialSimulation.png)

April To July   
:--------------------------:
![](FinancialSimulation2.png)  

July To October              
:--------------------------:
![](FinancialSimulation3.png)     
 
October To Total
![](FinancialSimulation4.png)


Here we can easily evaluate that effect of increasing QTY by 5% which cause incresing operating income by 9.26% with about $ 201K in Total due to:
   - Increasing in Revenue, Cost  by $ 484K, $ 283K respectively.

## Revenue Analysis
![](RevenueAnalysis.png)

Here is one of the most smart chart Decomposition Tree which give stackholder the applity to select any categorical features in any order on his point of view to check the 
Highest or Lowset revenue due to this feature.

On this dashboard I trace the cause of the highest revenue following this branches  
start with category and found that food is the highest about $9M.
Wheat Flours is the highest in group about $3M, Retail Team is the best contribute with about $1M in revenue 
Keep tracking and check supervesiors, found that Maci Pena superis had achieved the higest revenue with about $1M 
Great Now we reached that Shahid Duran is the best sales person Following this analysis. 

## % Gross Margin Analysis
Here is one of another smart chart which easily give stackholder the insights to know which Features influence Gross Margin to increase or decrease and by How much in %?
![](GrossMarginInfluencers.png)

Here we can find that Imported Wine to increase by about 27% on average 


## Conclusions/Recommendations
- **Wheat Flours** had the Highest  Revenue and sales.
- **Imported wine** had the highest % Gross Margin.
- **Recommend to studying the cross selling of Wheat Flours and Imported wine with the other products and make offers on the least product sales**.
------




###### My goal is to provide value to the stakeholders and not just to build reports and dashboard. 

Thank you.

