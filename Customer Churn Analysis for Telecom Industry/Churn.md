# Telecom Customer Churn Analysis

## Overview
This project focuses on analyzing and predicting customer churn in telecom services. The goal is to identify at-risk customers and provide actionable insights to develop targeted retention strategies, leveraging machine learning and data analytics.

### Business Value:
- Predict customer churn with high accuracy
- Proactively identify customers at risk of leaving
- Optimize retention strategies to reduce churn and improve customer lifetime value (CLV)

---

## Dataset Description
The dataset contains customer behavior and service usage metrics, including:

- **Anonymous Customer ID**: Unique identifier for each customer
- **Call Failures**: Number of dropped/failed calls
- **Complaints**: Binary (0: No complaint, 1: Complaint)
- **Subscription Length**: Total months of subscription
- **Charge Amount**: Ordinal (0: Lowest, 9: Highest)
- **Seconds of Use**: Total duration of calls
- **Frequency of Use**: Total number of calls
- **Frequency of SMS**: Total number of text messages
- **Distinct Called Numbers**: Unique numbers called
- **Age Group**: Ordinal (1: Younger, 5: Older)
- **Tariff Plan**: Binary (1: Pay-as-you-go, 2: Contractual)
- **Status**: Binary (1: Active, 2: Non-active)
- **Customer Value**: Calculated customer value
- **Churn**: Binary (0: Retained, 1: Churned) - Target variable

---

## Data Preprocessing
- **Balanced Dataset Creation**: 695 non-churned, 695 churned customers
- **SQL Database**: Created for aggregation queries
- **Feature Standardization**: For clustering analysis
- **Data Transformation**: Ensured compatibility with machine learning models

---

## Key Insights & Findings

### 1. **Customer Value vs. Churn**
- Non-churned customers show significantly higher customer value.
- Churned customers cluster around lower value points.
- **Customer value** is a strong indicator of retention likelihood.

### 2. **Subscription Length Patterns**
- Early subscription months (5-15) show elevated churn risk.
- Peak retention occurs around 35-40 months.
- Two distinct customer lifecycle phases observed.

### 3. **Usage Behavior**
- Churned customers predominantly show low usage (<2500 seconds).
- Non-churned customers display more varied usage patterns.
- High usage (>10,000 seconds) strongly correlates with retention.

### 4. **Complaints Impact**
- Strong positive correlation between complaints and churn.
- Critical intervention point for retention strategies.

---

## Correlation Analysis

- **Strongest Correlations with Churn**:
  - **Status** (0.61)
  - **Complaints** (0.49)
  - **Frequency of Use** (-0.45)
  - **Customer Value** (-0.45)
  - **Seconds of Use** (-0.44)

---

## Customer Segmentation (K-Means Clustering)

- **High-Value Users**: High usage, few complaints, long subscriptions
- **At-Risk Users**: Low usage, higher complaints, shorter subscriptions
- **Moderate Users**: Medium usage, varied complaint levels

---

## Machine Learning Models & Performance

**Random Forest Classification**:
- **Precision**: 97%
- **Recall**: 95%
- **F1-Score**: 96%
- **ROC-AUC**: 0.99

**Decision Tree Classification**:
- **Precision**: 94%
- **Recall**: 97%
- **F1-Score**: 96%
- **ROC-AUC**: 0.95

---

## Feature Importance

- **Top Churn Predictors**:
  1. **Status** (0.21) - Active/Non-active status
  2. **Complaints** (0.14) - Customer complaint history
  3. **Frequency of Use** (0.08) - Call volume
  4. **Seconds of Use** (0.07) - Call duration
  5. **Subscription Length** (0.07) - Tenure

---

## Risk Segmentation Framework

**Customer Risk Categories**:
- **High Risk** (>75% churn probability): Immediate intervention
- **Medium Risk** (25-75% churn probability): Proactive engagement
- **Low Risk** (<25% churn probability): Value enhancement

---

## Actionable Recommendations

1. **Complaint Resolution Enhancement**:
   - Implement 24-hour complaint resolution guarantee
   - Develop post-resolution satisfaction tracking

2. **Usage-Based Interventions**:
   - Create targeted offers for customers with <2500 seconds monthly usage
   - Develop service packages optimized for low-usage customers

3. **Subscription Milestone Program**:
   - Deploy special retention offers at months 10-15
   - Implement loyalty rewards at 12, 24, and 36-month milestones

4. **Tariff Plan Optimization**:
   - Review contractual vs. pay-as-you-go performance
   - Develop guided migration paths between plans

---

## Implementation Strategy

### Phase 1: Immediate Actions (0-3 months)
- Deploy predictive churn alerts for highest-risk customers
- Implement rapid response protocol for new complaints

### Phase 2: Process Integration (3-6 months)
- Integrate churn prediction models into customer service systems
- Launch subscription milestone intervention program

### Phase 3: Advanced Analytics (6-12 months)
- Implement real-time behavioral triggers
- Deploy dynamic pricing and promotion engine

---

## Expected Business Impact

- **5-8% reduction in overall churn rate**
- **15% improvement in high-value customer retention**
- **20% increase in Customer Lifetime Value**
- **ROI**: 3.5x return on retention program investment

---

## Requirements

- Python 3.x
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- SQL Database (optional)

---
