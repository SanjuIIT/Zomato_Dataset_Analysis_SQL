# Zomato Dataset Analysis using SQL

# Zomato Data Exploration & Analysis (SQL Server)

## Project Overview
This project focuses on **end-to-end data exploration and analysis** of the Zomato restaurant dataset (~9,000+ rows, 15 countries) using **SQL Server**.  
The goal is to clean, enrich, and analyze the data to extract meaningful **business insights** about restaurants, cuisines, locations, ratings, and services.

---

## Dataset
- Contains restaurant details: **`RestaurantID`, `RestaurantName`, `CountryCode`, `City`, `Locality`, `Cuisines`, `Votes`, `Rating`, `Price_range`, `Average_Cost_for_two`, `Currency`, `Has_Table_booking`, `Has_Online_delivery`** 
- Note that Country details merged from a separate mapping table (`ZOMATO_COUNTRY`).

---

## Process & Pipeline

### 1️.) Data Exploration & Cleaning
- Inspected schema: column names, datatypes, constraints.
- Removed duplicates in `RestaurantID`.
- Dropped irrelevant columns (`Address`, `LocalityVerbose`, `Switch_to_order_menu`).
- Merged two tables (`ZomatoData1` + `ZOMATO_COUNTRY`) to enrich data with **Country Names**.
- Corrected misspelled **city names** using string operations.
- Converted inconsistent datatypes (Votes → INT, Cost → FLOAT, Rating → DECIMAL).
- Created new **rating categories**: POOR, GOOD, GREAT, EXCELLENT.

### 2️.) Data Analysis
- Counted restaurants per city/locality using **window functions** (rolling/moving counts).
- Computed **min, max, avg** for votes, ratings, and costs.
- Analyzed percentage share of restaurants by **Country**.
- Identified **countries providing online delivery** and % penetration.
- Determined localities in India with **highest/lowest restaurant counts**.
- Found most popular **cuisines** in high-density localities.
- Compared ratings of restaurants **with vs without table booking**.
- Identified **best moderately priced restaurants** based on rules (cost < 1000, rating > 4, votes > 1000, with online delivery & table booking).

---

## Key Insights
- **90.67%** of restaurants are listed in **India**, followed by **USA (4.45%)**.  
- Only **India (28.01%)** and **UAE (46.67%)** have significant online delivery adoption.  
- **Connaught Place (New Delhi)** has the **most restaurants (122)**, with **North Indian food** as the top cuisine.  
- In Connaught Place:
  - Restaurants with **table booking** average a **3.9/5 rating**, higher than those without (**3.7/5**).  
- Identified **best value restaurant**: *India Restaurant, Kolkata* (RestaurantID: 20747) – affordable, highly rated, offers online delivery & table booking.

---

## Outcomes
- Cleaned Zomato dataset with added **Country Name** and **Rating Category** fields.  
- Analytical views & KPIs for restaurant distribution, delivery adoption, cuisines, and service quality.  
- Business insights applicable to **food delivery platforms, restaurant analytics, and consumer behavior studies**.

---

## Tech Stack equipped
- Strong **SQL Server (T-SQL)** skills: joins, CTEs, views, window functions, case-based categorization.  
- Ability to handle **real-world messy data** and perform cleaning, normalization, enrichment.  
- Converting raw data into **actionable insights** for business decision-making.  

---

## Myself:
**Muthu Sanjay P - CE22B076**  
IIT Madras • Data/Analytics/ML Enthusiast  
Mail: ce22b076@smail.iitm.ac.in • [LinkedIn](https://www.linkedin.com/in/muthusanjay/)  • [GitHub](https://github.com/SanjuIIT)  


