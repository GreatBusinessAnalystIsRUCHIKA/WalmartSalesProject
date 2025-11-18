**Walmart Sales Data Analysis — SQL + Exploratory Insights**

This project explores Walmart Sales data to uncover insights about branch performance, product trends, customer behavior, and revenue drivers.
Using SQL Server, the project performs data wrangling, feature engineering, and exploratory data analysis (EDA) to answer real business questions that help optimize sales strategies and profitability.

**🛒 About the Dataset**
The dataset comes from the Kaggle Walmart Sales Forecasting Competition, containing sales transactions from three Walmart branches located in:
Mandalay
Yangon
Naypyitaw
**
**📊 Dataset size: 1000 rows, 17 columns**

**📌 Column Overview****
| Column                  | Description                  | Data Type     |
| ----------------------- | ---------------------------- | ------------- |
| invoice_id              | Unique invoice number        | VARCHAR(30)   |
| branch                  | Walmart branch (A, B, C)     | VARCHAR(5)    |
| city                    | Location of the branch       | VARCHAR(30)   |
| customer_type           | Member / Normal              | VARCHAR(30)   |
| gender                  | Customer gender              | VARCHAR(10)   |
| product_line            | Category of product          | VARCHAR(100)  |
| unit_price              | Price per unit               | DECIMAL(10,2) |
| quantity                | Units purchased              | INT           |
| VAT                     | Value-added tax              | FLOAT         |
| total                   | Gross sales                  | DECIMAL(10,2) |
| date                    | Date of purchase             | DATE          |
| time                    | Time of purchase             | TIME          |
| payment_method          | Cash / Ewallet / Credit card | VARCHAR(30)   |
| cogs                    | Cost of goods sold           | DECIMAL(10,2) |
| gross_margin_percentage | Gross margin %               | FLOAT         |
| gross_income            | Gross income                 | DECIMAL(10,2) |
| rating                  | Customer rating              | FLOAT         |

⚙️ **Approach & Methodology**
1️⃣** Data Wrangling**
Loaded raw CSV into SQL Server
Created database and tables
Set NOT NULL constraints to remove null values
Checked for duplicates, invalid data types, inconsistencies

2️⃣ Feature Engineering

New fields were created to support deeper analysis:
🕒 Time of Day Classification
Morning
Afternoon
Evening
📅 Day of Week Extraction
To understand weekday performance.
🗓️ Month Name Extraction
To identify monthly revenue patterns.
Additional features added (optional for you to include):
➡️ Revenue per product line
➡️ Profit margin category (High/Medium/Low)
➡️ Customer frequency category (New / Returning)

3️⃣ Exploratory Data Analysis (EDA)

Using SQL Server, the following insights were extracted:
Product Analysis
Most popular product lines
Highest revenue-generating categories
VAT impact per product line
Product performance rating
Sales Analysis
Monthly revenue trends
Branch performance comparison

Time-of-day sales distribution
Holiday vs non-holiday effects
Weekday revenue (excluding Saturday & Sunday)
Customer Analysis
Customer type segmentation (Member vs Normal)
Gender-based purchasing patterns
Most profitable customer groups
Rating behavior by gender & branch

**🎯 Business Questions Answered

How many unique cities does the data have?
Which branch belongs to which city?

Product
Number of product lines
Most common payment method
Top-selling product line
Monthly revenue
Product line with highest VAT
Product lines marked as Good or Bad based on sales above/below average
Average rating per product line
Branch with sales above average sales

Sales
Sales made during morning/afternoon/evening per weekday
Customer type contributing most revenue
City with highest VAT %
Customer type paying the highest VAT

Customer
Unique customer types
Payment method distribution
Gender distribution per branch
Peak rating time of day
High rating weekday
Ratings per branch

