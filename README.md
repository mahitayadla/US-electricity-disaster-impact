### Electricity Revenue & Risk Across U.S. States (2024)

This project analyzes how extreme weather and disaster events impact electricity revenue and economic pressure across U.S. states. By combining federal disaster data with electricity revenue metrics, the dashboard helps stakeholders understand where infrastructure and revenue are most exposed to climate-related risk.

---

## Data Sources

All datasets are publicly available government data:

- **FEMA Disaster Declarations**  
Federal Emergency Management Agency (FEMA). 
OpenFEMA Dataset: Disaster Declarations Summaries – V2.
Public domain U.S. government data.   
https://www.fema.gov/openfema-data-page/disaster-declarations-summaries-v2


- **NOAA Storm Events Database (2024 – Locations File)**  
  National Centers for Environmental Information (NCEI), NOAA.  
  File: StormEvents_locations-ftp_v1.0_d2024_c20251204.csv.gz  
  Public domain U.S. government data.  
  https://www.ncei.noaa.gov/pub/data/swdi/stormevents/csvfiles/


- **U.S. Energy Information Administration (EIA)**  
  State-level electricity revenue, sales, and customer data
  Dataset: Sales_Ult_Cust_2024 (2024 final data)
  Public domain U.S. government data.  
  https://www.eia.gov/electricity/data/eia861/

---

## Technologies Used

- **Python** (Pandas, NumPy)
- **Jupyter Notebook**
- **Tableau Cloud**
  - Parameters
  - Calculated fields
  - Interactive dashboards
- **Public Federal APIs & Open Data**

---

## Data Preprocessing (Python)

All preprocessing was done using **Python (Pandas, NumPy)** in Jupyter notebooks.

Key steps included:

1. **Filtering to 2024 data** across all datasets for consistency
2. **Cleaning damage fields**  
   - Converted NOAA property and crop damage values from string formats (K, M, B) into numeric values
3. **Feature engineering**
   - Aggregated extreme events and disaster declarations by state
4. **State-level aggregation**
   - Grouped all metrics by `State` and `Year`
5. **Dataset integration**
   - Merged FEMA, NOAA, and EIA datasets into a single state-level analytical table

The final dataset was exported as a clean CSV (tableau_dataset.csv) for visualization.

---

## Tableau Dashboard

The final analysis was built in **Tableau Cloud** and includes:

- **Interactive U.S. map** showing disaster-driven risk by state
- **KPI cards** highlighting key metrics such as:
  - Extreme Event Count
  - Economic Stress Index
  - Total Electricity Revenue
- **Dynamic filters and parameters**
  - State selection
  - Metric focus for exploration
- **Calculated fields**
  - Economic stress Index
  - Property Damage(%)
  - Crop Damage(%)

---

## Purpose & Impact

This project demonstrates how environmental risk translates into economic pressure for electricity providers and infrastructure planners. It supports:

- Risk assessment for utilities
- State-level infrastructure planning
- Disaster preparedness and investment prioritization

---


## Future Improvements

With more time, this project could be expanded by:
- Adding **multi-year trend analysis**
- Modeling **predictive risk scenarios**

---


## Notes

Raw datasets were accessed directly from official public sources and are not stored in this repository. All transformation logic is documented in the notebooks.
