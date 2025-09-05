# Solar Power Forecasting – Week 2 Internship Project

## Project Overview
This project is part of the **AICTE Edunet Foundation Internship** under the theme **Sustainable Energy & Efficiency**. 
The goal of Week 2 is to **explore solar power generation data**, visualize trends, and analyze daily solar energy production.


## Dataset
The dataset contains solar power generation data from a solar plant:

| Column        | Description                                     |
|---------------|-------------------------------------------------|
| DATE_TIME     | Timestamp of the measurement                    |
| PLANT_ID      | Unique ID of the solar plant                    |
| SOURCE_KEY    | Panel/source identifier                         |
| DC_POWER      | Direct current power (kW)                       |
| AC_POWER      | Alternating current power (kW)                  |
| DAILY_YIELD   | Energy generated on that day (kWh)              |
| TOTAL_YIELD   | Cumulative energy generated (kWh)               |

**Files in the `data/` folder:**  
- `Plant_1_Generation_Data.csv` (used in Week 2 analysis)  
- Additional CSVs for future weeks/projects  


## Implementation
- Loaded and explored the solar power generation dataset using Pandas.  
- Checked dataset info, shape, and missing values.  
- Converted `DATE_TIME` to datetime format.  
- Plotted **daily solar power generation trends**.  
- Plotted **distribution of daily yield**.  
- Added observations summarizing key patterns in solar power generation.


## Observations
- Solar power generation varies day to day depending on weather conditions.  
- Peak generation occurs on sunny days; low or zero generation occurs at night.  
- Most daily yields are within a certain range, as seen in the histogram.


## Files
- `Solar_Forecasting_Week2.ipynb` → Colab notebook with code, plots, and observations  
- `data/` → Folder containing all CSV dataset files  


## Future Work
- Integrate **weather data** to improve solar power predictions.  
- Implement **machine learning models** for solar power forecasting.  
- Extend analysis to multiple plants and sources for comparative insights.  
