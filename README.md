# global_sales_powerbi_analytics
An enterprise-grade Power BI dashboard transforming multi-table commercial sales data into interactive business insights.

<img width="623" height="337" alt="Global Sales" src="https://github.com/user-attachments/assets/39dedaf6-0ee5-4753-b60e-5b0a609d708c" />


## 🛠️ Technical Workflow & Architecture

### 1. Data Extract, Transform, & Load (ETL)
Using Power Query, the raw datasets underwent rigorous cleaning and structural optimization:
* **Data Type Enforcement:** Explicitly converted dates, geographic attributes, and financial metrics to appropriate schemas (`Date`, `Text`, `Fixed Decimal/Currency`).
* **Data Cleansing:** Standardized lowercase categorical entries, addressed missing records, and optimized column tracking to minimize the data model's memory footprint.

### 2. Relational Data Modeling
Rather than relying on a single flat table, this solution implements a structured schema by separating the dataset into logical entities:
* **Fact Table:** Transactional sales records containing key performance indicators (`total_price`, `quantity`, dates).
* **Dimension Tables:** Segmented tables for `Products`, `Orders`, and geographic data to allow for clean filtering across multiple granularities.

### 3. UI/UX & Dashboard Design System
A heavy emphasis was placed on dashboard readability, scannability, and corporate formatting standards:
* **Grid Symmetry:** Leveraged canvas alignment properties to ensure identical chart proportions and balance across visual rows.
* **Clutter Reduction:** Eliminated redundant default axis titles to maximize data ink ratio.
* **Typography & Axis Layouts:** Angled horizontal date strings for seamless chronological scanning and applied clean data labels (`M` for Millions, `K` for Thousands).

---

## 📈 Visual Architecture Breakdown

* **Total Sales by Country (Horizontal Bar Chart):** Provides instant geographical performance benchmarking.
* **Units Sold by Category (Donut Chart):** Visualizes the structural volume distribution across key inventory segments.
* **Revenue Breakdown by Category (Funnel Chart):** Tracks the progressive monetary value contribution per product category.
* **Monthly Sales Trend (Line Chart):** Captures fiscal seasonality and macro-level revenue trajectory over the year.
* **Weekly Revenue Trends (Multi Line Chart & Slicer):** Offers operational deep dives by mapping daily city performance against a dynamic weekday filter.

---

## 🚀 How to Interact with this Project
1. **Static Preview:** View the crisp, full-screen dashboard capture (`dashboard_preview.png`) located in the root directory.
2. **Native Exploration:** Clone this repository and open the `sales_analytics.pbix` file locally in Power BI Desktop to test the fully interactive slicers and cross-filtering behaviors.
