# 🌞 Solar Power Forecasting (Week 2 Project)

## Project Overview
This project uses **solar power plant generation and weather sensor data** to predict AC Power output using machine learning.  

**Objective:** Forecast daily energy generation based on historical data and weather features.

**Dataset:**  
- Plant 1 & Plant 2 Generation Data (`AC_POWER`, `DC_POWER`, `DAILY_YIELD`, `TOTAL_YIELD`)  
- Plant 1 & Plant 2 Weather Data (`AMBIENT_TEMPERATURE`, `MODULE_TEMPERATURE`, `IRRADIATION`)  

---

## Workflow

### 1️⃣ Data Preprocessing
- Converted `DATE_TIME` to datetime objects.  
- Merged generation and weather data for each plant.  
- Combined datasets for both plants.  
- Filled missing values with median; dropped rows missing `DATE_TIME`.  

### 2️⃣ Exploratory Data Analysis (EDA)
- **Daily AC Power Trend:** Line plot to observe daily total power generation.  
- **Distribution of AC Power:** Histogram to check range and frequency.  
- **Correlation Analysis:** Heatmap to study relationships between weather features and AC Power.  

### 3️⃣ Feature Selection
- Selected features:  
  - `DC_POWER`  
  - `AMBIENT_TEMPERATURE`  
  - `MODULE_TEMPERATURE`  
  - `IRRADIATION`  
- Target variable: `AC_POWER`

### 4️⃣ Model Training
- Trained **Linear Regression** and **Random Forest Regressor** models.  
- Split dataset into **80% train / 20% test**.  

### 5️⃣ Model Evaluation
- Evaluated models using:  
  - **MAE (Mean Absolute Error)**  
  - **MSE (Mean Squared Error)**  
  - **RMSE (Root Mean Squared Error)**  
  - **R² Score**

**Model Performance Comparison:**

| Model               | MAE     | MSE      | RMSE  | R² Score |
|--------------------|---------|----------|-------|----------|
| Linear Regression  | 73.24   | 24219.20 | 155.53| 0.89     |
| Random Forest      | 0.20    | 4.95     | 2.22  | 1.00     |

> Random Forest outperformed Linear Regression in predicting AC Power.

### 6️⃣ Feature Importance
- Random Forest shows **IRRADIATION** as the most influential feature.  
- DC Power, Ambient Temperature, and Module Temperature also contribute to predictions.  

---

## Visualizations
- Daily AC Power trend line plot  
- AC Power distribution histogram  
- Correlation heatmap  
- Predicted vs Actual scatter plots for Linear Regression and Random Forest  

---

## Saved Model
- Trained Random Forest model saved as: `rf_ac_power_model.pkl`  
- Can be used for prediction without retraining.

---

## Observations & Insights
- AC Power shows **seasonal trends** with occasional peaks.  
- Random Forest provides **higher accuracy** with minimal error.  
- IRRADIATION is the key predictor of AC Power.  

---

## Future Work
- Explore **advanced models** like Gradient Boosting, XGBoost, or LSTM for better forecasting.  
- Deploy interactive **prediction app** using Streamlit, Gradio, or Flask.  
- Include additional panel/weather features to improve model accuracy.  

---

## How to Run
1. Clone the repository:  
   ```bash
   git clone <your-repo-url>
2.Install dependencies:

  ```bash
  pip install -r requirements.txt
```

3. Open the notebook (`.ipynb`) in **Google Colab** or **Jupyter Notebook**.  
4. Run all cells step by step to reproduce results and visualizations.  
5. Use the saved Random Forest model (`rf_ac_power_model.pkl`) to make predictions **without retraining**.

---

## Requirements
Create a `requirements.txt` file with the following packages for easy setup:

pandas
numpy
matplotlib
seaborn
scikit-learn
joblib


---

## Folder Structure (Example)
Solar-Power-Forecasting/
│
├── Plant_1_Generation_Data.csv
├── Plant_2_Generation_Data.csv
├── Plant_1_Weather_Sensor_Data.csv
├── Plant_2_Weather_Sensor_Data.csv
├── Solar_Power_Forecasting_Week2.ipynb
├── rf_ac_power_model.pkl
├── requirements.txt
└── README.md


---

## Author
**Prachi Manwar** – [Your GitHub Profile](https://github.com/prachi134-hash)  

---

## License
This project is open-source and available under the MIT License.  
