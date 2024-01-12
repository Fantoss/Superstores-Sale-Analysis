# Superstores Sales Analysis

### Project Overview
This data analysis project objective is to provide insights into the sales performance of United States of American Superstores between 2014-2017. By analyzing aspect of the sales data, we intent to identify sales patterns, make data driven recommendation and gain in depth understanding of the company performance. 

### Data Source
Sales data: This primary dataset used for this analysis is "sales_data.xlsx" file, containing detailed information.
[download here](https://www.kaggle.com/datasets/juhi1994/superstore)

### Tools
- Excel- Data cleaning
- Power BI- Data Analysis, Creating reports and Dashboard

### Data cleaning/Preparation

In preparation the following tasks was performed:
- data file converted from CVS to xlsx
- data loading and inspection
- Handling missing values and unwanted datapoints
- Remove duplicates, outliers and errors
- Perform ETL operations

### Exploratory Data Analysis

EDA means exploring the sales data to answer key questions, such as:

- How much profit is gained for each product?
- Top 10 customer by profits
- Which customer is regular/loyal over the years?
- Products having high discount rate?

#### Data Analysis

``` Power BI DAX

four-Year Customer = 
IF (
    CALCULATE (
        DISTINCTCOUNT('Orders'[Order ID]),
        FILTER ('Orders', 'Orders'[Customer ID] = EARLIER ('Orders'[Customer ID]) && YEAR('Orders'[Order Date]) >= 2014 && YEAR('Orders'[Order Date]) <= 2017)
    ) = 4,
    "Yes",
    "No"
)

``` Power BI DAX

Total_Rev = SUM(Orders[Sales])

``` Power BI DAX
Customers = DISTINCTCOUNT(Orders[Customer ID])

```
### Exploratory Data Analysis

Analysis results are summarised as follows:
The company profits have been steadily increasing over the past years with an obvious value in 2017. Product categoery Technology is the best performing in terms of profits while sub-category phones as highest revenue by segment.
Product category Furniture should be focused for promotion and marketing.
