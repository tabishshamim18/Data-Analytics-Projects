# 🛍️ Customer Segmentation & Revenue Analysis using RFM (E-commerce Project)

## 📝 Executive Summary
E-commerce businesses collect massive amounts of transactional data, but turning that data into **actionable customer insights** is often a challenge.  

This project focuses on applying the **RFM (Recency, Frequency, Monetary)** framework to segment customers into meaningful groups, such as **loyal**, **high-value**, or **at-risk**, using real e-commerce data.  

📊 A **Power BI dashboard** was created to visualize these segments, identify purchasing patterns, and highlight revenue trends over time.  

✅ **Key Outcomes:**  
- Segmented **4,335 customers** into 4 key groups using RFM scores.  
- Identified that **65% of revenue comes from loyal customers**, with clear purchasing seasonality.  
- Surfaced at-risk segments and low-frequency buyers to target for retention campaigns.  
- Enabled data-driven marketing strategies aimed at boosting **customer retention and lifetime value**.

---

## 💼 Business Problem
E-commerce companies generate vast transactional data but often lack a structured way to **understand customer behavior**. This leads to missed opportunities in:  
- Identifying **high-value customers** for loyalty programs  
- Spotting **at-risk segments** before they churn  
- Targeting marketing campaigns effectively  
- Maximizing **customer lifetime value**  

A systematic approach like RFM analysis allows businesses to classify customers based on **how recently**, **how often**, and **how much** they purchase — making segmentation clear, measurable, and actionable.

---

## 🧭 Methodology
Here’s a step-by-step overview of what was done:

1. **Data Collection & Preparation**  
   - Loaded transactional e-commerce dataset and cleaned missing or invalid records.  
   - Standardized date columns, customer IDs, and monetary fields.

2. **RFM Calculation**  
   - Calculated **Recency** (days since last purchase), **Frequency** (number of transactions), and **Monetary** (total spend).  
   - Assigned R, F, and M **scores from 1 to 5** for each metric.

3. **Segmentation**  
   - Created **RFM segments** based on score combinations.  
   - Grouped customers into meaningful clusters (e.g., Loyal, High Value, At Risk, Dormant).

4. **Visualization & Insights**  
   - Built a **Power BI dashboard** to visualize revenue trends, customer segment distribution, and activity patterns over time.  
   - Added filters for **Country**, **Month**, **Quarter**, and **Year** to support dynamic exploration.

5. **Business Analysis**  
   - Identified high-revenue segments and purchasing trends.  
   - Highlighted retention opportunities through RFM heatmaps and activity charts.

---

## 🧠 Skills Demonstrated

| Skill Area        | Techniques Used |
|--------------------|-----------------|
| **Python**         | Data cleaning with Pandas, datetime transformations, RFM score calculations |
| **Data Analysis**  | Cohort analysis, segmentation, aggregations, ranking |
| **Power BI**       | Interactive dashboard, slicers, pie & line charts, heatmaps, dynamic filters |
| **RFM Modelling**  | Recency, Frequency, Monetary scoring & segmentation logic |
| **Data Storytelling** | Translating complex data into business insights through clear visuals |

---

## 📈 Results & Business Recommendations

### 🟢 **Results**
- **Total Revenue:** £8.74M across **4,335 customers**  
- **Loyal customers (RFM high)** generated **~65%** of total revenue.  
- **At-risk and dormant segments** made up ~25% of the base but contributed less than 10% of revenue.  
- **Revenue peaks** observed between **September and December**, indicating seasonal buying behavior.  
- Top 10 customers accounted for **significant share of sales volume**, indicating key accounts.

### 🧭 **Recommendations**
- 🎯 **Loyal & High Value:** Launch exclusive offers or loyalty programs to retain and reward this group.  
- 📨 **At Risk:** Use personalized re-engagement campaigns (discounts, reminders) to bring them back.  
- 🛒 **Dormant Customers:** Offer win-back promotions or surveys to understand churn drivers.  
- 📆 **Seasonality:** Plan inventory and marketing campaigns ahead of peak months to maximize revenue.  
- 👤 **Top Customers:** Assign account managers or priority services to maintain their high contribution.

---

## 🚀 Next Steps
- ⏳ **Automate** the RFM pipeline to refresh segmentation periodically (e.g., weekly or monthly).  
- 📬 Integrate dashboard insights with **email marketing tools** to trigger campaigns automatically.  
- 🤖 Apply **machine learning models** to predict churn and potential high-value customers.  
- 🌍 Add more filters (e.g., product categories, channels) for deeper insights.

---

## 🧰 Tech Stack
- **Languages:** Python (Pandas, NumPy, Matplotlib, Seaborn), SQL  
- **Visualization:** Power BI  
- **Data Modelling:** RFM Framework  
- **Version Control:** Git & GitHub

---

## 📌 Dashboard Snapshot
![RFM Dashboard](./RFM%20Dashboard.png)

---

## 👤 Author
**Tabish Shamim**  
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=flat-square&logo=linkedin)](https://www.linkedin.com/in/tabish-shamim-2818h)  
[![Email](https://img.shields.io/badge/Email-Contact-red?style=flat-square&logo=gmail)](mailto:tabishshamim94@gmail.com)

---

⭐ If you found this project interesting, consider **starring the repository** — it helps support more analytics projects like this!


