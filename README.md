# 🍫 ChocoCrunch Analytics : Sweet Insights, Bitter Truths

A Comprehensive Data Analytics Project on Global Chocolate Products

## 📘 Overview

This project presents an end-to-end data analytics pipeline that focuses on the global chocolate market. The dataset was sourced using the OpenFoodFacts API, processed, cleaned, and stored in a structured MySQL database. The analysis and visualization are performed using Python, Pandas, and Streamlit, offering a clear understanding of chocolate nutritional profiles, brand performance, and ingredient trends.

The main objective is to explore chocolate products from a data-driven perspective — identifying health indicators, evaluating brand composition, and providing insights into nutritional diversity.

## 🎯 Objectives

- To collect and process chocolate-related product data through the OpenFoodFacts API.
- To perform data cleaning, feature engineering, and database creation using MySQL.
- To derive meaningful insights from the data using exploratory data analysis (EDA).
- To build an interactive Streamlit dashboard for dynamic visualization and user interaction.
- To classify chocolates based on calorie, sugar, and processing level categories.

## 🧩 Methodology

1. Data Extraction
- Source: OpenFoodFacts API
- Data Collected: Product name, brand, nutritional values, ingredients, additives, allergens, and processing level.
- Records Fetched: ~14,000+ global chocolate products.

2. Data Cleaning & Preprocessing
- Handled missing, inconsistent, and duplicate values.
- Standardized units for energy, sugar, and carbohydrates.
- Removed irrelevant attributes to maintain analytical focus.

3. Feature Engineering
New columns derived for better interpretability:
- sugar_to_carb_ratio
- calorie_category (Low / Moderate / High)
- sugar_category
- is_ultra_processed (based on NOVA classification)

4. Database Creation (MySQL)
Designed relational tables:
- product_info
- nutrient_info
- derived_metrics
- Data inserted and queried using Python’s SQLAlchemy connector.

5. Exploratory Data Analysis (EDA)
- Conducted descriptive analysis and summary statistics.
- Visualized calorie, sugar, and processing distributions using Matplotlib and Seaborn.
- Compared brand-level averages and correlations between nutrients.

6. Visualization (Streamlit App)
Built an interactive dashboard with:
- Brand-level comparisons
- Nutrient-based filtering
- Category-wise distributions
- Join-based query visualizations

## 🧠 Insights & Findings

- A significant number of chocolates are categorized as moderate to high in calories.
- Several popular brands show imbalanced sugar-to-carb ratios, indicating poor health value.
- Ultra-processed chocolates dominate global markets, highlighting health awareness concerns.

#### Exploratory Data Analysis & Visualizations
- Bar Charts: Number of products per calorie_category, top 10 brands by average calories.
- Pie Charts: Product distribution by NOVA classification (nova_group).
- Scatter Plots: Calories vs sugar content.
- Boxplots: Distribution of sugar_to_carb_ratio across brands.
- Treemaps: Product count by brand and calorie_category.
- Heatmaps: Correlation between calories, sugars, and fat.
- Stacked Bars & KPI Cards: Ultra-processed vs minimally 
- processed product counts, average calories, and sugars per brand.

All visualizations are interactive, making insights immediately actionable for decision-makers.

## ⚙️ Tech Stack

| Category            | Tools/Technologies             |
| ------------------- | ------------------------------ |
| **Programming**     | Python                         |
| **Data Processing** | Pandas, NumPy                  |
| **Database**        | MySQL                          |
| **Visualization**   | Streamlit, Matplotlib, Seaborn |
| **Integration**     | SQLAlchemy                     |
| **API Source**      | OpenFoodFacts                  |

## 🗂 File Structure & Descriptions

| File / Folder                 | Description                                                                                    |
| ----------------------------- | ---------------------------------------------------------------------------------------------- |
| `chococrunch_analytics.ipynb` | Main Jupyter Notebook showcasing full ETL, feature engineering, EDA, and visualizations.       |
| `choco_raw.csv`               | Raw data fetched directly from OpenFoodFacts API.                                              |
| `choco_cleaned.csv`           | Cleaned version of raw data with missing values handled.                                       |
| `choco_engineered.csv`        | Feature-engineered dataset with derived metrics and categories.                                |
| `sql_insertion.ipynb`         | Python script to create MySQL tables and insert processed CSV data into the database.          |
| `app.py`                      | Streamlit application for interactive dashboards, SQL query execution, and data visualization. |
| `.streamlit/secrets.toml`     | Secure storage of database credentials.                                                        |
| `requirements.txt`            | All Python dependencies for running ETL, EDA, SQL insertion, and Streamlit dashboards.         |

## 🚀 Getting Started

#### Prerequisites
- Python 3.10+
- MySQL Database (running locally or on a server)
- Git

#### Clone Repository
```
https://github.com/Maryam-Feroz/-ChocoCrunch-Analytics.git
cd ChocoCrunch-Analytics
```

#### Install Dependencies
```
pip install -r requirements.txt
```
#### Configure Secrets
Create .streamlit/secrets.toml with your MySQL credentials:
```
[database]
db_host="127.0.0.1"
db_user="root"
db_password="your_password"
db_name="choco_crunch"
```
#### Run the Streamlit App
```
streamlit run app.py
```
The app will open in your default browser at ```http://localhost:8501```.

## 📝 Usage

- ETL & SQL Insertion: Fetch raw chocolate product data, clean, engineer features, and populate MySQL tables.
- Exploratory Analysis: Explore distributions, correlations, and derived metrics using visualizations.
- Interactive Insights: Run predefined SQL queries and filter products by brand, sugar, calorie, or processing level.
- Dashboards: Visualize trends using bar charts, pie charts, scatter plots, treemaps, heatmaps, and KPI cards.

## 🚀 Future Enhancements

- Implement machine learning models to predict calorie or sugar categories.
- Integrate a recommendation system for “healthier chocolate alternatives.”
- Deploy the Streamlit app on Streamlit Cloud or HuggingFace Spaces.
- Expand dataset coverage across different countries and timeframes.

## 🤝 Contributing

- Fork the repository.
- Create a new branch for your feature or bug fix.
- Commit and push your changes.
- Open a pull request to the main branch.
- Ensure all code follows project style and includes documentation.




















