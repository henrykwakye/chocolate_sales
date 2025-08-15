
## Project Objectives
1. Clean and preprocess the dataset to handle inconsistencies and prepare it for advanced analysis.
2. Perform statistical analysis to test hypotheses about sales patterns (e.g., regional preferences).
3. Cluster salespeople based on performance metrics to identify distinct profiles.
4. Build a time-series model to forecast monthly sales.
5. Create an interactive dashboard to visualize insights dynamically.

# Advanced Chocolate Sales Analysis Project

This advanced project challenges you to analyze the `Chocolate Sales.csv` dataset to derive deep insights through statistical analysis, machine learning, and interactive visualizations. The project is designed for someone proficient in Python and data science, providing open-ended problems for you to solve independently. No solutions are provided—your task is to develop the code and interpret the results.

## Project Overview

The `Chocolate Sales.csv` dataset contains sales records with the following columns:
- **Sales Person**: Name of the salesperson.
- **Country**: Country of sale (e.g., UK, India).
- **Product**: Chocolate product sold (e.g., Mint Chip Choco).
- **Date**: Sale date (format: DD-MMM-YY).
- **Amount**: Sales amount (e.g., $5,320).
- **Boxes Shipped**: Number of boxes shipped (integer).

Your goal is to uncover patterns, build predictive models, and create interactive tools to explore sales dynamics. The project includes five tasks, each with specific questions to guide your analysis.

## Setup Instructions

1. **Environment**:
   - Use Python 3.8+ in a Jupyter notebook (recommended) or script.
   - Install libraries: `pandas`, `numpy`, `scikit-learn`, `statsmodels`, `plotly`, `dash`, `matplotlib`, `seaborn`.
   - Command: `pip install pandas numpy scikit-learn statsmodels plotly dash matplotlib seaborn`.

2. **Dataset**:
   - Save `Chocolate Sales.csv` in your working directory.
   - Load the dataset using `pandas.read_csv()`.

3. **Deliverables**:
   - Save all plots as PNG files.
   - Save any cleaned or processed datasets as CSV files.
   - Create a 1-page report (Markdown or notebook cell) summarizing your findings.
   - For interactive components, provide instructions to access them (e.g., Dash app URL).

## Task 1: Data Cleaning and Feature Engineering

**Objective**: Prepare the dataset for advanced analysis by cleaning inconsistencies and creating new features.

**Questions to Solve**:
- How will you handle missing or invalid values in `Amount`, `Date`, or `Boxes Shipped`? For example, what should you do with negative `Boxes Shipped` or non-numeric `Amount` values?
- How can you clean the `Date` column to ensure consistent formatting? What if some dates are malformed?
- Create at least three new features, such as:
  - Price per box (`Amount` / `Boxes Shipped`).
  - Day of the week or month of sale.
  - A categorical feature (e.g., high vs. low sales based on a threshold).
- How will you detect and handle outliers in `Amount` or `PricePerBox` (e.g., using IQR or z-scores)?

**Deliverable**:
- Save the cleaned dataset as `cleaned_chocolate_sales.csv`.
- Write a brief note in your report on any data quality issues you encountered.

## Task 2: Statistical Hypothesis Testing

**Objective**: Investigate whether sales patterns differ significantly across groups (e.g., countries or products).

**Questions to Solve**:
- Test the hypothesis: “Average sales amounts differ significantly by country.” What statistical test will you use (e.g., ANOVA, Kruskal-Wallis)? Why?
- If differences exist, which countries contribute most? How can you perform a post-hoc analysis to identify specific pairs?
- Test another hypothesis, such as: “Price per box varies significantly by product.” What test is appropriate, and how will you interpret the results?
- How will you account for multiple testing (e.g., Bonferroni correction)?

**Deliverable**:
- Print or save the test results (e.g., p-values, test statistics).
- Include a plot (e.g., boxplot of `Amount` by `Country`) to visualize differences.
- Summarize findings in your report, noting any surprising patterns.

## Task 3: Salesperson Performance Clustering

**Objective**: Group salespeople into performance-based clusters to identify distinct profiles.

**Questions to Solve**:
- What metrics will you use to cluster salespeople (e.g., total sales, average boxes shipped, transaction count)?
- Which clustering algorithm will you choose (e.g., KMeans, DBSCAN)? How will you standardize features?
- How will you determine the optimal number of clusters (e.g., elbow method, silhouette score)?
- After clustering, how will you characterize each cluster (e.g., “high-volume sellers”)? What visualizations will help?

**Deliverable**:
- Save a scatter plot of clusters (e.g., total sales vs. average boxes) as `salesperson_clusters.png`.
- Save a table summarizing cluster characteristics (e.g., mean metrics per cluster).
- Discuss cluster insights in your report.

## Task 4: Time-Series Sales Forecasting

**Objective**: Predict future monthly sales using a time-series model.

**Questions to Solve**:
- How will you aggregate sales data to a monthly level? What challenges might arise with sparse or irregular dates?
- Which time-series model will you use (e.g., ARIMA, Prophet, LSTM)? Why?
- How will you validate your model (e.g., train-test split, cross-validation)? What metric will you use (e.g., RMSE, MAPE)?
- Forecast sales for the next 6 months. How will you visualize historical vs. predicted values?

**Deliverable**:
- Save a plot of historical and forecasted sales as `sales_forecast.png`.
- Report the model’s performance metrics (e.g., RMSE).
- Discuss forecast reliability in your report.

## Task 5: Interactive Sales Dashboard

**Objective**: Build an interactive dashboard to explore sales data dynamically.

**Questions to Solve**:
- What visualizations will you include (e.g., bar chart of sales by country, line chart of monthly trends)?
- How will you allow users to filter data (e.g., dropdowns for country or product)?
- Which library will you use (e.g., Dash, Streamlit)? How will you structure the app?
- How will you ensure the dashboard is responsive and user-friendly?

**Deliverable**:
- Deploy the dashboard (e.g., Dash app running at `http://127.0.0.1:8050`).
- Provide instructions in your report to access and use the dashboard.
- Save a screenshot of the dashboard as `dashboard_screenshot.png`.

## Bonus Challenge: Open-Ended Exploration

Choose one or more of the following to deepen your analysis:
- **Predictive Modeling**: Build a regression model to predict `Amount` based on features like `Country`, `Product`, and `DayOfWeek`. Which features are most important?
- **Anomaly Detection**: Identify unusual transactions (e.g., high `Amount` with low `Boxes Shipped`). What algorithm will you use (e.g., Isolation Forest)?
- **Regional Preferences**: Are certain products preferred in specific countries? Use a statistical test (e.g., chi-squared) to analyze `Product` vs. `Country`.

**Deliverable**:
- Include findings in your report, with supporting plots or tables.

## Report Guidelines

Write a 1-page report summarizing:
- Key findings from each task.
- One surprising insight (e.g., an unexpected cluster or regional trend).
- Challenges you faced and how you addressed them.
- Suggestions for future analysis (e.g., new features or models).

Save the report as `chocolate_sales_report.md` or include it in your notebook.

## Tips
- Start by exploring the dataset with `df.info()` and `df.describe()`.
- Test code on a small subset to iterate quickly.
- Save intermediate results (e.g., processed data, model outputs).
- Use `plotly` for interactive plots to enhance your dashboard.
- Document your code with comments to track your approach.