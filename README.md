# 🍫 ChocoCrunch Analytics : Sweet Insights, Bitter Truths

A complete chocolate product analytics platform with ETL, SQL insights, and interactive dashboards using Python and Streamlit.

## 📣 Problem Statement

You’re a Data Analyst at a nutrition research firm analyzing the global chocolate market. The goal of this project is to:
- Extract chocolate product data from the OpenFoodFacts API.
- Clean, transform, and enrich the data with derived nutritional metrics.
- Store the processed data in a SQL database for querying and analysis.
- Perform Exploratory Data Analysis (EDA) and SQL-based insights.
- Visualize findings interactively through Streamlit dashboards.

## 📊 Business Use Cases

- Identify calorie and sugar-heavy chocolate products.
- Track ultra-processed chocolate trends via NOVA classification.
- Compare brands based on healthiness (calories & sugar).
- Categorize products based on derived calorie and sugar classes.
- Provide interactive dashboards for stakeholders to explore product insights.

## ✨ Key Features

#### ETL Pipeline
- Fetches 14,496+ chocolate products from OpenFoodFacts API.
- Cleans raw data, imputes missing values, standardizes units.
- Creates derived metrics: sugar_to_carb_ratio, calorie_category, sugar_category, and is_ultra_processed.
- Saves three versions: raw, cleaned, and engineered CSV datasets.

#### Database & SQL Insights
- Inserts processed data into a MySQL database.
- Includes predefined queries for average nutrient values, brand-wise product counts, ultra-processed analysis, and more.
- Enables dynamic SQL querying for stakeholder analysis.

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

## 🗂 File Structure & Descriptions

| File / Folder                 | Description                                                                                    |
| ----------------------------- | ---------------------------------------------------------------------------------------------- |
| `chococrunch_analytics.ipynb` | Main Jupyter Notebook showcasing full ETL, feature engineering, EDA, and visualizations.       |
| `choco_raw.csv`               | Raw data fetched directly from OpenFoodFacts API.                                              |
| `choco_cleaned.csv`           | Cleaned version of raw data with missing values handled.                                       |
| `choco_engineered.csv`        | Feature-engineered dataset with derived metrics and categories.                                |
| `sql_insertion.py`            | Python script to create MySQL tables and insert processed CSV data into the database.          |
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

## 🤝 Contributing

- Fork the repository.
- Create a new branch for your feature or bug fix.
- Commit and push your changes.
- Open a pull request to the main branch.
- Ensure all code follows project style and includes documentation.




















