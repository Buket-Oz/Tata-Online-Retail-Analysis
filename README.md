# **Tata Online Retail **
**Analysis of Online Retail Transactions** focusing on **revenue trends, demand insights, and market expansion opportunities**, with **data cleaning, exploratory analysis, and interactive visualizations in Tableau**.

---

## **Background & Overview**

Tata's online retail business processes thousands of transactions annually across multiple international markets. This analysis aims to provide **data-driven insights** on **revenue trends, demand fluctuations, and customer purchasing behaviors** to support **strategic decision-making** for both **business growth and operational efficiency**.

### **Key Business Questions**

#### **For the CEO:**
1️⃣ How does revenue fluctuate throughout the year?  
2️⃣ Which regions have the highest demand for Tata’s products?  

#### **For the CMO:**
3️⃣ Which countries generate the highest revenue and quantity sold?  
4️⃣ Who are the top revenue-generating customers?  

---


## **Data Structure & Initial Checks**

The dataset consists of **online retail transaction records from 2010 and 2011**, including:

- **Product details** (Descriptions, Stock Code)  
- **Sales metrics** (Quantity, Unit Prices)  
- **Customer Information** (Customer ID, Country)  
- **Invoice Data** (Invoice Number, Date)  

**Final cleaned dataset shape:** **514,376 rows, 8 columns**  

**Data Cleaning & Exploratory Analysis** was performed in **Python (pandas, NumPy, Matplotlib, Seaborn)** to ensure data quality before analysis.  

