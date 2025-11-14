
# Exploratory-Data-Analysis---SQL

### Objective
Understand data created in data warehouse in my previoud project.
Here we would explore that data for analysis with different analytical techniques

### Datasets
CRM and ERP data used to create data in previous project :  
https://github.com/megaeriv/Data-Engineering-Project-SQL-Data-Warehouse-from-Scratch

### Data Classificattion
The best way to see data is Dimensions and measure, and this helps create the best analytical mindset when exploring data  
- Measures to quantify the data  
- Dimensions to group the data  

To properly classify the data, this question heirachy is followed:

IS DATA TYPE A NUMBER  
NO = Dimension (Qualitative)  
YES = Next question  
  
DOES It MAKE SENSE TO AGRREGATE  
NO = DIMENSION  
YES = MEASURE

> [!NOTE]
> **Age** derived from birthdate column is a Measure  
> **ID** can be numeric but does not makes sense to aggreagte as are unique values so it is a dimension

Examples: 
  - Category column from Product table `gold.dim_product` (it is already known this is a dimesnion table)
  
  - Sales_amount column from Sales table `gold.fact_sales`(it is already known, this is a fact table)
    This column is a number column and makes sesne to aggregate it

---

## Exploration
The Data exploration would be done in 6 steps namely:
* Database Exploration 🔍
* Dimension Exporation 🔡
* Date Exploration 📅
* Measures Exploration 🔢
* Magnitude Analysis 📊
* Ranking ↘️


### 1. Database Exploration 🔍
Here Exploration would be done on the databse using INFORMATION_SCHEMA to explore all tables and columns of specific tables in the gold layer of medallion warehouse structure

### 2. Dimension Exporation 🔡
Here, the main objective is to identify the Unique values or Cateogires in each dimension using DISTINCT.  
This helps to recognize how data might be grouped or segmented which is useful for later anaysis e.g country, category

### 3. Date Exploration 📅
This uniques set of dimesnion date is explore to see the boundaries and time span. i.e earliest, latest

### 4. Measures Exploration 🔢
This is for calcultating the key metrics of our businessm , the highest levels of aggregations of measures in the datset  
e.g sum sales, average price, sum of quantity

### 5. Magnitude Analysis 📊
This is all about comparing measure values across different dimensions (e.g categories). It helps us understand the importance of different dimensions. 1.e aggragtion of measure by dimension  
Example: Average price by product

### 6. Ranking ↘️
This is very basic, just ordering of dimensions by measure, ranking dimensions by measures. e,g bottom three(3) customers  
by orders
