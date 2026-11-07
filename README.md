
# Explainable AI–Driven Net-Load Forecasting for the Indian Power System

<p align="center">
  <img src="https://img.shields.io/badge/Research-Explainable%20AI-blue?style=for-the-badge" alt="Explainable AI"/>
  <img src="https://img.shields.io/badge/Domain-Smart%20Grid-green?style=for-the-badge" alt="Smart Grid"/>
  <img src="https://img.shields.io/badge/Python-Machine%20Learning-yellow?style=for-the-badge&logo=python&logoColor=white" alt="Python"/>
  <img src="https://img.shields.io/badge/MATLAB-AGC--LFC-orange?style=for-the-badge" alt="MATLAB"/>
</p>

<p align="center">
  <a href="https://ieeexplore.ieee.org/document/11485825">
    <img src="https://img.shields.io/badge/IEEE-Xplore-00629B?style=for-the-badge&logo=ieee&logoColor=white" alt="IEEE Xplore"/>
  </a>
  <a href="https://journals.stmjournals.com/tee/article=2026/view=246108/">
    <img src="https://img.shields.io/badge/STM-Journals-245A83?style=for-the-badge" alt="STM Journals"/>
  </a>
</p>

This repository contains the complete research workflow for an **Explainable Artificial Intelligence (XAI)-based net-load forecasting framework for the Indian power system**.

The framework integrates weather information, variable renewable energy (VRE) generation data, machine learning models, and SHAP-based explainability to investigate net-load forecasting under increasing renewable energy penetration.

Python is used for data engineering, machine learning model development, forecasting, and explainability, while MATLAB is used for Automatic Generation Control (AGC) and Load Frequency Control (LFC) simulations using forecasted net-load profiles.

---

## 📚 Published Research Publications

This research repository is associated with the following published research papers.

### 1. IEEE Publication

**Explainable AI Framework for Net-Load Forecasting in Renewable-Rich Indian Grids**

<p>
  <a href="https://ieeexplore.ieee.org/document/11485825">
    <img src="https://img.shields.io/badge/IEEE%20Xplore-Read%20Publication-00629B?style=for-the-badge&logo=ieee&logoColor=white" alt="Read on IEEE Xplore"/>
  </a>
</p>

