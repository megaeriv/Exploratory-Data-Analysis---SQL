# Exploratory-Data-Analysis---SQL

### Objective
Understand data created in data warehouse in my previoud project.
Here we would explore that data for analysis with different analytical techniques

### Datasets
CRM and ERP data used to create data in previous project :
  - https://github.com/megaeriv/Data-Engineering-Project-SQL-Data-Warehouse-from-Scratch

The best way to see data is Dimensions and measure, and this helps create the best analytical mindset when exploring data 
Classificattion
To properly classify the data, this questionheirachy is followed

IS DATA TYPE A NUMBER
  NO = Dimension (Qualitative)
  YES = Next question
    DOES IE MAKE SENSE TO AGRREGATE
    NO = DIMENSION
    YES = MEASURE

Examples: 
  - Category column from Product table `gold.dim_product` (it already known this is a dimesnion table)
  
  - Sales_amount column from Sales table `gold.fact_sales`(it is already known, this is a fact table)
    + This column is a number column and makes sesne to aggregate it  

    
