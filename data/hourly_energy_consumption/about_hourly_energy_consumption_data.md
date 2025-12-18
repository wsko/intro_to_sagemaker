# PJM Hourly Energy Consumption Dataset

## Overview
The **PJM Hourly Energy Consumption Dataset** contains **hourly electricity demand (in megawatts)** for multiple regions operated by **PJM Interconnection LLC**, a regional transmission organization (RTO) in the United States.

PJM manages the electric transmission system across parts of the **Eastern Interconnection**, covering all or portions of:
Delaware, Illinois, Indiana, Kentucky, Maryland, Michigan, New Jersey, North Carolina, Ohio, Pennsylvania, Tennessee, Virginia, West Virginia, and Washington, DC.

This dataset is commonly used for **time series analysis, forecasting, and energy analytics**.

---

## Key Characteristics
- **Hourly time series data**
- Units: **Megawatts (MW)**
- Covers **multiple geographic regions**
- Region definitions **change over time**
- Contains **multiple tables** (one per region or regional grouping)
- Data sourced from **PJM’s public reports**

---

## Dataset Structure
The dataset is organized as **multiple tables**, typically one per PJM region (or load zone).

Each table follows a similar structure:
- Timestamp as the primary index
- One column representing electricity demand for that region

Not all regions have data for all time periods due to **organizational and boundary changes**.

---

## Data Dictionary (Typical Table)

| Column Name | Description |
|-------------|------------|
| `Datetime` | Hourly timestamp (local time) |
| `<REGION_NAME>` | Electricity consumption in MW for the region |

> Example region names may include: `PJM_Load`, `AEP`, `COMED`, `DAYTON`, `DOM`, `DUQ`, `EKPC`, `FE`, `NI`, `PJM_Midwest`, etc.

---

## Important Data Notes
- **Missing periods** are expected for some regions
- Daylight Saving Time transitions may create:
  - Duplicate hours
  - Missing hours
