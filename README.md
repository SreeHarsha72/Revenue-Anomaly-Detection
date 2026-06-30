# Revenue Anomaly Detection for Finance Business

## Project Overview

In this project, I built a revenue anomaly detection workflow for a finance-style business setting. The goal was to identify unusual revenue days,
understand whether they were positive spikes or negative drops, and explain the possible business reason behind each anomaly.

Instead of only saying "this day is abnormal," I focused on building a workflow that also answers:
-   Why the anomaly happened
-   What action the finance team should take next

## Business Case Background

Finance teams monitor daily revenue to identify unusual business events such as:
-   Marketing campaign spikes
-   Payment gateway failures
-   Refund spikes
-   Fraud or chargebacks
-   Data pipeline issues
-   Enterprise invoice bookings
-   Seasonal demand changes

This project automatically detects these anomalies and provides business-friendly explanations.


## Dataset and Tools

I created a synthetic daily revenue dataset covering January 2024 --June 2025.
- Tech Stack: Python, Pandas, NumPy, Matplotlib, Scikit-learn, Isolation Forest, Feature Engineering

## Project Workflow

### 1. Data Generation
I generated realistic finance data with business patterns including:

### 2. Exploratory Data Analysis

I analyzed:
-   Revenue trends
-   Revenue distribution
-   Weekly patterns
-   Summary statistics

### 3. Feature Engineering

Features include:
-   1-day and 7-day revenue lag
-   7-day and 30-day rolling averages
-   Revenue growth
-   Average order value
-   Refund rate
-   Failed payment rate
-   Chargeback rate
-   Weekend indicator
-   Month-start indicator

### 4. Z-Score Detection

A simple statistical baseline using:   |Z-score| > 3

### 5. Rolling Window Detection

Compared daily revenue against recent 30-day behavior to better handle seasonality and growth.

### 6. Isolation Forest

Machine learning anomaly detection using multiple business metrics rather than revenue alone.

### 7. Final Detection Logic

Combined rule-based detection with Isolation Forest to improve anomaly detection.

### 9. Model Evaluation

Performance on the synthetic dataset using metrics      
- Accuracy        
- Precision      
- Recall         
- F1 Score        

### 10. Final Output

The final report contains:
-   Date
-   Revenue metrics
-   Transactions
-   Refunds
-   Failed payments
-   Chargebacks
-   Marketing spend
-   Enterprise invoices
-   Anomaly score
-   Explanation
-   Severity
-   Recommended action

## Conclusion

I built this project to demonstrate an end-to-end revenue anomaly detection workflow that combines statistical techniques, machine learning, and business explanation logic to create practical, interpretable insights for finance teams.
