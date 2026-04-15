# 📊 Tech Instagram Influencer Analysis

## 🧾 Project Overview
Analyzed Instagram influencer data using SQL to identify content performance trends, audience engagement patterns, and growth opportunities.

---

## ❗ Problem Statement
The influencer lacked clarity on:
- Best performing content format  
- High engagement content categories  
- Growth trends over time  

---

## 🎯 Objective
- Analyze Instagram data using SQL  
- Identify high-performing content  
- Generate actionable insights  

---

## 📊 Key Insights

- Reels contribute ~62% of total reach → most effective content format  
- Reels show highest viral potential (highest impressions)  
- Gadget & Tech content drives maximum engagement  
- May recorded peak growth in followers and profile visits  
- Image posts generate highest shares  

---

## 🚀 Recommendations

- Focus on Reel-based content for better reach  
- Create more gadget-related and educational posts  
- Replicate strategies from high-growth periods  
- Use high-quality images for shareability  

---

## 🧠 Sample SQL

```sql
SELECT post_type,
SUM(reach),
ROUND(100 * SUM(reach) / SUM(SUM(reach)) OVER(), 2)
FROM gdb0120.fact_content
GROUP BY post_type; 

---

## ⚠️ Data Disclaimer

Datasets used in this project are not included in this repository due to data privacy and usage guidelines.

---

## 🛠 Tools Used

SQL (MySQL Workbench),
PowerPoint

---

### 🔹 Content Format Strategy
![Insight 1](images/insight1.png)

Reels contribute ~62% of total reach, making them the most effective format for audience visibility.

---

### 🔹 Viral Potential of Reels
![Insight 2](images/insight2.png)

Reels achieve the highest impressions, showing strong viral potential.

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

## 🎥 Project Presentation (Audio Explanation)
👉 [Click here to listen to the project explanation](https://drive.google.com/file/d/1_h8qlJdZeo3RP5AQfzmIfBrwMv_9je40/view?usp=sharing)


## 🙋‍♀️ Author
**G R S S SRI LALITHA**  
Aspiring Business Analyst | Power BI | SQL | Excel | Data Analysis | Data Visualization