📄 [Data Cleaning and EDA report](https://docs.google.com/document/d/1py6YwCyPSPAOKS8F337LnPJDdcFFgOQfSIt2tN-Gxpc/edit?usp=sharing)
📜 **[Python Script for Data Cleaning & EDA](./data_cleaning_eda.py)**


---


## **Executive Summary: Key Findings**

This analysis identifies **revenue trends, high-value markets, and customer segments** that can drive future growth. 

### **Revenue Trends**
- **Peak revenue in November (~$1M)** possibly driven by **Black Friday and early holiday shopping.**  
- **December revenue drop (~$370K)** suggests **demand shifts earlier in Q4.**  

### **Market-Specific Demand Patterns (Top 10 Countries)**
- **Netherlands, France, Germany, and Ireland** account for **~9% of total revenue**, with **both high sales volume and strong demand.**  
- **Australia, Spain, Switzerland, Belgium, Portugal, and Norway** contribute **~3% of total revenue** with **steady market demand and lower sales volume.**  
- **Ireland & Australia have higher revenue per unit, while France & Belgium are more volume-driven.**  

### **Customer Insights**
- **Top 10 customers contribute ~9% of total revenue.**  
- **Frequent buyers ≠ highest spenders**, indicating a **need for separate engagement strategies.**

### **Regional Demand & Expansion Opportunities**
- **Western Europe & Australia dominate in total quantity sold, highlighting strong regional demand.**  
- **Netherlands, Germany, France, Ireland, and Australia are key markets driving high product demand.**  


![Screenshot 2025-02-05 at 16 32 23](https://github.com/user-attachments/assets/52554a36-2ebd-415a-8904-e407a2d323c3)

📊 [Tableau Performance DashBoard](https://public.tableau.com/authoring/TataOnlineRetail-Dashboard/PerformanceDashboard#1)

---

## **Insights Deep Dive & Recommendations**

### **1️⃣ Revenue Performance & Seasonal Demand**
- **Revenue peaked in November (~$1M) but dropped significantly in December (~$370K).**  
- **Most markets peak in Q4, but Australia has an entirely different pattern—its strongest months are June & August.**  

✔ **Optimize Q4 promotions** by launching earlier to maintain post-November revenue.  
✔ **Adjust marketing efforts per country** to match **localized seasonal demand cycles.**  

![Screenshot 2025-02-05 at 16 34 36](https://github.com/user-attachments/assets/c927f2f6-d87f-43f5-b3e2-05ff601f149d)



---

### **2️⃣ Market-Specific Demand Patterns**
- **Two distinct market categories** emerged among the top 10 revenue-generating countries:  

  ✔ **High Revenue & Quantity** – Netherlands, France, Germany, and Ireland show **both strong demand and high sales volume.**  
  ✔ **Moderate Revenue & Quantity** – Australia, Spain, Switzerland, Belgium, Portugal, and Norway have **steady demand but lower total sales volume.**  

✔ **Premium Markets (Ireland, Australia):** Prioritize **high-value product promotions** to maximize per-unit revenue.  
✔ **Volume-Driven Markets (France, Belgium, Norway):** Implement **pricing optimization & bundling strategies** to boost per-unit revenue. 

![Screenshot 2025-02-05 at 16 34 17](https://github.com/user-attachments/assets/b11722b5-032f-4c58-9c05-12eb4f3df9a1)


---

### **3️⃣ High-Value Customers & Retention**
- **Top 10 customers contribute ~9% of total revenue, making retention essential.**  
- **A small customer base accounts for a significant portion of sales, reinforcing the need for loyalty strategies.**  

✔ **Develop a VIP loyalty program** with **exclusive offers and premium customer support.**  
✔ **Use personalized marketing** (email campaigns, early access deals) to **increase repeat purchases.**  

---

### **4️⃣ Expansion Strategy: High-Demand Regions**
- **Western Europe & Australia lead in total quantity sold**, signaling **strong regional demand.**  
- **Localized fulfillment strategies could optimize costs and logistics.**  

✔ **Invest in regional warehousing & delivery solutions** to **reduce shipping costs & delivery times.**  
✔ **Adapt supply chain strategies** for **high-volume international markets.**  

---

## **Key Takeaways & Next Steps**
✅ **Launch region-specific promotions** before peak seasons rather than relying on a **one-size-fits-all** approach.  
✅ **Differentiate marketing & pricing strategies** between **premium** and **volume-driven** markets.  
✅ **Strengthen high-value customer retention** through loyalty programs and personalized engagement.  
✅ **Optimize logistics in high-demand regions** to **reduce costs & increase efficiency.**  

---

This revision **removes unnecessary repetition, improves readability, and ensures clarity**, while **maintaining all key insights and recommendations in a structured flow.** 🚀

---

## **Next Steps & Future Analysis**
**Deeper Analysis of Country-Specific Peak Times** – Understanding what drives demand spikes (holiday impact, weather, local events).  

**Product Preferences by Country** – Identifying which product categories contribute the most to revenue in different regions.  

**Customer Segmentation for Retention Strategies** – Differentiating high-value customers from frequent buyers to optimize marketing.  

**Comparison of October vs. November Revenue Spikes** – Understanding why revenue spikes in October when excluding the UK.  

**Effectiveness of Black Friday & Seasonal Promotions** – Analyzing whether sales shift earlier in Q4 due to promotions.  

**Opportunities for Post-Black Friday Sales Recovery** – Investigating strategies to sustain December revenue instead of seeing a drop.  

---

## **Assumptions & Caveats**  

⚠️ **Unspecified Country Data** – Some transactions had `"Unspecified"` locations but **valid revenue data**, so they were **retained** to prevent revenue loss.  

⚠️ **Missing Customer IDs** – Some transactions lacked **Customer IDs** (guest checkouts or missing data) but were included in revenue calculations.  

⚠️ **Exclusion of Returns & Negative Transactions** – **All negative quantities or zero-priced transactions were removed** to ensure accurate revenue insights.  

⚠️ **Non-Product Transactions Removed** – Some descriptions such as `"POSTAGE"`, `"FEE"`, `"ADJUST"`, `"MANUAL"`, `"DOTCOM"`, `"CARRIAGE"`, `"REFUND"`, and `"DEBT"` did not represent actual product sales and were removed.  

⚠️ **Outlier Removal for Data Accuracy** – Extremely high values in **Unit Price and Quantity** (above the 99th percentile) were removed to eliminate **potential data entry errors** or **unrealistic transactions** that could skew the analysis.  

---

## **Final Deliverables**  

📊 [Tableau Story Board with Interactive Sales Insights](https://public.tableau.com/app/profile/buket.oztekin/viz/TataOnlineRetail_17385946205930/TataOnlineRetail-StoryBoard)

📄 [Data Cleaning and EDA report](https://docs.google.com/document/d/1py6YwCyPSPAOKS8F337LnPJDdcFFgOQfSIt2tN-Gxpc/edit?usp=sharing)
 
