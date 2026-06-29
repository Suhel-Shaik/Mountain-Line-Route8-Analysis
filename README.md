# Mountain Line Transit — Route 8 Passenger Demand Analysis & Predictive Modeling
 
**Capstone Project | Master of Science in Business Analytics | Northern Arizona University**
 
## Project Overview
 
This project was developed in partnership with **Mountain Line**, the public transit authority of Flagstaff, AZ. The core objective was to analyze Route 8 bus stop activity and passenger flow data, identify stops that do not align with defined stop waypoints, and build a predictive model to forecast daily passenger demand.
 
The analysis covers two months of ridership data (November–December) across 15 defined stops along Route 8, which runs from the Downtown Connection Center through the Rt. 66 corridor to NAU and surrounding neighborhoods.
 
> **95% of analytical results were validated and aligned with expectations by Mountain Line stakeholders and faculty advisors.**
 
---
 
## Key Results
 
| Metric | Value |
|---|---|
| Predictive Model Correlation (r) | **0.946** |
| Model RMSE | 17.937 |
| Total Defined Stop Records | 21,915 |
| Total Undefined Stop Records | 1,033 |
| Weekday Ridership (passengers on) | 5,559 |
| Weekend Ridership (passengers on) | 1,259 |
| Highest-Volume Stop | Downtown Connection Center (3,121 stops) |
| Peak Ridership Period | PM Peak (1,598 passengers off) |
 
---
 
## Analyses Conducted
 
- **Passenger Demand Analysis** — Stop-level boarding and alighting volumes across the full route
- **Peak Time Analysis** — Ridership segmented by hour type (PM Peak, Midday, Peak Shoulder, Early PM, Late Morning, Evening, Early Peak)
- **Weekday vs. Weekend Analysis** — Volume comparison showing weekday ridership ~4.4× higher than weekends
- **Trend Analysis** — Daily passenger flow tracked across November and December
- **Undefined Stop Identification** — Flagged 1,033 records where passenger activity occurred outside defined stop waypoints
- **Stop-Level Geo Analysis** — Geospatial passenger mapping using GeoPandas (Python)
- **Predictive Modeling** — Linear regression model trained on November data and validated against December actuals
---
 
## Predictive Model Approach
 
The model predicts daily passenger boardings (`passengers_on`) using temporal features.
 
**Training data:** November 2025 (aggregated daily)  
**Test data:** December 2025 (out-of-sample validation)
 
**Features used:**
- `day_of_week` — captures weekly ridership patterns
- `day_of_month` — captures within-month trends
**Algorithm:** Linear Regression (scikit-learn + RapidMiner)
 
**Workflow:**
1. Filter November data → aggregate to daily totals
2. Engineer time-based features
3. Train Linear Regression model (80/20 train-test split within November)
4. Save model → apply to December data
5. Compare predictions against actual December ridership
---
 
## Tools & Technologies
 
| Tool | Purpose |
|---|---|
| **Python** (pandas, numpy, scikit-learn) | Data processing and predictive modeling |
| **RapidMiner** | Visual ML workflow and model validation |
| **GeoPandas** | Geospatial stop-level demand analysis |
| **Power BI** | Interactive dashboards and visuals |
| **Excel** | Data cleaning and route data management |
 
---
 
## Repository Contents
 
| File | Description |
|---|---|
| `Route_8_-_Capstone_Project.xlsx` | Full ridership dataset (Nov–Dec) with stop-level records |
| `Python_Predictive_Model.docx` | Complete Python code for the predictive model (Google Colab) |
| `Predictive_Models_-_Description.docx` | Step-by-step methodology for both RapidMiner and Python models |
| `Rapid_Miner_and_Python_-_Screenshots.docx` | Screenshots of model outputs and RapidMiner workflow |
| `Visuals_Report.pdf` | Power BI charts — passenger trends, peak hours, stop demand, distributions |
| `Route_8_Map.pdf` | Route 8 bus stop map with all 15 stops and intersection types |
| `Mountain_Line_Project_PPT.pptx` | Full project presentation delivered to Mountain Line stakeholders |
 
---
 
## Route 8 Stop Network
 
Route 8 serves 15 defined stops along the Rt. 66 corridor in Flagstaff, AZ:
 
1. Downtown Connection Center / Mountain Line Headquarters *(highest volume)*
2. Rt. 66 / Riordan Rd. (The Standard)
3. Rt. 66 / Pinnacle St.
4. Rt. 66 / Thompson St. (Maverik)
5. Rt. 66 / Railroad Spring Blvd.
6. Rt. 66 / Northwestern St. (Hidden Hollow)
7. Woody Mountain Rd. / Patio del Presidio
8. Rt. 66 / Northwestern St. (Wildwood Hills)
9. Rt. 66 / Railroad Spring Blvd. (Kit Carson)
10. Thompson St.
11. University Av. / Forest Meadows St. (True North Dentistry)
12. Woodlands Village Blvd. / University Av.
13. Rt. 66 / Woodlands Village Blvd. (Doubletree)
14. Rt. 66 / Metz Walk
15. Milton Rd. / Butler Av. (NAU)
---
 
## Author
 
**Suhel Shaik (Larkin)**  
M.S. Business Analytics | Northern Arizona University  
[Portfolio](https://suhelshaikportfolio.netlify.app)
 
---
 
*This project was completed as part of the NAU Franke College of Business capstone program in collaboration with Mountain Line Transit, Flagstaff, AZ.*
