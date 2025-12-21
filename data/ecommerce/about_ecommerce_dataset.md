# Google TheLook E-Commerce Dataset

## Overview

This synthetic retail dataset** created by Google represents a fictitious online clothing retailer and is designed for **analytics, data science, and BI experimentation**.

The dataset captures the **end-to-end eCommerce lifecycle**, including:

* Users and demographics
* Products and inventory
* Orders and fulfillment
* Web events and sessions
* Logistics and distribution centers
* Digital traffic sources

---

## Availability & Access

* **Hosting platform:** Google BigQuery (Public Dataset)
* **Ideal for:** SQL analytics, BI dashboards, data engineering pipelines, ML feature engineering, and forecasting demos

---

## Dataset Structure

The dataset is organized into **seven relational tables**, closely mirroring a real-world eCommerce schema.

---

## 1. `distribution_centers.csv`

Information about logistics hubs that store and ship products.

| Column      | Description                                   |
| ----------- | --------------------------------------------- |
| `id`        | Unique identifier for the distribution center |
| `name`      | Distribution center name                      |
| `latitude`  | Latitude coordinate                           |
| `longitude` | Longitude coordinate                          |

**Use cases:**
Logistics optimization, shipping distance analysis, geospatial visualization.

---

## 2. `events.csv`

Web and user interaction events generated during browsing sessions.

| Column                         | Description                                   |
| ------------------------------ | --------------------------------------------- |
| `id`                           | Unique event identifier                       |
| `user_id`                      | Associated user                               |
| `sequence_number`              | Event order within session                    |
| `session_id`                   | Session identifier                            |
| `created_at`                   | Event timestamp                               |
| `ip_address`                   | Origin IP address                             |
| `city`, `state`, `postal_code` | Event location                                |
| `browser`                      | Browser used                                  |
| `traffic_source`               | Acquisition channel                           |
| `uri`                          | Page or resource accessed                     |
| `event_type`                   | Type of interaction (view, add-to-cart, etc.) |

**Use cases:**
Clickstream analysis, funnel modeling, session analytics, attribution modeling.

---

## 3. `inventory_items.csv`

Tracks individual inventory units and their product metadata.

| Column                           | Description             |
| -------------------------------- | ----------------------- |
| `id`                             | Inventory item ID       |
| `product_id`                     | Associated product      |
| `created_at`                     | Inventory creation date |
| `sold_at`                        | Sale timestamp          |
| `cost`                           | Item cost               |
| `product_category`               | Product category        |
| `product_name`                   | Product name            |
| `product_brand`                  | Brand                   |
| `product_retail_price`           | Retail price            |
| `product_department`             | Department              |
| `product_sku`                    | SKU                     |
| `product_distribution_center_id` | Distribution center     |

**Use cases:**
Inventory turnover, margin analysis, stock lifecycle modeling.

---

## 4. `order_items.csv`

Line-item–level view of purchased products.

| Column              | Description         |
| ------------------- | ------------------- |
| `id`                | Order item ID       |
| `order_id`          | Parent order        |
| `user_id`           | Purchasing user     |
| `product_id`        | Product purchased   |
| `inventory_item_id` | Inventory unit      |
| `status`            | Order item status   |
| `created_at`        | Order creation time |
| `shipped_at`        | Shipping timestamp  |
| `delivered_at`      | Delivery timestamp  |
| `returned_at`       | Return timestamp    |

**Use cases:**
Revenue analysis, returns modeling, fulfillment SLAs.

---

## 5. `orders.csv`

Order-level summary data.

| Column         | Description         |
| -------------- | ------------------- |
| `order_id`     | Unique order ID     |
| `user_id`      | Customer            |
| `status`       | Order status        |
| `gender`       | User gender         |
| `created_at`   | Order creation time |
| `returned_at`  | Return time         |
| `shipped_at`   | Shipping time       |
| `delivered_at` | Delivery time       |
| `num_of_item`  | Items per order     |

**Use cases:**
Order lifecycle analysis, cohort analysis, AOV calculation.

---

## 6. `products.csv`

Master catalog of products.

| Column                   | Description         |
| ------------------------ | ------------------- |
| `id`                     | Product ID          |
| `cost`                   | Product cost        |
| `category`               | Product category    |
| `name`                   | Product name        |
| `brand`                  | Brand               |
| `retail_price`           | Retail price        |
| `department`             | Department          |
| `sku`                    | SKU                 |
| `distribution_center_id` | Distribution center |

**Use cases:**
Product performance analysis, pricing strategy, assortment optimization.

---

## 7. `users.csv`

Customer profiles and demographics.

| Column                                    | Description           |
| ----------------------------------------- | --------------------- |
| `id`                                      | User ID               |
| `first_name`, `last_name`                 | User name             |
| `email`                                   | Email address         |
| `age`                                     | Age                   |
| `gender`                                  | Gender                |
| `street_address`                          | Address               |
| `city`, `state`, `postal_code`, `country` | Location              |
| `latitude`, `longitude`                   | Coordinates           |
| `traffic_source`                          | Acquisition channel   |
| `created_at`                              | Account creation time |

**Use cases:**
Customer segmentation, demographic analysis, LTV modeling.

---

## Entity Relationships (High-Level)

* **Users → Orders → Order Items → Products → Inventory Items**
* **Products & Inventory Items → Distribution Centers**
* **Users → Events (sessions & web activity)**

---

## Example Analytical Use Cases

### Geospatial Analysis

* User vs. distribution center proximity
* Regional demand and fulfillment efficiency

### User Behavior Analysis

* Session paths and funnels
* Traffic source performance
* Event-to-purchase conversion

### Sales & Revenue Analysis

* Revenue by category, brand, or department
* Profitability using cost vs. retail price
* Return rate analysis

### Product Performance

* Best-selling products
* Inventory aging and turnover
* Category-level demand trends

### User Demographics

* Customer segmentation
* Cohort and retention analysis
* Geographic distribution of users

### Order Fulfillment

* Shipping and delivery timelines
* Bottleneck identification
* Return behavior patterns
