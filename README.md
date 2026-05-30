# 🏋️‍♂️ SUMMITS Operations & Member Exercise Analytics (SQL)

## 📌 Project Overview
This project focuses on analyzing operational data and member exercise behavior at **SUMMITS Fitness Center**. Utilizing a MySQL database, this analysis evaluates the most popular workout trends, calorie expenditure by gender, cardiovascular performance, and body composition segmentation. The insights derived aim to optimize business strategies, facility allocation, and the efficiency of Personal Training (PT) programs.

## 🛠️ Tech Stack & Tools
- **Database Server:** MySQL
- **Query Tool:** MySQL Workbench
- **Dataset:** Gym Members Exercise Tracking (Kaggle)

---

## 📝 Business Questions & Insights

### 1. Calorie Burn Analysis by Gender
**Question:** Which demographic group burns more calories per exercise session?

| Gender | Average Calories Burned |
| :--- | :--- |
| **Male** | 944.46 kcal |
| **Female** | 862.25 kcal |

**Business Insight:** Male members burn approximately 9.5% more calories per session. The operations team can leverage this data to optimize the distribution of complimentary hydration or supplement offerings at the gym juice bar based on daily demographic traffic.

---

### 2. Most Popular Workout Type Segmentation
**Question:** Which workout types are most preferred by gym members?

| Workout Type | Total Members |
| :--- | :--- |
| **Strength** | 258 |
| **Cardio** | 255 |
| **Yoga** | 239 |
| **HIIT** | 221 |

**Business Insight:** Strength Training and Cardio are the primary drivers of member engagement. **Business Recommendation:** Prioritize budget allocation for the routine maintenance of cardio equipment (treadmills) and ensure a well-stocked inventory of dumbbells and weight plates to minimize bottlenecking during peak hours.

---

### 3. Profile Analysis of Active Members (> 3 Days/Week)
**Question:** What are the average workout duration and cardiovascular metrics of highly active members?

| Average Avg_BPM | Average Session Duration |
| :--- | :--- |
| 143.41 BPM | 1.49 Hours (~90 Minutes) |

**Business Insight:** Active members average a 90-minute workout window while sustaining an ideal active cardio heart rate zone (143 BPM). This segment represents a high-conversion target audience for Personal Trainers to pitch advanced, long-term premium training programs due to their pre-existing high commitment levels.

---

### 4. Body Fat Percentage Segmentation for Members > 70 kg
**Question:** What is the average body fat percentage by gender for members weighing over 70 kg?

| Gender | Average Body Fat Percentage |
| :--- | :--- |
| **Male** | 21.75% |
| **Female** | 30.07% |

**Business Insight:** This physiological baseline allows the club management to design tailored, data-driven "Fat Loss Challenges" or body recomposition programs that cater specifically to the weight-to-fat ratios of heavier demographics.

---

### 5. Youth Demographic Exercise Trends (< 25 Years Old) & Cardiovascular Health
**Question:** What are the preferred workout types for younger members, and what does their average Resting Heart Rate (Resting BPM) indicate about their fitness level?

| Workout Type | Youth Member Count | Average Resting BPM |
| :--- | :--- | :--- |
| **Cardio** | 47 | 63.57 BPM |
| **HIIT** | 43 | 62.77 BPM |
| **Strength** | 38 | 62.08 BPM |
| **Yoga** | 37 | 59.08 BPM |

**Business Insight:** The youth demographic (< 25 years old) heavily favors dynamic, high-intensity workouts (Cardio & HIIT). Furthermore, their average Resting BPM ranging between 59–63 BPM indicates excellent cardiovascular health and athletic conditioning, signaling a highly fit micro-segment within the SUMMITS community.

---

## 📂 File Structure
- `gym_analytics_queries.sql` : Raw SQL script containing all analytical queries.
- `README.md` : Comprehensive project documentation and data-driven business insights.
