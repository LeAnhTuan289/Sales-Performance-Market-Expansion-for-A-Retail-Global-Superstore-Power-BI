# 🌍 Sales Performance & Market Expansion For A Global Superstore | Power BI

![image](https://github.com/user-attachments/assets/65df4f32-c787-4986-856f-49ef3f9034b6)

**Author:** Lê Anh Tuấn

**Tools Used:** Power BI

## Table of Contents
1. [📌 Background & Overview](#background--overview)
2. [📂 Dataset Description & Data Structure](#dataset-description--data-structure)
3. [🧠 Design Thinking Process](#design-thinking-process)
4. [📊 Key Insights & Visualizations](#key-insights--visualizations)
5. [🔎 Final Conclusion & Recommendation](#final-conclusion--recommendation)

---

## 📌 Background & Overview

**Objective:**

**📖 What is this project about?**

This project aims to build a **Power BI dashboard** using the *Global Superstore Sales* dataset, which includes data on transactions (**Orders**), sales representatives (**People**), and product returns (**Returns**).
The goal is to provide senior managers with **data-driven insights** to:

- **Understand current business performance**
 
- **Optimize market expansion strategies**

- **Identify strategic products for growth**

- **Support better decision-making to drive revenue and ROI**


**👤 Who is this project for?**

✔️ Data analysts & business analysts seeking actionable insights.

✔️ Marketing and sales teams focusing on product performance and market growth.

✔️ Route to market team aiming to improve distribution strategies and market reach.


**❓Business Questions:**

✔️ How is the business performing?

✔️ Which market should we expand?

✔️ Which products should be prioritized and which ones should be limited?


**🎯Project Outcome:**

- Revenue increased significantly, but profit margin remained flat, indicating rising costs and limited operational efficiency gains.  
- Canada emerged as a high-margin market (28%) despite low revenue, while Africa and EMEA showed the fastest YoY growth, revealing expansion potential.  
- Oceania and Africa attracted the most new customers, whereas most revenue still came from loyal, returning buyers.  
- Technology led revenue growth and profitability, but return rates in some tech SKUs (e.g., Cisco, Motorola) impacted margins.  
- Products like Copiers delivered the highest profit per unit, while low-performing items (e.g., Suppliers, Furnishings) diluted overall profitability.

By aligning regional and product strategies, senior managers can **scale in high-margin markets**, **invest in scalable profitable categories**, and **optimize acquisition and return management**, driving **sustainable long-term growth**.

## 📂 Dataset Description & Data Structure

### **📌 Data Source** 

- **Source**: Kaggle  
- **Size**: The **Orders** table contains **51,290** records.  
- **Format**: CSV  

### 📊 **Data Structure & Relationships**  

#### 1️⃣ **Tables Used:**  
The dataset consists of **three tables**:  

- 🛒 **Orders** – Contains detailed transaction and customer information (**51,290 records**).

<details>
<summary> <strong>Table 1: Orders</strong></summary>

| Column Name       | Data Type   | Description                              |
|------------------|------------|------------------------------------------|
| `Order ID`      | `VARCHAR`   | Unique identifier for each order.       |
| `Order Date`    | `DATE`      | Date when the order was placed.         |
| `Ship Date`     | `DATE`      | Date when the order was shipped.        |
| `Ship Mode`     | `VARCHAR`   | Shipping method used for delivery.      |
| `Customer ID`   | `VARCHAR`   | Unique identifier for each customer.    |
| `Customer Name` | `VARCHAR`   | Full name of the customer.              |
| `Segment`       | `VARCHAR`   | Customer segment (e.g., Consumer, Corporate). |
| `City`         | `VARCHAR`   | City where the order was placed.        |
| `State`        | `VARCHAR`   | State where the order was placed.       |
| `Country`      | `VARCHAR`   | Country where the order was placed.     |
| `Postal Code`  | `VARCHAR`   | Postal code of the shipping address.    |
| `Market`       | `VARCHAR`   | Market region (e.g., APAC, EMEA).       |
| `Region`       | `VARCHAR`   | Geographical region of the order.       |
| `Product ID`   | `VARCHAR`   | Unique identifier for each product.     |
| `Category`     | `VARCHAR`   | Product category (e.g., Furniture, Office Supplies). |
| `Sub-Category` | `VARCHAR`   | Sub-category of the product.            |
| `Product Name` | `VARCHAR`   | Name of the product ordered.            |
| `Sales`        | `DECIMAL`   | Revenue generated from the order.       |
| `Quantity`     | `INT`       | Number of items ordered.                |
| `Profit`       | `DECIMAL`   | Profit earned from the order.           |

</details>

- 🔄 **Returns** – Stores data on returned orders.

<details>
<summary> <strong>Table 2: Returns</strong></summary>

| Column Name  | Data Type | Description |
|--------------|-----------|-------------|
| `Returned`   | `VARCHAR` | Indicates whether the order was returned (e.g., 'Yes' or 'No'). |
| `Order ID`   | `VARCHAR` | Unique identifier for each order. |

</details>
  
- 👥 **People** – Holds information about sales representatives.

<details>
<summary> <strong>Table 3: People</strong></summary>

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| `Person`    | `VARCHAR` | Name of the salesperson. |
| `Region`    | `VARCHAR` | Geographic region where the salesperson operates. |

</details>

#### 2️⃣ Data Relationships:

![Image](https://github.com/user-attachments/assets/ea814a90-0f20-4b7d-9cb1-929e79163978)

| **From Table** | **To Table** | **Join Key**   | **Relationship Type**                                  |
|------------|----------|------------|----------------------------------------------------|
| `Orders`   | `People` | `Region`   | Many-to-One (multiple orders belong to one region) |
| `Orders`   | `Returns`| `Order ID` | One-to-One or Left Join (not all orders are returned) |

## 🧠 Design Thinking Process

### 1️⃣ Empathize

![Image](https://github.com/LeAnhTuan289/Sales-Performance-Market-Expansion-for-A-Retail-Global-Superstore-Power-BI/blob/0ad42c69b65a90da96361a4bef98dcc26ac41f1c/documents/5W1H_Decision_Framework.png)

![Image](https://github.com/LeAnhTuan289/Sales-Performance-Market-Expansion-for-A-Retail-Global-Superstore-Power-BI/blob/0ad42c69b65a90da96361a4bef98dcc26ac41f1c/documents/Empathy_Map_Stakeholder_Needs.png)

### 2️⃣ Define point of view 

![Image](https://github.com/LeAnhTuan289/Sales-Performance-Market-Expansion-for-A-Retail-Global-Superstore-Power-BI/blob/0ad42c69b65a90da96361a4bef98dcc26ac41f1c/documents/Define_POV_NorthStar_Mapping.png)

This part is in the dashboard

## 📊 Key Insights & Visualizations

### 🔍 Dashboard Preview

This dashboard is designed for Senior Managers to monitor global business performance, identify potential markets for expansion, and select strategic products for future growth.  
The analysis focuses not only on revenue performance, but also on profitability quality, market potential, and product-level risk.

---

## I. Business Overview

![Image](https://github.com/LeAnhTuan289/Sales-Performance-Market-Expansion-for-A-Retail-Global-Superstore-Power-BI/blob/0ad42c69b65a90da96361a4bef98dcc26ac41f1c/documents/db1.png)

### 📌 Key Findings

**1. Revenue and Profit increased steadily from 2011 to 2014, showing that the company is expanding in scale.**  
The yearly trend shows consistent growth in both revenue and profit. This indicates that the company has strong business momentum and enough scale to consider further market expansion.

**2. Profit Margin improved until 2013 but slightly declined in 2014, signaling that profitability efficiency is not continuously improving.**  
Although revenue continued to grow, margin did not keep increasing. This suggests that the company should not evaluate growth only by sales volume, but also by the quality of profit generated.

**3. Order volume increased consistently while Return Rate decreased in 2014.**  
The company is scaling order volume without creating a major return issue at the overall level. This indicates that operational performance remains relatively stable during growth.

**4. Technology is the strongest category because it combines high revenue with the highest profit margin among major categories.**  
Technology contributes strongly to both revenue and profit, making it the best candidate for strategic product investment.

**5. Furniture generates large revenue but has weak profitability.**  
Furniture has a much lower profit margin than Technology and Office Supplies. This means the company should avoid scaling Furniture aggressively before fixing low-margin sub-categories.

### 💡 Recommendation

The company should continue expanding, but future growth should prioritize **profit quality**, not only revenue growth. Senior Managers should focus investment on high-margin categories such as **Technology**, while reviewing low-margin areas such as **Furniture**, especially products that negatively affect profitability.

---

## II. Market Analysis

![Image](https://github.com/LeAnhTuan289/Sales-Performance-Market-Expansion-for-A-Retail-Global-Superstore-Power-BI/blob/0ad42c69b65a90da96361a4bef98dcc26ac41f1c/documents/db2.png)

### 📌 Key Findings

**1. APAC and EU are the core markets because they generate the largest revenue and profit contribution.**  
These two markets are the current business foundation of the company. Any strategic decision should protect and strengthen performance in these regions first.

**2. Canada has the highest Profit Margin but a very small revenue base.**  
Canada is not yet a core market by revenue, but its high profitability shows strong potential as a niche expansion market if the company can scale carefully.

**3. US and LATAM generate high revenue but only moderate profitability.**  
These markets are commercially important, but they require margin optimization before receiving aggressive expansion investment.

**4. EMEA has the weakest profitability among markets.**  
EMEA has low revenue and the lowest profit margin, making it a low-priority market for major expansion. The company should diagnose the causes of poor profitability before investing more.

**5. Top revenue countries are not automatically the best expansion targets.**  
United States, Australia, France, China, and Germany are the largest revenue countries. However, expansion decisions should also consider Profit Margin and growth quality, not revenue ranking alone.

### 💡 Recommendation

APAC and EU should remain the company’s core investment markets. Canada should be tested as a controlled high-margin expansion opportunity. US and LATAM should focus on margin improvement, while EMEA should be treated as a low-priority market until profitability improves.

---

## III. Product Analysis

![Image](https://github.com/LeAnhTuan289/Sales-Performance-Market-Expansion-for-A-Retail-Global-Superstore-Power-BI/blob/0ad42c69b65a90da96361a4bef98dcc26ac41f1c/documents/db3.png)

### 📌 Key Findings

**1. Phones and Copiers are the strongest candidates for strategic products.**  
Phones show strong demand and high revenue, while Copiers generate strong profit and high margin. Together, they support both revenue growth and profitability improvement.

**2. Technology is the best strategic category overall.**  
Technology outperforms other categories by combining scale and profitability. It should be the main focus for product strategy, marketing, inventory planning, and sales enablement.

**3. Tables is the most critical loss-making sub-category.**  
Tables generate sizable revenue but negative profit across multiple major markets. This is a clear profitability risk and should not be scaled further without corrective action.

**4. Office Supplies is a stable supporting category.**  
Office Supplies has healthy profitability and can support repeat purchases, bundling, and customer retention strategies.

**5. Furniture should be optimized rather than aggressively expanded.**  
Furniture has high revenue but weak margin, mainly due to poor-performing sub-categories such as Tables. Scaling Furniture without fixing margin issues may reduce overall profitability.

### 💡 Recommendation

The company should prioritize **Phones and Copiers** as strategic products. **Technology** should receive more investment in marketing, inventory, and sales focus. **Tables** should be reviewed immediately in terms of pricing, discounting, cost structure, and logistics. **Office Supplies** should be used as a supporting category for cross-selling and customer retention.

---

## IV . Insight & Recommendation

![Image](https://github.com/LeAnhTuan289/Sales-Performance-Market-Expansion-for-A-Retail-Global-Superstore-Power-BI/blob/613175ac4b1ca8ff214ad7f6972f44ffff9033a0/documents/Screenshot%202026-07-02%20103518.png)
