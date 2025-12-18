# UCI Online Retail Dataset Guide

## Overview
The **UCI Online Retail Dataset** contains **real transactional data** from a UK-based online retailer, covering the period from **December 2010 to December 2011**.  
The company primarily sells **unique, all-occasion gift items**, and a significant portion of its customers are **wholesalers**.

Because real e-commerce transaction data is rarely public, this dataset is widely used for **data mining, customer analytics, and machine learning education**.

---

## Key Characteristics
- Real-world **transaction-level data**
- Covers **1 full year of sales activity**
- Mix of **retail and wholesale** customers
- Requires **significant data cleaning**
- Ideal for **unsupervised learning and business analytics**

---

## Dataset Structure
Each row represents a **single line item in a transaction**, not an entire order.

---

## Data Dictionary

| Column Name | Description |
|-------------|------------|
| `InvoiceNo` | Invoice number (identifies a transaction; cancellations start with `C`) |
| `StockCode` | Product (item) code |
| `Description` | Product description |
| `Quantity` | Number of units purchased (negative values indicate returns) |
| `InvoiceDate` | Date and time of the transaction |
| `UnitPrice` | Price per unit (GBP) |
| `CustomerID` | Unique customer identifier (missing for some records) |
| `Country` | Customer’s country |

---

## Important Data Notes
- **Cancellations and returns** are included (negative quantities)
- Some transactions have **missing CustomerID**
- Prices are in **British Pounds (GBP)**
- A single invoice can include **multiple products**
- Dataset is not pre-aggregated — all metrics must be derived

---

## Common Preprocessing Tasks
Students should expect to:
- Remove or handle canceled invoices
- Filter negative quantities (returns)
- Handle missing `CustomerID` values
- Convert timestamps and extract time features
- Create transaction-level aggregates

---

## Example Learning Use Cases

### Exploratory Data Analysis (EDA)
- Revenue trends over time
- Top-selling products and categories
- Country-level sales distribution

### Customer Analytics
- RFM analysis (Recency, Frequency, Monetary)
- Customer lifetime value (CLV) estimation
- Wholesale vs retail customer segmentation

### Unsupervised Learning
- Customer clustering (K-means, hierarchical clustering)
- Market basket analysis
- Product similarity analysis

### Time Series Analysis
- Daily or monthly sales forecasting
- Seasonality detection
- Impact of returns on revenue

---

## Example Questions to Explore
- Who are the most valuable customers?
- Which products are frequently returned?
- How does purchasing behavior differ by country?
- Can customers be segmented based on buying patterns?

---

## Attribution
Data provided by:
> **Dr. Daqing Chen**  
> Public Analytics Group  
> London South Bank University  
> UCI Machine Learning Repository

Dataset title on UCI: **“Online Retail”**

---

## Why This Dataset?
This dataset offers a rare opportunity to work with **真实 transactional e-commerce data**, making it ideal for:
- Business-focused data science exercises
- Customer segmentation and analytics
- End-to-end data cleaning and feature engineering practice

It closely mirrors the challenges faced in real commercial analytics projects.

