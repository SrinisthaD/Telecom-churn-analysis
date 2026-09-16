# Telecom Churn Data Profiling Report

This project generates an automated, interactive Exploratory Data Analysis (EDA) report for a **Telecom Churn dataset**. It uses `ydata-profiling` to evaluate data quality, analyze variable distributions, and identify correlations before building predictive models.

## 🚀 Features
* **Data Overview:** Summarizes missing values, duplicate rows, data types, and memory usage.
* **Variable Analysis:** Detailed analysis of every column (distribution, missing values, distinct values, and basic statistics).
* **Correlations & Interactions:** Auto-calculates correlation matrices (Pearson, Spearman, Phik, etc.) to reveal hidden relationships.
* **Missing Value Visualizations:** Easy-to-read charts showing the distribution and patterns of missing data.

## 📦 Requirements

Before running the script, ensure you have Python installed along with the following libraries:

```bash
pip install pandas ydata-profiling
```

## 🛠️ How to Use

1. Place your dataset (`telecom_churn.csv`) in the same directory as the script.
2. Run the script using Python:

```python
import pandas as pd
from ydata_profiling import ProfileReport

# Load the telecom churn dataset
df = pd.read_csv('telecom_churn.csv')

# Generate the profiling report
profile = ProfileReport(df, title="Data Report")

# Export the report as an interactive HTML file
profile.to_file("report.html")
```

## 📊 Output

* **`report.html`**: A standalone, interactive HTML document. Open this file in any modern web browser to explore your detailed data insights.
