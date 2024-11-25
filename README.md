# Flight Delays Analysis using PySpark in Databricks

## Objective

This project demonstrates an end-to-end data analysis pipeline using PySpark in Databricks, focused on analyzing and modeling flight delays data. The dataset contains information on flight delays, cancellations, and causes from various airlines. The key goals are to clean, explore, and analyze the data while extracting actionable insights.

---

## Dataset

The project uses the **Flight Delays and Cancellations** dataset, which includes:
- Airline operations data.
- Flight delay and cancellation details.
- Causal factors for delays and cancellations.

---

## Steps in the Analysis

### 1. Data Loading and Initial Exploration
- **Data Import**: The dataset was imported into Databricks and loaded into a PySpark DataFrame.
- **Exploration**: The schema, sample data, and overall structure were reviewed to understand the dataset.
- **Key Questions**:
  - How many rows and columns does the dataset contain?
  - What are the data types of each column?

---

### 2. Data Cleaning and Transformation
- **Handling Missing Values**: 
  - Columns with excessive missing values (over 50%) were dropped, excluding critical columns like `CANCELLATION_REASON`.
  - Remaining missing values were imputed where applicable.
- **Feature Engineering**:
  - New features like `DAY_OF_WEEK`, `MONTH`, and a binary `DELAYED` column (based on `ARRIVAL_DELAY > 0`) were created.
- **Key Questions**:
  - Which columns had missing values, and how were they handled?
  - What new features were created, and why?

---

### 3. Exploratory Data Analysis (EDA) using Spark SQL
- **SQL Queries**: 
  - Average delay time by airline.
  - Top 5 airports with the most delayed departures.
  - Analysis of cancellation reasons.
- **Visualization**:
  - Patterns of delays by day of the week or month.
  - Average delays by airline.
- **Key Questions**:
  - Which airlines had the highest average delays?
  - What patterns were observed in delays by day of the week?

---

### 4. Summary and Insights
- Airlines with the highest delays and common patterns were identified.
- Cancellation reasons were categorized:
  - **B**: Airline/Carrier-related issues.
  - **A**: Administrative/Operational airline issues.
  - **C**: Weather conditions.
- Temporal trends and factors affecting flight delays were highlighted.

---

## Technologies Used

- **PySpark**: For data processing and feature engineering.
- **Spark SQL**: For querying and analyzing the data.
- **Databricks**: As the integrated development environment.
- **Visualization Tools**: Databricks visualizations and `matplotlib` for generating insights.

---

## Project Deliverables

- **Databricks Notebook**: Contains all code, analysis, and outputs.
- **Summary Report**: Key findings and insights from the analysis.
- **Visualizations**: Charts and graphs illustrating trends and patterns.

---

