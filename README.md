# 🛒 E-Commerce Sales Analysis — Bluemazon (2019)

## 📘 Overview
**Bluemazon** is a fictional e-commerce company selling electronic products.  
This project analyzes its **2019 sales data** to uncover trends, identify top-performing products, detect sales patterns, and generate actionable insights to boost revenue.

Using **Python, Pandas, Matplotlib, and Seaborn**, the project demonstrates strong data cleaning, exploratory data analysis (EDA), feature engineering, and visualization skills — all essential for a data analyst role.

---

## 🎯 Project Objectives
- Combine and clean **12 monthly sales CSV files** into one dataset.  
- Extract key time-based and location-based features: `Month`, `Hour`, and `City`.  
- Visualize trends to identify:
  - Top-selling products  
  - Peak sales hours  
  - Best-performing cities  
  - Monthly revenue patterns  
- Provide data-driven business insights and strategic recommendations.

---

## ⚙️ Tech Stack
| Tool | Purpose |
|------|----------|
| **Python** | Core programming language |
| **Pandas** | Data cleaning and manipulation |
| **Matplotlib** | Data visualization |
| **Seaborn** | Statistical plotting and heatmaps |
| **Jupyter Notebook / VS Code** | Analysis and visualization environment |

---

## 🧩 Dataset Information
The dataset contains **12 CSV files** (Jan–Dec 2019) with a total of **186,850 records**.  
Each file includes order-level details:

| Column | Description |
|---------|-------------|
| `Order ID` | Unique order identifier |
| `Product` | Product name |
| `Quantity Ordered` | Quantity of each product |
| `Price Each` | Unit price (USD) |
| `Order Date` | Timestamp of purchase |
| `Purchase Address` | Customer shipping address |

**New engineered columns:**
- `Month` — extracted from `Order Date`  
- `Hour` — extracted from `Order Date`  
- `City` — extracted from `Purchase Address`  
- `Sales` — computed as `Quantity Ordered × Price Each`

---

## 🧠 Data Processing Workflow

1. **Import & Merge**  
   Combined all monthly CSVs using `pandas.concat()`.  

2. **Clean Data**  
   - Removed null and duplicate entries  
   - Converted numerical and datetime columns to correct formats  

3. **Feature Engineering**  
   - Created new fields: `Month`, `Hour`, `City`, and `Sales`  
   - Extracted insights for time-based and geographical trends  

4. **Exploratory Data Analysis (EDA)**  
   - Univariate, bivariate, and multivariate visualizations  
   - Correlation heatmaps and revenue distribution charts  

---

## 📊 Data Analysis Highlights

### 1️⃣ Monthly Sales Trend
<img src="images/image3.png" width="500">
- **Highest revenue** observed in **December and October**.  
- **Seasonal pattern:** gradual increase from Jan–Apr, dip mid-year, sharp rise in Q4.  

---

### 2️⃣ City-Wise Sales
<img src="images/image2.png" width="500">
- **San Francisco (CA)** leads all cities with **$8.1M+** in total sales.  
- **Los Angeles (CA)** and **New York (NY)** follow closely.  

---

### 3️⃣ Sales by Hour (Rush Hour)
<img src="images/image4.png" width="500">
- Sales peak between **9 AM – 12 PM** and **7 PM – 9 PM**.  
- Indicates strong opportunities for **targeted ads or promotions** during these windows.  

---

### 4️⃣ Top-Selling Products
<img src="images/image5.png" width="500">
- Most sold items:  
  - **USB-C Charging Cable**  
  - **Bose SoundSport Headphones**  
  - **Lightning Charging Cable**  
- Average order size is **1–2 items**, confirming single-item purchase dominance.

---

## 💡 Business Insights & Recommendations

### 🧩 1. Product Bundling
- Frequently bought combinations:
  - Phone + Charging Cable  
  - Phone + Headphones  
  - Charging Cable + Headphones  
- Offer combo discounts to increase **average order value (AOV)**.

### ⏰ 2. Rush Hour Promotions
- Run ads during **morning (9–12)** and **evening (7–9)** peaks to maximize conversion rates.

### 🏙️ 3. Geographic Focus
- Maintain higher inventory and faster shipping in **San Francisco**, **Los Angeles**, and **New York** — these cities drive majority of revenue.

### 📦 4. Inventory Planning
- Allocate higher stock for **high-demand items** like charging cables and headphones.

---

## 📈 Summary of Results
| Metric | Value |
|---------|-------|
| Total Orders | 185,916 |
| Total Items Sold | 209,038 |
| Total Revenue | **$34,483,365.68 USD** |
| Peak Sales Month | December |
| Top City | San Francisco (CA) |
| Peak Hour | 19:00 – 21:00 |

---

## 🧰 Installation
Clone the repository and install required packages:

```bash
git clone https://github.com/<your-username>/Ecommerce-Sales-Analysis.git
cd Ecommerce-Sales-Analysis
pip install pandas matplotlib seaborn
