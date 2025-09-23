# Telco Customer Churn Prediction & Insights

**Using Data Science & Explainable AI to Identify High-Risk Customers and Boost Retention**

![Hero Thumbnail](images/churn-dashboard.png)

---

## Concept / Problem

Telecom companies lose millions annually due to customer churn. Predicting which customers are likely to leave helps companies proactively retain them.  
In this project, I developed a predictive model to identify high-risk customers and provide actionable insights to reduce churn while protecting recurring revenue.

---

## Approach

1. **Exploratory Data Analysis (EDA):** Understand patterns in churn, tenure, and service usage.  
2. **Feature Engineering:** Created derived features like tenure groups, total services, and high charges flags.  
3. **Modeling:** Tested Logistic Regression, Random Forest, and XGBoost. Selected the best-performing model based on accuracy, precision, recall, and ROC-AUC.  
4. **Explainability:** Used SHAP values to identify key features driving churn for each customer.  
5. **Business Insights:** Calculated expected saved revenue and suggested targeted retention strategies.

![Process Flow](images/workflow_diagram.png)

---

## Data

The dataset consists of 7,043 telecom customers with features like gender, seniority, service usage, contract type, payment method, and monthly charges.  

**Key variables:**
- `tenure`, `MonthlyCharges`, `TotalCharges`  
- Contract & Payment Type  
- Service usage flags (Online Security, Streaming, Tech Support)  
- Target variable: `Churn` (Yes/No)

![Dataset Snapshot](images/data-overview.png)

---

## Key Insights & Visuals

- **Churn Drivers:** Customers with Fiber-optic internet, month-to-month contracts, or electronic check payments are more likely to churn.  
- **Demographics:** Senior citizens and customers without partners or dependents have higher churn rates.  
- **Revenue Opportunity:** Targeting high-risk customers can potentially save ~$145,000 in annual revenue.

### Screenshots Carousel
<div class="carousel">
  <img src="images/key-influencers.png" alt="Key Influencers Visual">
  <img src="images/top10_highrisk.png" alt="Top 10 High-Risk Customers">
  <img src="images/pie_chart_contract.png" alt="Churn by Contract Type">
  <img src="images/line_chart_tenure.png" alt="Tenure vs Churn Probability">
</div>

---

## Code & Dashboard

- Notebook snippets: EDA, Feature Engineering, Model Training  
- Power BI dashboard: Key Influencers, customer segmentation, churn probabilities  
- SHAP feature importance visuals

![Code Snippet](images/code_snippet.png)
![Dashboard Screenshot](images/dashboard_screenshot.png)

---

## Impact / Results

**Model Performance:**
- Accuracy: 80%  
- Precision: 65%  
- Recall: 52%  
- ROC-AUC: 0.84  

**Business Impact:**
- Identified 684 high-risk customers  
- Expected saved revenue: $145,095 if retention campaigns are applied successfully

![KPIs](images/kpi_dashboard.png)

---

## Links

- **GitHub Repository:** [View on GitHub](https://github.com/yourusername/telco-churn)  
- **Medium Article:** [Read on Medium](https://medium.com/@yourusername/telco-churn-analysis)  

---

### Optional Features for GitHub Pages

- Use `<details>` to toggle code snippets for cleaner layout:
```html
<details>
<summary>View Feature Engineering Code</summary>

```python
# Example snippet
df['tenure_group'] = pd.cut(df['tenure'], bins=[0, 12, 24, 36, 48, 60, 72], labels=['0-12','13-24','25-36','37-48','49-60','61+'])