- **Publisher:** IEEE
- **Publication Platform:** IEEE Xplore
- **Document ID:** 11485825
- **Paper:** [View Published Paper](https://ieeexplore.ieee.org/document/11485825)

### 2. STM Journals Publication

**Integrated Explainable Forecasting and Metaheuristic PI Optimization for LFC/AGC**

<p>
  <a href="https://journals.stmjournals.com/tee/article=2026/view=246108/">
    <img src="https://img.shields.io/badge/STM%20Journals-Read%20Publication-245A83?style=for-the-badge" alt="Read on STM Journals"/>
  </a>
</p>

- **Journal:** Trends in Electrical Engineering
- **Publisher:** STM Journals
- **Year:** 2026
- **Volume:** 16
- **Issue:** 02
- **Pages:** 26–32
- **Authors:** Neha Khurana, Chetan Yadav, Gopal Krishan, Rajesh Kumar
- **Publication:** [View Published Article](https://journals.stmjournals.com/tee/article=2026/view=246108/)

---

## 🌍 Project Overview

**Region:** India

**Research Objective:** Develop accurate and explainable day-ahead and multi-step net-load forecasting models and investigate the major factors influencing net-load variations.

### Input Data

- NASA-POWER reanalysis weather data (Global Horizontal Irradiance, temperature, wind, etc.).
- Variable Renewable Energy (VRE) generation reports (solar and wind).
- Historical power-system data and derived net-load profiles.

### Expected Outputs

- Cleaned and integrated master datasets.
- Machine learning feature matrices.
- Trained forecasting models and performance metrics.
- SHAP-based global and local explanations.
- Research figures and tables.
- MATLAB-based AGC–LFC simulation results driven by forecasted net load.

---

## 📁 Repository Structure

```text
explainable-ai-netload-forecasting/
│
├── Data/
│   └── Raw and merged input datasets
│       (NASA-POWER and related data)
│
├── Python_Code/
│   ├── XAI_Driven_Load_Forecasting.ipynb
│   ├── XAI_Part_2.ipynb
│   └── Shap_Analysis.ipynb
│
├── m-file/
│   └── run_AGC_JOURNAL_CASE1.m
│
├── Output_of_XAI/
│   ├── CSV_Outputs/
│   ├── JPG_Outputs/
│   └── pre_analysis_outputs/
│       ├── CSV/
│       └── JPG/
│
├── README.md
└── LICENSE
```

---

## 📂 External VRE Dataset

To avoid duplication, the solar and wind Variable Renewable Energy (VRE) reports used in this project are maintained in the related repository:

**VRE Data Repository:**

[Inertia Trading and Grid Stability – VRE Data](https://github.com/rajesh101191/inertia-trading-grid-stability/tree/main/Data/VRE)

The repository contains:

- Daily solar and wind summary files.
- Cleaned VRE datasets.
- Final merged VRE profiles used for correlation analysis and feature creation.

---

## 🧪 Research Methodology

### 1. Data Engineering and Pre-processing

- Integration of multi-year NASA-POWER daily weather time-series with VRE generation data.
- Missing-value treatment and outlier analysis.
- Investigation of seasonal and temporal patterns.
- Development of machine learning feature matrices.

**Feature Engineering Includes:**

- Lag features.
- Rolling statistical features.
- Calendar-based features.
- Weather and VRE interaction features.

**Main Notebook:**

`Python_Code/XAI_Driven_Load_Forecasting.ipynb`

**Pre-analysis Outputs:**

`Output_of_XAI/pre_analysis_outputs/`

### 2. Net-Load Forecasting Models

The forecasting framework investigates tree-based ensemble learning algorithms and baseline statistical approaches.

**Machine Learning Models:**

- Random Forest.
- XGBoost.
- Gradient Boosting.
- Other baseline forecasting models.

**Performance Evaluation Metrics:**

- Mean Absolute Error (MAE).
- Root Mean Square Error (RMSE).
- Mean Absolute Percentage Error (MAPE).
- Prediction interval coverage, where applicable.

**Additional Experiments:**

`Python_Code/XAI_Part_2.ipynb`

### 3. Explainable Artificial Intelligence (XAI)

SHAP (SHapley Additive exPlanations) is used to interpret the forecasting models and investigate the contribution of individual features.

**Notebook:**

`Python_Code/Shap_Analysis.ipynb`

**Explainability Analysis Includes:**

- Global feature importance using mean absolute SHAP values.
- SHAP summary and dependence plots.
- Time-local explanations for extreme operating conditions.
- Analysis of high VRE ramp events and heat-wave conditions.
- Interaction analysis between weather variables, VRE generation, and net load.

All SHAP figures are saved in:

`Output_of_XAI/JPG_Outputs/`

### 4. MATLAB-Based AGC–LFC Simulation

The forecasting framework is further connected to power-system frequency control studies through MATLAB-based AGC–LFC simulations.

**MATLAB Script:**

`m-file/run_AGC_JOURNAL_CASE1.m`

**Simulation Workflow:**

- Reads forecasted net-load profiles from CSV/Excel files.
- Executes AGC–LFC simulations for a multi-area power system.
- Investigates the impact of forecast scenarios on system frequency.
- Evaluates tie-line power responses.
- Analyses the influence of renewable-rich net-load variations on frequency regulation.

---

## ▶️ How to Run the Project

### 1. Python Environment Setup

Install the required Python packages:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn
pip install xgboost shap jupyter
```

**Recommended Environment:**

- Python 3.x
- Jupyter Notebook
- NumPy
- Pandas
- Scikit-learn
- XGBoost
- SHAP
- Matplotlib
- Seaborn

**Execution Steps:**

1. Clone or download this repository.
2. Install the required Python libraries.
3. Open `XAI_Driven_Load_Forecasting.ipynb`.
4. Execute the notebook cells to generate cleaned datasets and train forecasting models.
5. Open `XAI_Part_2.ipynb` to reproduce additional experiments.
6. Open `Shap_Analysis.ipynb` to generate explainability plots.

### 2. MATLAB Environment

**Recommended:** MATLAB with compatible scripting and plotting functionality.

**Execution Steps:**

1. Open MATLAB.
2. Navigate to the `m-file` directory.
3. Open `run_AGC_JOURNAL_CASE1.m`.
4. Verify that the forecast output file paths are correctly configured.
5. Execute the script.
6. Generate and analyse the AGC–LFC frequency and tie-line power response plots.

---

## 📊 Key Research Outputs

| Directory / File | Description |
|---|---|
| `Output_of_XAI/CSV_Outputs/` | Processed datasets and feature matrices |
| `final_master_dataset*.xlsx` | Final modelling dataset |
| `ml_feature_matrix_daily.xlsx` | Machine learning feature matrix |
| `Output_of_XAI/JPG_Outputs/` | Final research figures and SHAP plots |
| `Output_of_XAI/pre_analysis_outputs/` | Statistical summaries and correlation analysis |
| `m-file/` | MATLAB AGC–LFC simulation scripts |

---

## 📡 Data Sources and Acknowledgements

### NASA-POWER

Weather and solar radiation data are obtained from the NASA Prediction of Worldwide Energy Resources (POWER) project.

[https://power.larc.nasa.gov/](https://power.larc.nasa.gov/)

### VRE and Net-Load Data

Solar and wind generation reports are maintained in the associated project repository.

[Access VRE Dataset](https://github.com/rajesh101191/inertia-trading-grid-stability/tree/main/Data/VRE)

Official net-load data source and additional data acknowledgements can be added as applicable.

---

## 📖 Citation

If you use this repository, its code, or the associated research workflow in your academic work, please refer to the published research articles listed above.

### IEEE Publication

[View IEEE Xplore Publication](https://ieeexplore.ieee.org/document/11485825)

### STM Journals Publication

[View STM Journal Publication](https://journals.stmjournals.com/tee/article=2026/view=246108/)

Please consult the respective publisher pages for the complete bibliographic citation and DOI information.

---

## 👨‍💻 Research and Development

**Dr. Rajesh Kumar**

Research Interests:

- Explainable Artificial Intelligence (XAI).
- Machine Learning and Deep Learning.
- Renewable Energy Integration.
- Net-Load Forecasting.
- Smart Grids and Power System Stability.
- Automatic Generation Control (AGC).
- Load Frequency Control (LFC).
- AI-Driven Power System Optimization.

**GitHub:** [@rajesh101191](https://github.com/rajesh101191)

---

## 📜 License

This repository is distributed under the MIT License.

See the [LICENSE](LICENSE) file for details.

---

<p align="center">
  <b>Explainable AI | Renewable Energy | Smart Grids | Power System Stability</b>
</p>

<p align="center">
  Developed for research and academic advancement in intelligent and renewable-rich power systems.
</p>
Explainable AI–driven net-load forecasting for the Indian grid using NASA-POWER weather data, VRE reports, Python (XGBoost/ML models + SHAP) and MATLAB AGC–LFC simulations.
