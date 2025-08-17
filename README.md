🚕 Uber Trip Analysis Power BI Project
A comprehensive, end-to-end analytics and dashboarding project leveraging real-world Uber trip data (NYC, June 2024) to uncover actionable business insights. Built 100% by BeroshinSamuel, this solution demonstrates Power BI design, advanced DAX, dimensional modeling.

🟢🟢🟢 Project Overview
This project analyzes 100,000+ Uber rides from New York City using Power BI. It demonstrates data modeling, interactive dashboards, and complex DAX logic to deliver strategic insights such as demand hotspots, time trends, driver deployment strategies, and customer preferences.

🟢🟢🟢 Data Sources

uber_trip_details.xlsx

a) trip_id: Unique ride identifier

b) pickup_time, dropoff_time: Datetime for start/end of each ride

c) passenger_count

d) distance_miles

e) pickup_location_id, dropoff_location_id

f) fare_amount, surge_fee

g) vehicle_type: UberX, XL, Comfort, etc.

h) payment_type: Uber Pay, Cash, etc.

locations.xlsx

a) id: each location have seperate for identification

b) name: Friendly location name

c) city: Borough or main NYC area

🟢🟢🟢 Technical Architecture

Active (pickup) and inactive (dropoff, DAX-activated) relationships between trips and locations to support dual geographic context.

Calendar table for time calculations (date hierarchy, days, weeks, weekdays, time bins).

Optimized DAX: Measures for KPIs, dynamic ranking, 10-minute time binning, switching metrics via parameter tables, advanced filter logic.

Performance best practices: Proper datatypes, cardinality checks, minimized columns, no calculated columns on large tables unless necessary.

🟢🟢🟢 Development Process

1. Data Prep & QA

Imported Excel data with Power Query.

Validated row counts, data types; checked for nulls/errors.

2. Data Modeling & DAX

Defined relationships and built a robust star schema.

Wrote custom DAX:

KPIs (Total Bookings, Avg Distance, Total Revenue, etc.)

Hotspot detection (TOPN, SUMMARIZE, CONCATENATEX)

Farthest trip (MAX + LOOKUPVALUE)

Dropoff analytics (USERELATIONSHIP)

Time and metric parameter switching (SWITCH, SELECTEDVALUE)

3. Dashboard Design

Overview: KPIs, payment splits, vehicle mix

Time Analysis: Slicers, hourly trends in 10-min bins, weekday demand, heatmaps

Location Analytics: Top pickup/dropoff points, top-5 locations by bookings, farthest trip, vehicle type by location

Drill-through: Row-level detail, export option for filtered data

4. UX/UI & Interactivity

Dynamic chart titles, cross-filtering on all visuals

Slicers for city, date, vehicle, payment type

Conditional formatting, bookmark navigation, filter reset buttons

🟢🟢🟢 How to Use

Clone/download this repo (including data and screenshots if shared).

Open Uber_NYC_Analysis.pbix (Power BI Desktop 2023+ recommended).

Adjust data source paths if needed (Data > Transform Data > Edit file path).

Use dashboard slicers to filter, explore, and drill into the data.

Export filtered results from detail pages for reporting as required.

🟢🟢🟢 Sample Screenshots

📷 Overview Analysis <img width="1702" height="912" alt="image" src="https://github.com/user-attachments/assets/1b4a2aec-c1fa-402d-807a-08992fdddb18" />
📷 Time Analysis <img width="1701" height="911" alt="image" src="https://github.com/user-attachments/assets/0b164c2a-3c16-4993-a58e-33ae8e9568b2" />
📷 Details <img width="1668" height="912" alt="image" src="https://github.com/user-attachments/assets/7dc9ffb8-b06e-4928-a2ea-0240218db34a" />


