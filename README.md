# -Analyzing-Smart-City-Bike-Sharing-Data-using-Power-BI
                       The objective of this project is to analyze the performance of the bike-sharing system using Power BI. It helps monitor bike availability, station status, and bike usage across different locations. 
 Project Overview
•	Business Problem: The task is to analyze this real-time bike station dataset to understand station performance, usage efficiency, and operational patterns across cities.
•	Objective: The objective of this project is to analyze the performance of the bike-sharing system using Power BI..
•	Target Audience: bike-sharing operators, transportation authorities
🗃️ Data Sources & Architecture
•	Source Systems: Power BI for data cleaning, modeling, analysis, and dashboard creation.
•	Data Volume: The dataset contains 45 bike stations
•	Storage Mode: Specify if using Import.
⚙️ Data Transformation (ETL)
•	Tool Used: Power Query Editor.
•	Key Cleanups: List standard transformations applied to raw data (e.g., merging, unpivoting).
•	Custom Functions: Mention any customized M code scripts used.
🧠 Data Model & DAX
•	Model Type: Star Schema.
•	Fact Tables: BIKE data tables.
•	Dimension Tables: Dim_station,Dim_date,Dim_time.
•	Key Measures:
•	Total Bike Stands = SUM ('BIKE DATA'[Bike Stands])
•	Total Available Bikes = SUM ('BIKE DATA'[Available Bikes])
•	Bike Usage = SUM ('BIKE DATA'[Bike Stands]) - SUM('BIKE DATA'[Available Bikes])
•	Bike Availability % = DIVIDE ([Total Available Bikes], [Total Bike Stands], 0 ) * 100
•	Open Stations = CALCULATE (COUNTROWS ('BIKE DATA'), 'BIKE DATA'[Status] = "OPEN”)
•	Closed Stations = CALCULATE (COUNTROWS ('BIKE DATA'), 'BIKE DATA'[Status] = "CLOSED”)

🖥️ Dashboard Features
Dashboard Features
                The dashboard presents a comprehensive overview of the bike-sharing system on a single page. It includes KPI cards, bar charts, line charts, a donut chart, a map, and interactive slicers to analyze bike availability, station status, bike usage, and trends by month and hour. Cross-filtering enables users to explore station performance and demand patterns efficiently.
💡 Key Insights
Trend A:
Bike usage is highest during peak commuting hours, indicating increased demand at specific times of the day.
Trend B:
Some stations have consistently low bike availability, suggesting the need for better bike redistribution.
Recommendation:
Redistribute bikes to high-demand stations during peak hours and continuously monitor station availability to improve service efficiency and customer satisfaction.

