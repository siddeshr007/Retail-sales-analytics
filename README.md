# Retail Sales Analytics Project 
End-to-end analysis of the Sample Superstore dataset.

## Tech Stack
- Python (pandas, numpy, matplotlib)
- Jupyter Notebook (Anaconda)
- Git & GitHub
- Tableau (dashboard WIP)

## Dataset
- 9,994 orders from the Sample Superstore dataset  
- Columns include order details, customer, geography, product, sales, discount, and profit.

## Work Done
1. **Data cleaning**
   - Loaded raw Excel file.
   - Standardised column names to snake_case.
   - Converted `order_date` and `ship_date` to datetime.

2. **Feature engineering**
   - Created `order_year`, `order_month`, `order_dayofweek`.
   - Calculated `profit_margin = profit/sales`.

3. **EDA**
   - Sales & profit by category and region.
   - Monthly sales trends across years.
   - Visualisations using matplotlib.

4. **Outputs**
   - Cleaned dataset: `data/processed/superstore_clean.csv`
   - Full notebook: `notebooks/01_data_cleaning_eda.ipynb`
