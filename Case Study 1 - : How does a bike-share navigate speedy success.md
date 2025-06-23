
 # Introduction

Welcome to the Cyclistic bike-share analysis case study! In this case study, you work for a
ctional company, Cyclistic, along with some key team members. In order to answer the
business questions, follow the steps of the data analysis process: Ask, Prepare, Process,
Analyze, Share, and Act. Along the way, the Case Study Roadmap tables — including guiding
questions and key tasks — will help you stay on the right path.

# Scenario
You are a junior data analyst working on the marketing analyst team at Cyclistic, a bike-share
company in Chicago. The director of marketing believes the company’s future success
depends on maximizing the number of annual memberships. Therefore, your team wants to
understand how casual riders and annual members use Cyclistic bikes dierently. From these
insights, your team will design a new marketing strategy to convert casual riders into annual
members. But rst, Cyclistic executives must approve your recommendations, so they must be
backed up with compelling data insights and professional data visualizations.


# 🚲 Cyclistic Bike-Share Case Study (2022)

## 🎯 Goal:
Help the Cyclistic marketing team understand how **casual riders** and **annual members** use bikes differently, and develop strategies to convert casual users into members.

---

## ✅ Step 1: Ask

**Primary Question Assigned to Analyst**:  
**How do annual members and casual riders use Cyclistic bikes differently?**

**Additional Business Questions:**
1. What motivates casual riders to become members?
2. How can Cyclistic use digital tools to influence casual riders?

---

## 📁 Step 2: Prepare

### 📦 Data Source:
- **12 CSV files** (one per month from Jan to Dec 2022).
- Provided publicly by **Motivate International Inc.**.
- Each file includes data like ride ID, timestamps, bike types, stations, coordinates, and user types.

### 📊 Key Columns:
- `ride_id`, `rideable_type`, `started_at`, `ended_at`  
- `start_station_name`, `end_station_name`,  
- `start_lat`, `start_lng`, `end_lat`, `end_lng`,  
- `member_casual`

---

## ⚙️ Step 3: Process

### 🔨 Tool Used:
- **Google BigQuery**

### 🧹 Cleaning & Combining Steps:
- Combined all 12 monthly files using `UNION ALL`.
- Removed rows with:
  - Missing station or coordinate data
  - Trip durations less than 1 minute or more than 1 day
- Added:
  - `ride_length` (in minutes)
  - `day_of_week` (Mon–Sun)
  - `month` (Jan–Dec)
- Created a new clean table: `alldata_cleaned`

---

## 📊 Step 4 & 5: Analyze & Share

### 1. 🚴‍♀️ Bike Type Usage
- **Classic bikes** are most used.
- **Electric bikes** are second.
- **Docked bikes** are mostly used by **casual riders**.

---

### 2. 📅 Trip Patterns

| Time Dimension | Casual Riders                            | Members                                 |
|----------------|-------------------------------------------|------------------------------------------|
| Month          | Peak in **spring & summer**               | Peak in **spring & summer**              |
| Day of Week    | Ride more on **weekends**                 | Ride more on **weekdays**                |
| Hour of Day    | Peak around **10 AM to 6 PM**             | Peak around **8 AM & 5 PM**              |

---

### 3. ⏳ Ride Duration

- **Casual riders take longer trips** (avg. nearly 2x members).
- Members take **shorter, more consistent** rides.
- Longest casual rides occur:
  - **Weekends**
  - **Spring/Summer**
  - **Midday hours**

---

### 4. 📍 Start & End Locations

| Rider Type     | Common Trip Locations                                                  |
|----------------|------------------------------------------------------------------------|
| Casual         | Parks, beaches, museums, harbors – mostly **recreational** zones       |
| Members        | Offices, universities, residential areas – mostly **commuting** zones  |

---

## 🚀 Step 6: Act (Recommendations)

1. **Seasonal Marketing**  
   - Focus on casual riders in **spring and summer**.

2. **Flexible Memberships**  
   - Offer **weekend passes** or **seasonal plans**.

3. **Incentives for Long Rides**  
   - Give **discounts on long rides** to match casual habits.

4. **Geo-Targeted Ads**  
   - Run ads near **parks, beaches, and tourist sites**.

5. **Cost Comparison Campaigns**  
   - Show casual riders how much they’d **save as members**.

---

## 📌 Summary Table

| Feature         | Casual Riders                          | Annual Members                        |
|------------------|-----------------------------------------|----------------------------------------|
| Ride Purpose     | Fun, leisure, recreation                | Daily commute, short errands          |
| Peak Time        | Weekends, midday, summer                | Weekdays, commute hours               |
| Ride Duration    | Long (avg ~2x longer than members)      | Short and consistent                  |
| Ride Locations   | Tourist areas, lakes, parks             | Residential, office, universities     |

---





