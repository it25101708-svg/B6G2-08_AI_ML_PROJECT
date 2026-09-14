# Project Overview: Warsaw Daily Weather Data Analysis

This project implements an end-to-end Machine Learning preprocessing and analysis pipeline using the Warsaw Daily Weather Dataset. The pipeline handles essential data preprocessing steps such as missing data imputation, outlier detection and handling, data transformation, feature encoding, and feature scaling.

## Repository Structure

```text
B6G2-08_AI_ML_PROJECT/
├── data/
│   ├── external/            # Third-party data sources
│   └── raw/                 # Original, immutable datasets
├── notebooks/               # Jupyter notebooks for data analysis and preprocessing
│   ├── IT25101533_Missing_Data.ipynb
│   ├── IT25101708_Encoding.ipynb
│   ├── IT25103406_Outliers.ipynb
│   └── IT25103602_Scaling.ipynb
├── results/                 # Generated outputs, logs, and visual results
│   ├── eda_visualizations/  # Charts and graphs from Exploratory Data Analysis
│   ├── logs/                # Execution logs
│   └── outputs/             # Processed datasets and models
└── README.md                # Project documentation
```

## Dataset Details

**Dataset Name:** Warsaw Daily Weather Dataset
**Source:** [Kaggle](https://www.kaggle.com/datasets/mateuszk013/warsaw-daily-weather) (originally from Climate Data Online)

This dataset includes 30 years (1993-2022) of daily weather measurements in Warsaw, Poland. It is highly suitable for time series analysis and regression tasks like ARIMA and RNN models for weather forecasting.

**Columns:**
- `DATE` - Measurement date (YYYY-MM-DD)
- `STATION` - Station ID
- `NAME` - Station name
- `LATITUDE` - Station latitude
- `LONGITUDE` - Station longitude
- `ELEVATION` - Station elevation
- `PRCP` - Precipitation
- `SNWD` - Snow depth
- `TAVG` - Average temperature
- `TMAX` - Maximum temperature
- `TMIN` - Minimum temperature

## Getting Started

1. **Clone the repository:**
   ```bash
   git clone https://github.com/it25101708-svg/B6G2-08_AI_ML_PROJECT.git
   cd B6G2-08_AI_ML_PROJECT
   ```

2. **Environment Setup:**
   Ensure you have Python installed along with common data science libraries (`pandas`, `numpy`, `scikit-learn`, `matplotlib`, `seaborn`, `jupyter`).

3. **Running the Notebooks:**
   Open the Jupyter notebooks in the `notebooks/` directory and execute the cells to see the preprocessing steps in action. The individual notebooks cover:
   - Handling Missing Data (`IT25101533`)
   - Feature Encoding (`IT25101708`)
   - Outlier Detection and Handling (`IT25103406`)
   - Feature Scaling (`IT25103602`)

## Team Members and Contributions

* **IT25101533 - PERERA D.T.M** - Missing Data Handling
  * **Task:** Impute missing `SNWD` (snow depth) and temperature values.
  * **EDA:** Bar chart of missing counts before and after imputation.
  * **File Name:** `IT25101533_Missing_Data.ipynb`
* **IT25101708 - KURUPPU R.A.L** - Feature Encoding
  * **Task:** Extract seasons from `DATE` and apply One-Hot Encoding.
  * **EDA:** Bar chart of seasonal frequencies.
  * **File Name:** `IT25101708_Encoding.ipynb`
* **IT25102520 - NIRMAL W A D D T** - Data Transformation
  * **Task:** Apply log transformation to fix heavily skewed `PRCP` data.
  * **EDA:** Histogram before and after transformation.
  * **File Name:** `IT25102520_Transformation.ipynb`
* **IT25103406 - RATHNAYAKE R.M.M.M** - Outliers Detection & Handling
  * **Task:** Remove extreme `PRCP` or `TMAX` values using IQR or Z-score.
  * **EDA:** Boxplot before and after outlier removal.
  * **File Name:** `IT25103406_Outliers.ipynb`
* **IT25103602 - THIDASVIN R.K.P.L** - Normalization & Scaling
  * **Task:** Apply Min-Max or Standard Scaling to numerical columns.
  * **EDA:** Histogram before and after scaling.
  * **File Name:** `IT25103602_Scaling.ipynb`
* **IT25100613 - JAYATHILAKE K A V S** - Feature Selection
  * **Task:** Remove redundant correlated temperature columns.
  * **EDA:** Correlation Matrix Heatmap.
  * **File Name:** `IT25100613_Feature_Selection.ipynb`
