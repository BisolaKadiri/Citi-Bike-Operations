# Citi Bike Operations
This report analyses the operational performance of New York City's bike-sharing service which reveals insights into station performance, user demographics, and trip patterns. It also provides recommendations to optimize bike availability, reduce wait times, and improve overall user experience.
New York City's bike-sharing service, launched in 2013, has revolutionized the way residents and tourists navigate the city. With over 24,000 bikes and 750 stations across the five boroughs, the system provides an efficient, sustainable, and affordable transportation option. However, as the demand for bike-sharing continues to grow, optimizing its operations becomes crucial to ensure user satisfaction, scalability, and profitability.

## Project Overview
This project involves analyzing bike-sharing data for optimizing city bike operations. The analysis leverages SQL for querying data in Google BigQuery and Tableau for visualizations. It incorporates two datasets:

1. City Bike Trip Dataset: Contains trip details, such as trip start time, end time, station details, and user type.

2. City Bike Station Dataset: Originally provided in JSON format, converted to CSV using Google Colab.

## Tools and Technologies

- Google BigQuery: For SQL-based data exploration and analysis.

- Tableau: For creating visualizations to interpret data insights.

- Google Colab: For data preprocessing and format conversion (JSON to CSV).

## Datasets

Dataset 1: City Bike Trip
Source: https://citibikenyc.com/system-data?form=MG0AV3

Key Columns:
- ride_id: Unique identifier for each trip.
- rideable_type: Type of bike (e.g., electric or regular).
- started_at: Timestamp of when the trip started.
- ended_at: Timestamp of when the trip ended.
- start_station_name: Name of the station where the trip started.
- start_station_id: ID of the start station.
- end_station_name: Name of the station where the trip ended.
- end_station_id: ID of the end station.
- start_lat: Latitude of the start location.
- start_lng: Longitude of the start location.
- end_lat: Latitude of the end location.
- end_lng: Longitude of the end location.
- member_casual: Indicates if the user is a member or casual user.

## Dataset 2: City Bike Station
Source: https://gbfs.citibikenyc.com/gbfs/en/station_status.json (JSON File)
CSV File: https://colab.research.google.com/drive/1OF9c46CZ7d4qwM4hvWkqgs1haZpMwh1m (Converted in Google Colaboratory)

Key Columns (after conversion):
- num_docks_available: The number of docks currently available for parking bikes at the station.
- is_renting: Indicates whether the station is currently allowing bikes to be rented (1 for true, 0 for false).
- num_docks_disabled: The number of docks at the station that are not functional or are out of service.
- station_id: A unique identifier for the station.
- eightd_has_available_keys: Indicates if the station has physical keys available for users who require them to unlock bikes (1 for true, 0 for false).
- last_reported: The timestamp of the last update/report for the station's status.
- is_installed: Indicates whether the station is installed at its location (1 for true, 0 for false).
- num_ebikes_available: The number of electric bikes currently available at the station.
- legacy_id: An older or alternate identifier for the station, possibly from a previous system.
- num_bikes_disabled: The number of bikes at the station that are disabled or not available for use.
- num_bikes_available: The total number of bikes currently available for use at the station.
- is_returning: Indicates whether the station is accepting returns of bikes (1 for true, 0 for false).
- num_scooters_available: The number of scooters currently available at the station.
- num_scooters_unavailable: The number of scooters at the station that are not available for use.


## Process Workflow

1. Data Preparation

- City Bike Trip Dataset:
Loaded directly to BigQuery.

- City Bike Station Dataset:
Loaded the JSON file into Google Colab.
Converted the JSON file into a CSV file using Python:

Uploaded the CSV file to BigQuery for integration.

## Data Analysis - SQL Queries in BigQuery:
Link to the SQL Queries  Workbook: https://drive.google.com/file/d/11_96HsejgIlru9y_0kwxBtqR2S0JrYV8/view?usp=sharing

### A: Station Performance Analysis
1.Top 10 Busiest Stations by Trip Count:

2.Total Trips Starting at Each Station

3.Total Trips Ending at Each Station

4.Frequently used stations and how many trip

5.Average Bike and Dock Availability

6.Stations with the Highest Proportion of Disabled Bikes and Docks


### B: Trip Duration and Patterns
1.Most Common Routes (Start to End)

2.Average Trip Duration by User Type

3.Peak Usage Hours

4.Total Trip Counts Each Day of the Week

5.Hourly Trip Counts for Weekdays vs. Weekends

6.Most frequent rideable type


### C: System Reliability 
1.Stations frequently offline (Is Installed or Is Renting)

2.Days not Installed and days not Renting

Downloaded each of the results as a CSV File. Here is the link to access the SQL Queries Results: https://drive.google.com/drive/folders/16un8KIShmHS8S1O566kap1TORIYONVuE?usp=sharing

## Visualization in Tableau 
The dashboard aims to provide insights into the operational performance of New York City's bike-sharing service, enabling data-driven decisions to optimize bike availability, reduce wait times, and enhance the overall user experience.
      
- Benefits
1. Improved Operational Efficiency: Optimizes bike availability and reduces wait times.
2. Enhanced User Experience: Provides insights to improve station placement and capacity.
3. Data-Driven Decision Making: Enables informed decisions based on data analysis and visualization.


### Visualization Report:

The Dashboard can be accessed through this link: https://public.tableau.com/app/profile/bisola.sobowale/viz/NYC_Citi_BikeAnalysis/Dashboard1?publish=yes 

## Recommendations
The recommendations outlined in this report can be implemented as follows:
- Short-term: Implement dynamic bike distribution and dock expansion at busy stations to reduce wait times and congestion.
-	Long-term: Analyze user data and trends to identify opportunities for further optimization and improvement.
  
The expected impact of these recommendations is:
-	Reduced wait times: Dynamic bike distribution and dock expansion will reduce wait times and congestion at busy stations.
-	Improved user experience: By optimizing bike distribution and dock capacity, users will experience a more efficient and convenient bike-sharing service.

## CONCLUSION
The key findings of this report are:
-	Operational challenges: Inefficient bike distribution and insufficient dock space are major operational challenges impacting user experience.
- Solutions and strategies: Dynamic bike distribution, dock expansion, and optimized maintenance scheduling can mitigate these challenges.







