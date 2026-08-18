# 🏡 California Housing Data Analysis & EDA

An end-to-end Exploratory Data Analysis (EDA) project investigating the classic 1990 California Housing dataset. This project uncovers geographical pricing trends, demographic correlations, and feature distributions using Python and data visualization libraries.

---

## 📌 Project Overview
* **Goal**: To clean, analyze, and visualize housing metrics across California districts to understand the primary drivers of median house values.
* **Scope**: Analysis of 20,640 block groups in California, focusing on features like location, median income, housing age, and total rooms.
* **Tech Stack**: Python 3.10+, Pandas, NumPy, Matplotlib, Seaborn, Google Colab.

---

## 📂 Data Source

* **Dataset**: `housing.csv` (Sourced from the Hands-On Machine Learning repository).
* **Key Features**: 
  * `longitude`, `latitude`: Geographical coordinates of the block group.
  * `housing_median_age`: Median age of houses in the district.
  * `total_rooms`, `total_bedrooms`: Room counts per district.
  * `population`, `households`: Demographic density metrics.
  * `median_income`: Median income of residents (measured in tens of thousands of US Dollars).
  * `median_house_value`: Target variable representing the median house price.
  * `ocean_proximity`: Categorical feature indicating distance to the ocean.

---

## ⚙️ Key Data Pipeline & Engineering Steps

1. **Data Acquisition**: Automated direct download from the official raw repository to bypass localized pathing issues.
2. **Data Cleaning**: 
   * Identified and handled missing values (e.g., nulls in the `total_bedrooms` column).
   * Verified data types and cleaned categorical constraints.
3. **Exploratory Data Analysis (EDA)**:
   * **Distribution Analysis**: Plotted histograms to detect right-skewed data and artificial data caps (e.g., clipped median house values at $500,000).
   * **Geographical Mapping**: Built high-density scatter plots utilizing latitude and longitude to map house values and population density across the state.
   * **Correlation Matrix**: Analyzed the Pearson correlation coefficient between median income and house values.

---

## 📊 Key Findings & Insights

* **Income vs. Value**: `median_income` is the strongest predictor of `median_house_value`, showing a prominent positive correlation.
* **Geographical Premium**: Houses located near the ocean (e.g., Bay Area, Los Angeles, San Diego) command significantly higher prices compared to inland districts.
* **Data Artifacts**: Visible horizontal lines in scatter plots reveal artificial price capping in the original data collection process at $500,000.

---

## 🚀 How to Run the Project

### Run via Google Colab (Recommended)
1. Open `housing_eda.ipynb` in [Google Colab](https://colab.research.google.com/).
2. Click `Runtime` $\rightarrow$ `Run all`. The notebook is configured to automatically fetch the dataset and generate all visualizations.

### Run Locally
```bash
# Clone the repository
git clone [https://github.com/keerthi-180205/california-housing-eda.git](https://github.com/keerthi-180205/california-housing-eda.git)
cd california-housing-eda

# Install required dependencies
pip install pandas numpy matplotlib seaborn

# Launch Jupyter Notebook
jupyter notebook housing_eda.ipynb
