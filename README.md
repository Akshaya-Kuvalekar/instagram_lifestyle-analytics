# Instagram Usage Analytics (AWS Athena Project)

## 📌 Project Overview
This project analyzes instagram usage patterns and their impact on engagement, happiness, stress, and subscription behavior using **AWS Athena SQL** on data stored in **Amazon S3**.

The analysis focuses on:
- Screen time vs mental well-being
- Premium vs Free user engagement
- How subscription type and screen time together affect engagement quality

No dashboards or BI tools were used. The project intentionally demonstrates **SQL-first analytics on AWS**.
---

## 🧱 Architecture

CSV Data stored in Amazon S3 is queried directly using Amazon Athena, with table metadata managed by AWS Glue Data Catalog.

![Architecture](architecture/aws_architecture.png)

**Services Used**
- Amazon S3
- AWS Glue Data Catalog
- Amazon Athena

---

## 📊 Analysis & Queries

### 1️⃣ Screen Time vs Happiness vs Stress

**Goal:**  
Understand how daily Instagram screen time impacts happiness, stress, and sleep.

**Key Insight:**
- Moderate usage shows the best balance of happiness and stress
- High usage correlates with increased stress

📄 Query:  
<img width="1022" height="344" alt="1_Screen Time vs Happiness vs Stress" src="https://github.com/user-attachments/assets/a15c7209-01bf-46ca-b253-8b31853d6fbc" />


📸 Result:  
<img width="928" height="156" alt="1_Output" src="https://github.com/user-attachments/assets/cd7fdbfe-93e2-4c9b-82de-73b4fef6b6c0" />

---
### 2️⃣ Premium vs Free User Engagement

**Goal:**  
Compare engagement value between Free, Premium, and Business users.

**Metrics Used:**
- Engagement Score
- Feed Time
- Posts Created
- Ad Clicks

📄 Query:  
<img width="997" height="305" alt="2_Premium vs Free – Engagement Value" src="https://github.com/user-attachments/assets/3b2b6006-52b8-4511-9b5d-f598c64312a0" />


📸 Result:  
<img width="922" height="118" alt="2_output" src="https://github.com/user-attachments/assets/be1f83b8-f9b8-459f-b739-95d7e7f1b7ad" />

---

### 3️⃣ Screen Time × Subscription × Engagement Quality

**Goal:**  
Analyze how screen time behavior interacts with subscription type to influence engagement quality and mental well-being.

**Key Insight:**
- Premium users maintain higher engagement at moderate screen times
- High screen time increases stress across all subscription types

📄 Query:  
<img width="1268" height="338" alt="3_Screen Time × Subscription × Engagement Quality" src="https://github.com/user-attachments/assets/920f66fd-d85d-4a2b-8a82-f980ca50ab0b" />
<img width="861" height="312" alt="3 2_Screen Time × Subscription × Engagement Quality" src="https://github.com/user-attachments/assets/a594e81a-7eb1-4465-a499-267fc316f13e" />


📸 Result:  
<img width="970" height="241" alt="3_output" src="https://github.com/user-attachments/assets/d6a13221-58ee-47b3-ae02-a136f37e1991" />

---
## 🗂️ Data Catalog (AWS Glue)

- Database: `social_media_lifestyle_db`
- Table: `social_media_user_lifestyle`
- Format: CSV
- Storage: Amazon S3
 
<img width="1354" height="301" alt="AWS Glue" src="https://github.com/user-attachments/assets/f9c416ab-a12f-4692-9397-7de344df25bb" />




AWS Glue Data Catalog is used as the metadata layer for Athena queries.  
No ETL jobs were required.

---

## 🧠 Skills Demonstrated

- SQL Analytics (Advanced Aggregations, CASE logic, CTEs)
- AWS Athena
- AWS Glue Data Catalog
- Data Modeling for Behavioral Analysis
- Insight-driven analysis (not just queries)

---

## 👤 Author
**Akshaya Kuvalekar**  
Aspiring Data Analyst / Analytics Engineer 
