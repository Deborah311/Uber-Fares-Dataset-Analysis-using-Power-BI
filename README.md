
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

<img width="564" height="549" alt="image" src="https://github.com/user-attachments/assets/a29526ea-619d-4440-85cb-909137594979" />


<img width="439" height="550" alt="image" src="https://github.com/user-attachments/assets/933a83d5-3bf8-41fa-9c38-bf21deb199d6" />

<img width="649" height="362" alt="summary" src="https://github.com/user-attachments/assets/e0d882b0-a7f4-49e3-93d8-d1b8681c9468" />

<img width="500" height="192" alt="dropoff" src="https://github.com/user-attachments/assets/1619e519-c741-4850-bf80-4baa5124a33b" />
# Check for missing values

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
    
<img width="283" height="237" alt="image" src="https://github.com/user-attachments/assets/ff8906af-6d95-459b-9670-6ed33309b512" />

# Drop rows with missing values in important columns
uber_df_clean = uber_df.dropna(subset=['fare_amount', 'pickup_datetime', 'pickup_longitude', 'pickup_latitude'])
# Fill missing passenger count with mode (most common value)
if 'passenger_count' in uber_df_clean.columns:
    mode_value = uber_df_clean['passenger_count'].mode()[0]
    uber_df_clean['passenger_count'].fillna(mode_value, inplace=True)
    
    
    <img width="1033" height="145" alt="image" src="https://github.com/user-attachments/assets/77e3b9e4-afb4-4231-acc4-fd53dc045970" />

    # Convert pickup_datetime to datetime
uber_df_clean['pickup_datetime'] = pd.to_datetime(uber_df_clean['pickup_datetime'], errors='coerce')

# Remove invalid fare values

uber_df_clean = uber_df_clean[uber_df_clean['fare_amount'] > 0]

 3. Feature Engineering
  
# Ensure pickup_datetime is in datetime format

uber_df['pickup_datetime'] = pd.to_datetime(uber_df['pickup_datetime'])

# 1. Extract hour, day, and month

uber_df['hour'] = uber_df['pickup_datetime'].dt.hour
uber_df['day'] = uber_df['pickup_datetime'].dt.day
uber_df['month'] = uber_df['pickup_datetime'].dt.month

# 2. Extract day of the week

uber_df['day_of_week'] = uber_df['pickup_datetime'].dt.day_name()

# 3. Define peak/off-peak hours

def classify_peak(hour):
    if 7 <= hour <= 9 or 17 <= hour <= 19:
        return 'Peak'
    else:
        return 'Off-Peak'

uber_df['peak_time'] = uber_df['hour'].apply(classify_peak)

# Preview the new columns

print(uber_df[['pickup_datetime', 'hour', 'day', 'month', 'day_of_week', 'peak_time']].head())

# Save enhanced dataset

uber_df.to_csv("uber_cleaned_dataset.csv", index=False)
print("Enhanced dataset saved as 'uber_cleaned_dataset.csv'")

<img width="593" height="162" alt="image" src="https://github.com/user-attachments/assets/b6e072f0-2671-4303-89dc-cce80872946d" />
:Created time periods (Peak/Off-Peak), ride distance, and duratio

# Import necessary library

import pandas as pd

# Show basic statistics (mean, std, min, max, quartiles)

print("Descriptive statistics:")
print(uber_df_clean.describe())

# Median for each numeric column
print("\nMedian values:")
print(uber_df_clean.median(numeric_only=True))

# Mode for each column
print("\nMode values:")
print(uber_df_clean.mode(numeric_only=True).iloc[0])

# Standard deviation for each numeric column
print("\nStandard deviation:")
print(uber_df_clean.std(numeric_only=True))

# Mean for each numeric column
print("\nMean values:")
print(uber_df_clean.mean(numeric_only=True))





👤 Developed by
Your Name : MURUNGI DEBORAH
ID : 26020
AUCA  software engineering
Group: B 
Date: 25 July 2025


