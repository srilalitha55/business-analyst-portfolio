# 📊 Tech Instagram Influencer Analysis

## 🧾 Project Overview
This project analyzes the performance of a Tech Instagram Influencer account using SQL to uncover content trends, audience behavior, and engagement patterns.

The goal is to generate actionable insights that help improve reach, engagement, and follower growth.

---

## ❗ Problem Statement
The influencer wants to grow their audience but lacks clarity on:

- Which content format performs best  
- What type of content drives engagement  
- When audience growth peaks  
- How users interact with different post types  

---

## 🎯 Objective
- Analyze Instagram data using SQL  
- Identify high-performing content strategies  
- Generate business insights  
- Provide actionable recommendations  

---

## 📊 Key Insights

### 🔹 Content Format Strategy
![Insight 1](images/insight1.png)

Reels contribute ~62% of total reach, making them the most effective format for audience visibility.

---

### 🔹 Viral Potential of Reels
![Insight 2](images/insight2.png)

Reels achieve the highest impressions, showing strong viral potential compared to other formats.

---

### 🔹 Best Performing Content Categories
![Insight 3](images/insight3.png)

Gadget-related content and tech tips generate the highest engagement.

---

### 🔹 Growth Breakthrough Month
![Insight 4](images/insight4.png)

May recorded peak performance in profile visits and follower growth.

---

### 🔹 Share Behaviour Insight
![Insight 5](images/insight5.png)

Image posts receive the highest shares, making them effective for awareness.

---

## 🚀 Recommendations

- Prioritize Reel-based content to maximize reach  
- Focus on gadget-related and educational content  
- Replicate strategies used during high-growth periods  
- Use high-quality images for better shareability  

---

## 🧠 Sample SQL Queries

```sql
-- Reach Percentage by Post Type (Key Insight Driver)
SELECT 
    post_type,
    SUM(reach) AS total_reach,
    ROUND(100 * SUM(reach) / SUM(SUM(reach)) OVER(), 2) AS reach_percentage
FROM gdb0120.fact_content
GROUP BY post_type; 


-- Monthly Growth Analysis (Business Trend)
SELECT 
    dd.month_name,
    SUM(fa.profile_visits) AS total_profile_visits,
    SUM(fa.new_followers) AS total_new_followers
FROM gdb0120.fact_account fa
JOIN gdb0120.dim_dates dd ON dd.date = fa.date
GROUP BY dd.month_name;


-- Top Performing Content Categories (Engagement Insight)
WITH july_likes AS (
    SELECT 
        fc.post_category,
        SUM(fc.likes) AS total_likes
    FROM gdb0120.fact_content fc
    JOIN gdb0120.dim_dates dd ON dd.date = fc.date
    WHERE dd.month_name = 'July'
    GROUP BY fc.post_category
)
SELECT * FROM july_likes
ORDER BY total_likes DESC; 


📂 SQL Queries

👉  [View Full SQL Queries](01-queries/)

🎥 Project Presentation

👉 (https://drive.google.com/file/d/1v3HtmiwkUEB4i7Uc0xCamlTmLjXVCmAe/view?usp=sharing)


🛠 Tools Used
SQL (MySQL Workbench)
PowerPoint


⚠️ Data Disclaimer

Dataset not included due to privacy and usage restrictions.

🙋‍♀️ Author

G R S S SRI LALITHA
Aspiring Business Analyst | SQL | Excel | Power BI
