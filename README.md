E-Commerce Data Cleaning and Analysis Pipeline ::

Overview  ::

This repository contains a Data Analysis and Preprocessing pipeline built using Python and Pandas in a Jupyter Notebook. 
The project processes raw e-commerce transaction data, performs comprehensive data cleaning, creates feature-engineered columns,
converts data types, and computes regional aggregation statistics.


1. Data Loading & Inspection Workspace Setup: 

Sets working directories dynamically using Python's os module.  

Dataset Import:     Imports raw transaction records (pd.csv) into a Pandas DataFrame.  

Integrity Auditing:  Inspects dataset dimensions (shape), missing values (isnull()), and duplicate records (duplicated()). 


2. Data Cleaning & ImputationDeduplication: 

Removes duplicate rows, reducing the total dataset to 1,000 unique records.  
Missing Value Imputation:Imputes missing discount values with 0.  
Replaces missing payment_method entries with an 'unknown' categorical tag.  
Fills missing customer_rating records using the median rating (4.0).  


3. Feature Engineering & Type ConversionDatetime Conversion: 

Standardizes date formats (signup_date, transaction_date) to datetime64 objects.  
Feature engineering::(gross_amount,discount_amount,final_amount)  

4. Group Aggregation & FilteringRegional Analysis:

Groups performance metrics (sum, min, max, mean, count) by region based on final_amount.  
Targeted Filtering: Filters regions based on revenue thresholds and transaction counts (identifying high-performing regions such as South and North).  

Libraries: 
Pandas, NumPy, OS  Environment: Jupyter Notebook 















