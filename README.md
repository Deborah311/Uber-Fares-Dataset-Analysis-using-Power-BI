
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
:  Check for missing values

print("Missing values:")
print(uber_df.isnull().sum())
# Check for duplicates
print("Number of duplicate rows:", uber_df.duplicated().sum())
# Check for zero or negative fare amounts (if Fare is a column)
if 'fare_amount' in uber_df.columns:
    print("Zero or negative fares:", (uber_df['fare_amount'] <= 0).sum())
# Check for data ranges (e.g., for datetime columns)
if 'pickup_datetime' in uber_df.columns:
    print("Pickup datetime range:")
    print(uber_df['pickup_datetime'].min(), " to ", uber_df['pickup_datetime'].max())

<img width="221" height="218" alt="missing values" src="https://github.com/user-attachments/assets/4be5cb99-8494-4b4e-8232-9e7af8f6587e" />



👤 Developed by
Your Name : MURUNGI DEBORAH
ID : 26020
AUCA  software engineering
Group: B 
Date: 25 July 2025


