# A Guide to Brazilian E-Commerce Public Dataset by Olist
## Overview
This dataset contains **~100,000 real e-commerce orders** placed on the **Olist Store** between **2016–2018** across multiple Brazilian marketplaces.  
It is anonymized commercial data and is widely used for **data analytics, machine learning, and NLP** practice.

The dataset allows you to analyze the **full lifecycle of an order** — from purchase and payment to delivery, product details, and customer reviews.

---

## Key Characteristics
- Real-world, anonymized e-commerce data
- Orders may contain **multiple items**
- Items in the same order may come from **different sellers**
- Review text replaces company names with **Game of Thrones house names**
- Includes optional **geolocation data** (ZIP → latitude/longitude)

---

## Dataset Structure
The data is split into multiple relational tables.

### Core Tables

#### `olist_orders_dataset`
**Order-level information**
- `order_id` (PK)
- `customer_id`
- `order_status`
- `order_purchase_timestamp`
- Delivery-related timestamps

Use this table as the **starting point** for most analyses.

---

#### `olist_order_items_dataset`
**Line-item details per order**
- `order_id` (FK)
- `product_id`
- `seller_id`
- `price`
- `freight_value`

Used for **revenue, seller performance, and basket analysis**.

---

#### `olist_products_dataset`
**Product attributes**
- `product_id` (PK)
- `product_category_name`
- Physical dimensions and weight

Useful for **product analysis and feature engineering**.

---

#### `olist_customers_dataset`
**Customer location data**
- `customer_id` (PK)
- `customer_unique_id`
- `customer_zip_code_prefix`

Note: A single customer may place **multiple orders**.

---

#### `olist_order_reviews_dataset`
**Customer satisfaction**
- `review_id` (PK)
- `order_id` (FK)
- `review_score` (1–5)
- `review_comment_message`

Ideal for **sentiment analysis and NLP tasks**.

---

#### `olist_order_payments_dataset`
**Payment information**
- `order_id` (FK)
- `payment_type` (credit card, boleto, etc.)
- `payment_installments`
- `payment_value`

Used for **payment behavior and risk analysis**.

---

## How Tables Connect
- Join tables using `order_id`, `product_id`, or `customer_id`
- Typical workflow:
  1. Start with `olist_orders_dataset`
  2. Join items, payments, reviews
  3. Enrich with product and customer data

---

## Example Learning Tasks
### Data Analysis
- Revenue trends over time
- Average delivery delay by region
- Product category performance

### Machine Learning
- Predict review scores
- Forecast sales volume
- Classify late vs on-time deliveries

### NLP
- Sentiment analysis on review text
- Topic modeling of customer complaints

### Feature Engineering
- Delivery delay features
- Order complexity (number of items, sellers)
- Customer repeat purchase behavior

---

## Notes & Caveats
- Some orders have **no reviews**
- Canceled orders exist — filter by `order_status` where appropriate
- Text data is partially obfuscated (intentionally)

---

## Attribution
Dataset provided by **Olist**, Brazil’s largest department store for online marketplaces.  
Source: Kaggle — *Brazilian E-Commerce Public Dataset by Olist*

---