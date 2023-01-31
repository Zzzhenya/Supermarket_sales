# Supermarket_data
Explorative analysis of a supermarket sales data set from Kaggel

## Source
https://www.kaggle.com/datasets/aungpyaeap/supermarket-sales

## Tools

* Jupyter Lab

* Python ( Pandas, Numpy, Seaborn, Matplotlib )

* Xmind

## Data Columns
![](Columns.png)

## Equations

cogs = Unit price * Quantity

Tax 5% = cogs * 5/ 100

Total = cogs + Tax 5%

gross income = Total * gross margin percentage/ 100

All products have the same gross margin percentage

## Conclusions

### 1. Does products of the same product line have the same unit price?

* Products of the same product line have different prices. >> One product line does not represent one product.

* Since each invoice only has one unit price, all extracted invoices are of monotypic product sales.

* In the selected dataset 99% of the products have unique unit prices. Only 1% are repeated prices.

* Since most items have unique unit prices one could say for each unique product most of the time (99% of the time)only one invoice was extracted from sales of that specific product.

* There is a possibility that all* of the products in the dataset are unique and the 1% of the time where the unit price is repeated may be due to more than one product bearing the same price.*

** Maybe this dataset is a subset of all the sales made at each store.

** i.e.: For each store, extract one invoice where the customer bought only one type of product( Qty can be many) and product unit price is unique.

#### Extension

* Each record is unique to a combination of;
    
    "Product line","Unit price","Branch","Payment","Gender" or
    
    "Product line","Unit price","Branch","Payment","Customer type"

###  2. Which City/ Branch sold the highest quantity of products?

* Sales quantities are almost equally divided among the three cities/branches.

### 3. Which City/Branch earned the highest gross income?

* Total gross income is also almost equal in the three cities/branches.

* Only Naypyitaw has a slight increase of ~208 (1%)

### 4. What is the gross income by product line ?

* Gross income percentage of each product line is around 17%

* "Health and beauty" is considerably below average (15%)

### 5. What is the gross income by product line by City/Branch?

* Both total gross income and the percentage gross income of each product line when isolated by the city shows a considerable variance. 

** Might be a good parameter to explore later

### 6. What is the Total revenue by payment type?

* There is relatively low amount of credit card revenue compared to Ewallet and Cash. About 3% less

* Mandalay has highest revenue through credit card payments. This is only a small increased relative to the other payment methods. Lowest in Mandalay is Ewallet.

* Naypytiw has highest revenue through cash payments. This is significantly higher than other methods.The lowest method of revenue in Naypyitaw is through credit card.

* Yangon has highest revenue through Ewallet. The other methods seem to have relatively equi amounts.

### 7. Are men more likely to purchase high price low quantity products?

When average quantity and average unit price is considered against gender for all records;

* Average sales quantity by females is slightly higher than males, a difference of just 0.43

* Average unit price of sales by males is slightly higher than females, a difference of just 0.82

When average quantity and average unit price is considered against gender for records grouped by cities/supermarket branches;

* The differences are more visible. eg: In Naypyitaw average sales quantity has a considerable gap between males and females. (0.68, compared to 0.43 overall value)

* Some cities show opposite patterns to overall pattern. eg: In Yangon average unit price sales by females is higher than males.

### 8. Revenue fluctuation over time (datetime)

* Because of the fixed tax rate and lack of margine the fluctuation patterns of daily sum of gross income and daily sum of invoice total trends are similarly shaped.

* Daily sum of gross income might be an interesting field to analyze further because of the fluctuations.

* Overall cumulative gross income as well as cumulative gross income of each city show a trend of linear steady increase.

### 9. When (time, month, day) are people more likely to make purchases? Higher revenue

Day of Week

* The supermarket sales occuer all 7 days of the week at all three locations.

* When considering total gross income by day of the week,the highest total revenue was made on Saturday, closely followed by Tuesday.

* The lowest total revenue was made on Monday 

Day of Week by City

    * Lowest sales for Mandalay is Sunday

    * Lowest sales for Naypyitaw is Monday

    * Lowest sales for Yangon is Wednesday

    * Highest sales for Mandalay is Saturday

    * Highest sales for Naypyitaw is Saturday

    * Highest sales for Yangon is Sunday


* Because of this it is hard to generaize a particular day of week as the day with highest or lowest revenue.

* One must also consider that this dataset is not a raw dataset and is already cleaned to be balanced for an unknown analysis.

Hour of Day

* When considering total gross income of all three supermarkets by the hour of day, 19th hour is the highest and the 20th hour is the lowest.

When considering the total income by the hour of day of each supermarket seperately;

* For some reason Mandalay has a significanly low total gross income in the 16th hour (4 - 4.59 PM).
This is the lowest total gross income for any hour of all three cities.

* Mandalay also has a significantly high total gross income in the 19th hour ( 7 - 8 PM).
This is the highest total gross income for any hour of all three cities.
