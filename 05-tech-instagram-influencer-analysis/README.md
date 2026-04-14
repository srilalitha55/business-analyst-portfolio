# 📊 Tech Instagram Influencer Analysis

## 🧾 Project Overview
This project focuses on analyzing the performance of a Tech Instagram Influencer account to identify content trends, audience behavior, and engagement patterns.

The objective is to analyze Instagram activity data using SQL and generate actionable insights to improve reach, engagement, and follower growth.

---

## ❗ Problem Statement
The influencer aims to grow their audience and improve content performance.

However, key challenges include:

- Identifying high-performing content formats  
- Understanding which categories drive engagement  
- Analyzing follower growth trends  
- Improving reach and visibility  

Management wants to:

- Monitor content performance  
- Identify high-performing strategies  
- Improve engagement and reach  
- Make data-driven content decisions  

---

## 🎯 Objective
- Analyze Instagram data using SQL  
- Identify top-performing content formats  
- Evaluate engagement metrics  
- Analyze monthly growth trends  
- Provide actionable business insights  

---

## 📌 Key Metrics
- Reach Percentage  
- Impressions  
- Likes  
- Shares  
- Profile Visits  
- New Followers  

---

## 📊 SQL Queries & Outputs

### 🔹 Query 1 – Unique Post Types
```sql
SELECT COUNT(DISTINCT post_type) AS unique_post_types
FROM gdb0120.fact_content; 
output
![Query 1 Output](images/query1_output.png)


### 🔹 Query 2 – Highest & Lowest Impressions
SELECT post_type,
MAX(impressions) AS highest_impressions,
MIN(impressions) AS lowest_impressions
FROM gdb0120.fact_content
GROUP BY post_type; 
output

### 🔹
