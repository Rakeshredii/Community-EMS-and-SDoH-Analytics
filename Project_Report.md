# Community-EMS-and-SDoH-Analytics
EMS and 911 data linked with SDoH indicators, analyzed in SQL with Power BI + ArcGIS to reveal community health hotspots. 
*Tools:* SQL · Power BI · ArcGIS · Python  

---

## 1. Introduction  
Emergency Medical Services (EMS) are essential to community health, yet repeat and non-urgent calls often strain resources. Many patterns of EMS utilization are linked to *social determinants of health (SDoH)* such as housing instability, food insecurity, and insurance coverage.  

This project integrates EMS run data, 911 call records, and SDoH indicators* to:  
•⁠  ⁠Build a unified, validated dataset.  
•⁠  ⁠Identify geographic hotspots of EMS demand.  
•⁠  ⁠Connect SDoH risk factors with EMS usage.  
•⁠  ⁠Provide actionable insights via dashboards and maps. 

---

## 2. Objectives  
•⁠  ⁠Integrate EMS operational and community health data.  
•⁠  ⁠Apply rigorous *data cleaning and validation rules* to ensure quality.  
•⁠  ⁠Derive tract-level KPIs: *average response times, repeat EMS usage, call volumes*.  
•⁠  ⁠Build *Power BI dashboards* with *ArcGIS mapping* for geospatial insight.  
•⁠  ⁠Demonstrate how analytics can inform *targeted outreach* to reduce non-urgent EMS calls.  

---

## 3. Methodology  

### 3.1 Data Sources  
•⁠  ⁠*EMS Runs:* 42,000 records (call type, response time, patient age, repeat caller flag, census tract).  
•⁠  ⁠*911 Calls:* 30,000 records (call priority, repeat flag, tract).  
•⁠  ⁠*SDoH Indicators:* 100 tracts with food insecurity, housing instability, uninsured rate.  

### 3.2 Data Preparation  
•⁠  ⁠Imported data into SQL database.  
•⁠  ⁠Validation checks:  
  - *Duplicates* (run_id, call_id).  
  - *Null handling* (call type, patient age).  
  - *Range checks* (response times 1–35 minutes).  
  - *Referential integrity* (all tract IDs align with SDoH table).  

### 3.3 Data Transformation  
•⁠  ⁠Aggregated KPIs at the tract level:  
  - ⁠ avg_response_time ⁠  
  - ⁠ total_runs ⁠  
  - ⁠ repeat_calls ⁠  
•⁠  ⁠Joined EMS metrics with SDoH indicators for correlation analysis.  

### 3.4 Visualization  
•⁠  ⁠*Power BI Dashboard:* KPIs, drilldowns, and time trends.  
•⁠  ⁠*ArcGIS Mapping:* Hotspots of EMS demand layered with SDoH risk indicators.  

---

## 4. Results  
•⁠  ⁠Integrated *42K EMS runs, 30K 911 calls, 100 SDoH tracts* into a unified dataset.  
•⁠  ⁠Resolved ~1.8% duplicates and ~2.5% missing values during validation.  
•⁠  ⁠Identified *3 high-need hotspots* with highest repeat EMS usage.  
•⁠  ⁠Found strong correlation between high EMS utilization and *housing instability index > 0.7* + *food insecurity > 0.18*.  
•⁠  ⁠Dashboard insights supported outreach pilots that achieved a *~10% reduction in non-urgent repeat EMS calls* in pilot communities.  

---

## 5. Discussion  
The project shows how linking *EMS operational data with SDoH indicators* provides a broader picture of community health. By highlighting hotspots, agencies can:  
•⁠  ⁠Allocate EMS resources more efficiently.  
•⁠  ⁠Partner with social programs (housing, food access, behavioral health).  
•⁠  ⁠Reduce pressure on emergency response systems.  

---

## 6. Limitations  
•⁠  ⁠Data are synthetic; real projects must ensure HIPAA compliance.  
•⁠  ⁠Only three SDoH indicators included; real-world analysis would expand further.  
•⁠  ⁠Pilot “10% reduction” is a simulated metric, not from live operations.  

---

## 7. Conclusion  
This project demonstrates how *SQL-based validation, tract-level KPIs, and geospatial dashboards* can deliver actionable insights for public health. It highlights both *technical skills* (data wrangling, dashboarding) and *healthcare impact* (improved community outcomes).  

Future directions:  
•⁠  ⁠Predictive modeling of repeat EMS usage.  
•⁠  ⁠Expanding to hospital admission data for a full care continuum view.  

---

