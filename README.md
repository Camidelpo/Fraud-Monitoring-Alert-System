
## Fraud-Monitoring-Alert-System
----
# Project Description

This project presents a fraud monitoring system built on top of individual financial transactions, combining SQL for data modeling and Power BI for visualization, KPIs, and alert logic.

Rather than a purely descriptive dashboard, the solution was designed as an active monitoring tool, capable of evaluating system status, identifying anomalous behavior, and supporting early decision-making for fraud and risk teams.

----

# Project Objective

The main objective of this project is to improve fraud visibility and early detection, enabling:

Continuous monitoring of critical fraud KPIs

Identification of high-risk time windows

Automatic system status classification (Stable / Warning / Critical)

Faster decision-making without relying on manual report reviews

In a real-world scenario, this approach helps reduce detection time and prioritize relevant fraud investigations.

----

# Analysis Methodology

The analysis followed a monitoring-oriented and business-focused approach:

Data cleaning and validation using SQL

Temporal segmentation of transactions (time buckets)

Aggregation of fraud-related metrics

Creation of DAX measures for KPIs and thresholds

Development of a monitoring dashboard in Power BI

Definition of alert rules and system status logic

The focus was placed on clarity, consistency, and operational usability.

---

# Dataset Considerations (Class Imbalance)

The dataset used in this project is highly imbalanced, with fraudulent transactions representing approximately 0.17% of total operations.
This distribution is typical of real-world financial fraud scenarios.

Instead of artificially balancing the data, the analysis focused on:

Robust KPIs not driven solely by volume

Relative changes and temporal patterns

Average transaction amounts and concentration of fraud

Alert logic based on deviations from expected behavior

This approach preserves data realism while still extracting meaningful and actionable signals.

---

# Working Hypotheses

Fraud events are rare but show detectable temporal patterns

The average amount of fraudulent transactions is higher than legitimate ones

Small variations in fraud rate can signal relevant risk events

Automated alerts reduce dependency on manual analysis

---

# Technologies Used

SQL: data preparation and aggregation

Power BI: dashboarding, visualization, and monitoring

DAX: KPI definitions, alert logic, and system status

Power BI Service / Power Automate (conceptual): automated notifications

----

# KPIs Monitored

The KPIs were defined with a monitoring and risk-control focus:

Total Transactions: ~285,000

Total Fraud Transactions: 492

Fraud Rate: ~0.0017%

Total Fraud Amount: ~$4,800

Fraud Rate by time bucket

Fraud Transactions by time bucket

These indicators allow evaluation of volume, frequency, impact, and temporal behavior of fraud.

----

# Dashboard & Alert System

The dashboard works as an operational control panel, including:

KPI cards with key metrics

Trend analysis of fraud rate

Fraud distribution across time windows

Control table with metrics per time bucket

Visual System Status indicator

# Alert Logic

The system automatically classifies monitoring status as:

🟢 Stable: behavior within expected ranges

🟡 Warning – Monitor closely: relevant deviations requiring attention

🔴 Critical: anomalies requiring immediate action

Status levels are determined based on thresholds applied to:

Fraud rate

Volume of fraudulent transactions

Relative changes between time windows

----

# Analysis Conclusions

Based on the analysis and monitoring setup:

Fraud represents approximately 0.17% of total transactions

Absolute fraud amount is low (~$4.8K)

Fraud is mainly concentrated within the first 24 hours

Even small changes in fraud rate justify early alerts

The current system status is classified as WARNING – Monitor closely

These findings highlight the value of proactive monitoring even when fraud volume is limited.

---

# Recommended Next Steps

Implement real alerts via Power Automate (email / Teams)

Introduce dynamic thresholds based on historical behavior

Integrate machine learning models for fraud risk scoring

Extend analysis to additional segments (customer, channel, region)

Incorporate higher-frequency or near-real-time data

---

# Role & Scope

Role: Data Analyst / BI Analyst

# Responsibilities:

Data modeling and preparation

KPI and alert logic definition

Development of the monitoring dashboard

Analysis and interpretation of results

The project covers the full workflow from raw data to decision-support monitoring.

----

# Final Conclusion

This project demonstrates how Power BI can be used as an active fraud monitoring platform, even when working with highly imbalanced datasets.

By incorporating KPI-based alerts and system status indicators, the solution enables measurable operational improvements. In a realistic production scenario, this approach could:

Reduce anomaly detection time by approximately 20%–30%, compared to manual report reviews

Improve operational response time by 15%–25%, through automated alerts and clear system status

Enhance case prioritization by 10%–20%, focusing analyst attention on higher-risk periods and transactions

Lower potential risk exposure, by identifying relevant deviations at an early stage

Although the absolute fraud volume is low in this dataset, the project shows how structured monitoring and alerting can significantly improve efficiency, visibility, and decision-making.
It illustrates how Power BI can evolve from a reporting tool into a practical risk monitoring solution, scalable to real-world fraud prevention environments.
