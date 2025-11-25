# Retail Sales Analytics Project 
End-to-end analysis of the Sample Superstore dataset to understand sales and profitability by product, region, and customer segment.

🎯 Objective

Provide actionable insights on:
* Which categories/sub-categories drive the most revenue and profit
* Which regions and customer segments are most valuable
* How sales trend over time (seasonality, growth)
* Where profit margins are strong or weak

🧱 Project Structure

Retail-sales-analytics/
│
├── data/
│ ├── processed/
│ │ └── superstore_clean.csv # Cleaned & feature-engineered dataset
│ └── raw/
│ └── superstore_raw... # Original Excel file (not tracked on GitHub)
│
├── docs/
│ └── project_brief.md # Problem statement & findings (summary)
│
├── notebooks/
│ └── 01_data_cleaning_eda.ipynb # Jupyter notebook: cleaning + EDA
│
└── README.md # This file

🛠 Tech Stack

* Python: pandas, numpy, matplotlib
* Jupyter Notebook (Anaconda)
* Git & GitHub for version control
* Tableau (planned dashboard using superstore_clean.csv)

📊 Dataset

* ~9,994 orders from the Sample Superstore dataset

Key fields:
* Order details: order_id, order_date, ship_date, ship_mode
* Customer: customer_id, customer_name, segment
* Geography: country, city, state, postal_code, region
* Product: category, sub_category, product_name
* Metrics: sales, quantity, discount, profit

🔧 1. Data Cleaning

Performed in notebooks/01_data_cleaning_eda.ipynb.

Steps:
* Loaded raw Excel file using pandas.read_excel.
* Standardised column names:
  - Trimmed spaces
  - Converted to snake_case (e.g., Order Date → order_date).
* Converted date columns to datetime:
  - order_date
  - ship_date
* Verified missing values:
  - The dataset contains no nulls in key fields.

🧩 2. Feature Engineering

New fields created:
* order_year – year of the order
* order_month – year-month period (e.g. 2016-11)
* order_dayofweek – weekday name (e.g., Monday)
* profit_margin – profit/sales

These features are used for trend and profitability analysis and are saved in superstore_clean.csv.

🔍 3. Exploratory Data Analysis (EDA)

Key analyses in the notebook:
* Sales by Category
  - Compute total sales by category and rank them in descending order.
* Sales by Region
  - Compare Central, East, South, and West by total sales and profit.
* Monthly Sales Trend
  - Aggregate sales by order_month to see seasonality and growth.
* Profitability
  - Examine profit_margin alongside sales to identify high-revenue, low-margin areas.

Visuals include:
* Bar chart: total sales by category
* Line chart: monthly sales trend over time

💾 4. Outputs

* Processed dataset
  data/processed/superstore_clean.csv
    - Cleaned and feature-engineered, ready for Tableau / Power BI / SQL analysis.
* Notebook
  notebooks/01_data_cleaning_eda.ipynb
    - Contains full data cleaning, feature engineering, and EDA workflow.

📈 5. Planned Tableau Dashboard

Using data/processed/superstore_clean.csv, the planned dashboard will include:
* KPI Cards
  - Total Sales
  - Total Profit
  - Average Profit Margin
* Sales by Category & Sub-Category
  - Bar chart with colour by profit or profit margin.
* Sales by Region
  - Map or bar chart showing sales & profit by region.
* Monthly Sales Trend
  - Line chart of sales over time with filters for:
    - segment
    - category
* Filters / Slicers
  - Year
  - Region
  - Segment
  - Category

📌 How to Run Locally

* Clone the repo:
**git clone https://github.com/siddeshr007/Retail-sales-analytics.git
cd Retail-sales-analytics**

* Create environment & install dependencies (example with pip):
**python -m venv .venv
.\.venv\Scripts\activate         # Windows
pip install pandas numpy matplotlib jupyterlab openpyxl**

* Launch Jupyter:
**jupyter notebook**

* Open notebooks/01_data_cleaning_eda.ipynb and run all cells.

✍️ Author
Sai Siddesh Reddy Bynigeri
Business / Data Analyst – Python, SQL, Tableau, Excel
