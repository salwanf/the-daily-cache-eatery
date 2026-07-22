# The Daily Cache Eatery - Data Pipeline & Analysis

### Description
This project builds a simple ETL pipeline to clean sales transaction data from a fictional casual restaurant, The Daily Cache Eatery, which contains messy data (inconsistent formats, missing values, invalid entries), then loads it into a relational PostgreSQL database and produces sales analysis visualizations.

### Project Flow
1. Extract - Read raw data from raw_orders.csv
2. Transform - Clean the data using Python (pandas):
   - Standardize mixed date formats (DD-MM-YYYY, DD/MM/YYYY, YYYY-MM-DD)
   - Handle missing values in the table and quantity columns
   - Standardize capitalization and whitespace in menu item names
   - Handle invalid data (negative quantities, unregistered table codes)
3. Load - Insert the cleaned data into a PostgreSQL database with a relational schema (tables: meja, menu, pesanan) using SQLAlchemy
4. Analyze - Run SQL queries to generate business insights

### Tech Stack
- Python (pandas, SQLAlchemy, matplotlib)
- PostgreSQL
- Jupyter Notebook
- DBeaver (database design and querying)

### Key Insights
- Kopi susu (milk coffee) and es teh (iced tea) are the highest-selling menu items by volume at The Daily Cache Eatery
- However, nasi goreng (fried rice) generates the highest revenue despite lower sales volume, due to its higher price per portion
- This highlights the importance of analyzing revenue, not just sales volume, in business decision-making

### Files
- data_pipeline_analysis.ipynb - Main notebook covering data cleaning, database loading, and analysis
- raw_orders.csv - Raw transaction data
- best_selling_items.png - Visualization of best-selling menu items by volume
- revenue_by_menu.png - Visualization of total revenue by menu item

### How to Run
1. Install dependencies: pip install pandas sqlalchemy psycopg2-binary matplotlib
2. Set up a PostgreSQL database and adjust the connection string in the notebook
3. Run all cells in the notebook sequentially
