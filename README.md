
# 🚖 Uber Fares Dataset Analysis Using Power BI

## 🔍 Project Overview

This project is part of the course **Introduction to Big Data Analytics (INSY 8413)** at **AUCA**, instructed by **Mr. Eric Maniraguha**. The objective is to explore and analyze the **Uber Fares Dataset** using Python for data cleaning and Power BI for visualization. The analysis aims to uncover patterns in Uber fares, ride durations, time trends, and other operational insights.

🎯 Project Objectives

:To analyze Uber fare patterns,ride durations, and temporal trends

:To create new analytical features (e.g., hour, day, time categories)

:To develop an interactive Power BI dashboard showing:

💵 Fare distribution

histograms

box plots

🚗 Ride patterns

Hourly

Daily

Monthly

🌦️ Seasonal and 🌍 geographic trends

To highlight busiest periods and, if possible, assess weather impact

To deliver actionable business insights through data storytelling

Methodology:
🗃️ 1. Data Collection


Downloaded Uber Fares dataset from Kaggle
Included:

fare amount

pickup time

geolocations

🧹 2. Data Cleaning (Python)

pip install pandas

Used Pandas to load and inspect data


<img width="428" height="412" alt="IMPORTPANDAS" src="https://github.com/user-attachments/assets/8d10f32d-1e48-46cb-8cf2-6ccd700c9600" />


<img width="989" height="357" alt="image" src="https://github.com/user-attachments/assets/a4fa264b-fb03-4708-a975-c31548a9c07d" />


<img width="852" height="422" alt="image" src="https://github.com/user-attachments/assets/319f44e1-bf54-4008-ad9a-d982a1962cbe" />


<img width="311" height="230" alt="image" src="https://github.com/user-attachments/assets/9731219a-caac-4012-ad08-a92dd17b333d" />


<img width="653" height="230" alt="image" src="https://github.com/user-attachments/assets/1b744dcd-35e9-48d5-b1ef-8c19a9a7537c" />

3. Feature Engineering
   
Hour, day, month extracted from timestamps


<img width="690" height="331" alt="image" src="https://github.com/user-attachments/assets/5a39efbf-beec-44c5-9648-55876c904d3e" />


<img width="221" height="218" alt="missing values" src="https://github.com/user-attachments/assets/4be5cb99-8494-4b4e-8232-9e7af8f6587e" />


<img width="526" height="170" alt="image" src="https://github.com/user-attachments/assets/5f87f8c2-f63c-4994-a6d9-95c50a5848ae" />


Confirmed Extracted Features:


<img width="808" height="343" alt="image" src="https://github.com/user-attachments/assets/f66b7470-f466-4189-b76d-57425c99ef9d" />


Day of week categorization


<img width="652" height="403" alt="image" src="https://github.com/user-attachments/assets/7a0b84c6-5cf9-453c-a9dc-108079426cd2" />


Peak/off-peak time indicators


<img width="620" height="474" alt="image" src="https://github.com/user-attachments/assets/506cfd97-a059-4a7a-aa0a-e53e9b019415" />


📊 4. Power BI Analysis


Imported dataset into Power BI Desktop

<img width="1324" height="495" alt="image" src="https://github.com/user-attachments/assets/912a6556-da3d-4d39-ac82-6537bd2d63c3" />

:Built interactive visuals

DAX formulas used:

Count
Sum
Average
Variance
Standard Variation

all charts needed to be used
<img width="990" height="547" alt="charts" src="https://github.com/user-attachments/assets/84033f26-13d2-4852-81f3-e7153084e8c0" />

sum of _amount by dropff_longitude

<img width="565" height="319" alt="sum of f amuont" src="https://github.com/user-attachments/assets/2b4d5d15-3148-480c-995e-efb57aff6419" />


countof fare_amount by passenger_count

<img width="522" height="324" alt="countfare" src="https://github.com/user-attachments/assets/00a2e128-d6ec-43ff-9abe-8639ea3d3534" />


sum of pickup_longitude by pickup_latitude

<img width="296" height="329" alt="sumof pickup" src="https://github.com/user-attachments/assets/37dbd66b-6a21-48d9-9359-8832780a13c9" />


pickup_latitude_pickup_longitude

<img width="575" height="364" alt="map" src="https://github.com/user-attachments/assets/2b38e835-0c27-44fb-ae59-7dc8945e694b" />


sum of passengers_count by pickup_deteime


<img width="611" height="347" alt="sum" src="https://github.com/user-attachments/assets/b0551ce2-a1fe-4226-a2ea-ec684e0bf430" />


<img width="886" height="422" alt="all charts" src="https://github.com/user-attachments/assets/d04bd5b7-eb4c-42f1-8b5f-a0152c826fcb" />


Added slicers, filters, and drill-down capabilities
Slicers:Interactive Filters

<img width="885" height="440" alt="dashboad" src="https://github.com/user-attachments/assets/d6c82534-8ed4-4605-9b8f-d84385e63a71" />

📊 Analysis: Detailed Findings & Statistical Insights
🚗 1. Fare Distribution
Most Uber fares fall within $5–$20

Box plot visualizations identified outliers exceeding $100 (likely airport/long-distance rides)

Slightly higher fares during peak hours due to high demand

⏰ 2. Time-Based Ride Patterns
Busiest hours: 7–9 AM and 5–7 PM (commute times)

Friday and Saturday show highest ride activity

Summer months see higher monthly trends in rides

📍 3. Geographic Trends
Pickup concentrations in central NYC

Hotspots include Midtown and Lower Manhattan

Heatmaps show higher fare zones near airports and business hubs

📈 4. Correlations & Metrics
Positive correlation between distance and fare

Longer ride durations usually result in higher prices

Fare per km is consistent, but slightly higher during peak hours

🔍 Key Results: Discoveries and Pattern Identification
Insight Area	Finding
Peak Ride Hours	Morning (7–9 AM) and Evening (5–7 PM)
Weekly Trends	Highest activity on Fridays and Saturdays
Fare Patterns	Most rides cost $5–$20, few exceed $100
Geographic Hotspots	Central Manhattan and Airport Areas
Distance vs Fare	Strong positive correlation
Seasonal Trends	Increased rides in summer
Peak Time Impact	Slight fare surge during high demand hours

🧠 Conclusion
Uber ride demand peaks during commute times

Weekend activity is consistently high, especially Fridays and Saturdays

Majority of fares are economical, with occasional high outliers

Central NYC and airport routes see the highest demand

Strong correlation between distance and fare

Summer months see a noticeable increase in ride frequency

Peak hours come with slightly elevated fare averages

💡 Recommendations: Data-Driven Suggestions
Increase Driver Availability: Prioritize peak times (7–9 AM, 5–7 PM)

Weekend Offers: Promote discounts on Fridays/Saturdays

Airport Pricing Strategy: Consider flat-rate or transparent fare policies

Hotspot Optimization: Deploy more drivers in Midtown & Lower Manhattan

Prepare for Seasonal Demand: Launch summer incentives for drivers

Off-Peak Promotions: Encourage rides with reduced fares during low-demand hours

Fare Estimation Enhancement: Improve algorithms using fare-per-km insights

💾 File Export
The cleaned dataset with new features was saved as:

plaintext
Copy
Edit
uber_cleaned_dataset.csv
Ready for direct import into Power BI.

📄 License
This project is licensed under the MIT License – see the LICENSE file for details.
👤 Developed by
Your Name : MURUNGI DEBORAH
ID : 26020
AUCA  software engineering
Group: B 
Date: 25 July 2025


