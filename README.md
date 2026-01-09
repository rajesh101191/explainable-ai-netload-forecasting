
<p align="center">
  <img src="A_banner_image_for_Explainable_AI–Driven_Net-Load.png" alt="Explainable AI – Net-Load Forecasting Banner" width="100%">
</p>
# Explainable AI–Driven Net-Load Forecasting for the Indian Power System

This repository contains the complete workflow for an **explainable AI (XAI) based net-load forecasting framework** for the Indian grid.  
Python is used for data engineering, ML model training and SHAP-based explainability, while MATLAB is used for AGC–LFC simulations using the forecasted net load.

---

## 🌍 Overview

- **Region:** India  
- **Goal:** Build accurate and explainable **day-ahead / multi-step net-load forecasts** and analyse the drivers using SHAP.
- **Inputs**
  - NASA-POWER reanalysis weather data (GHI, temperature, wind, etc.)
  - VRE generation reports (solar + wind)
- **Outputs**
  - Cleaned master dataset and feature matrix
  - Trained ML models and performance metrics
  - SHAP-based global & local explanations
  - Figures and tables used in the manuscript
  - MATLAB AGC–LFC simulation results driven by the forecast.

---

## 📁 Repository Structure

```text
Data/                      # Raw and merged input datasets (NASA + VRE)
Python_Code/               # Jupyter notebooks for ML & XAI
m-file/                    # MATLAB script for AGC–LFC simulations
Output_of_XAI/             # All processed datasets and figures
    ├── CSV_Outputs/       # Final & intermediate Excel/CSV files
    ├── JPG_Outputs/       # Final plots used in the paper
    └── pre_analysis_outputs/
          ├── CSV/         # Summary stats, missingness, correlation tables
          └── JPG/         # EDA plots & pre-analysis figures
## 📂 External VRE Dataset (linked from previous project)

To avoid duplication, all VRE (solar + wind) reports used in this project are stored in the related repository:

🔗 **VRE Data Folder**  
https://github.com/rajesh101191/inertia-trading-grid-stability/tree/main/Data/VRE

These include:
- Daily solar/wind summary files  
- Cleaned VRE datasets  
- Final merged VRE profile used for correlation & feature creation  

🧪 Methods
Data Engineering


Merge multi-year NASA-POWER daily time-series with VRE generation data.

Handle missing values, outliers and seasonal patterns.

Generate ML feature matrix (lags, rolling statistics, calendar features, weather-VRE interactions).

Main notebook: Python_Code/XAI_Driven_Load_Forecasting.ipynb
Pre-analysis exports: Output_of_XAI/pre_analysis_outputs/

Forecasting Models

Tree-based ensemble models (e.g. Random Forest, XGBoost / Gradient Boosting)

Baseline statistical models for comparison

Evaluation using MAE, RMSE, MAPE and coverage of prediction intervals.

Additional experiments: Python_Code/XAI_Part_2.ipynb

Explainable AI (XAI)

Notebook: Python_Code/Shap_Analysis.ipynb

Global feature importance (mean |SHAP| values)

Partial dependence style SHAP plots

Time-local explanations for extreme days (high VRE ramp, heat waves, etc.)

Interaction analysis between weather variables, VRE output and net load.

All SHAP figures are saved inside Output_of_XAI/JPG_Outputs/.

MATLAB AGC–LFC Simulation

Script: m-file/run_AGC_JOURNAL_CASE1.m

Reads forecasted net load profile from CSV/Excel.

Runs AGC–LFC simulation for a multi-area power system.

Evaluates impact of forecast scenarios on frequency and tie-line power.

▶️ How to Run
1. Python environment
pip install -r requirements.txt


Recommended key packages (if you create requirements.txt):

pandas, numpy, scikit-learn, matplotlib, seaborn

xgboost (if used)

shap

jupyter

Then:

Open XAI_Driven_Load_Forecasting.ipynb

Run all cells to generate cleaned datasets and trained models.

Open Shap_Analysis.ipynb to reproduce the XAI plots.

2. MATLAB

Open m-file/run_AGC_JOURNAL_CASE1.m in MATLAB.

Make sure the forecast output file path is correctly set.

Run the script to generate AGC–LFC response plots.

📊 Key Outputs

Output_of_XAI/CSV_Outputs/final_master_dataset*.xlsx – final modelling dataset

Output_of_XAI/CSV_Outputs/ml_feature_matrix_daily.xlsx – ML feature matrix

Output_of_XAI/JPG_Outputs/ – final figures (EDA, SHAP, time-series composites, etc.)

Output_of_XAI/pre_analysis_outputs/ – summary statistics and correlation analysis.

📄 Data Source Acknowledgement

NASA-POWER data: https://power.larc.nasa.gov/

VRE / net-load data: [Add the official source link here when you publish].

🔖 Citation

If you use this code or workflow in your research, please cite:

R. Kumar, Explainable AI–Driven Net-Load Forecasting for Renewable-Rich Indian Power Systems, [working paper / under review].

📜 License

Add your preferred license here (e.g., MIT, Apache-2.0) or state “For academic use only” if you don’t want unrestricted reuse.
# explainable-ai-netload-forecasting
Explainable AI–driven net-load forecasting for the Indian grid using NASA-POWER weather data, VRE reports, Python (XGBoost/ML models + SHAP) and MATLAB AGC–LFC simulations.
