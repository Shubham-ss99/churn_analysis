Project Case Study: Subscription Churn Analysis & Customer Intelligence


1. Executive Summary

Customer churn analysis quantifies the rate at which customers terminate their subscriptions or cease transactions with a business. In hyper-competitive subscription markets—such as the Over-the-Top (OTT) streaming sector (e.g., Netflix, Disney+ Hotstar, Amazon Prime)—retention serves as the primary engine for sustainable revenue growth.

This project establishes a data-driven framework to identify high-risk subscribers by analyzing multi-dimensional datasets, including user demographics, subscription tiers, billing histories, and customer support escalation logs.


2. Core Technical Stack

The analysis integrates relational database management with advanced data science workflows to transform raw data into operational business intelligence:

Data Extraction & Engineering: SQL (sqlite3), pandas, and numpy for multi-table relational joins, data cleaning, feature extraction, and cohort aging.
Behavioral Visualization: matplotlib and seaborn for exploratory data analysis (EDA) and multi-facet risk distribution mapping.
Strategic Reporting: Execution of actionable executive summaries connecting technical metrics to business outcomes.

3. Project Milestones & Methodology

Relational Data Extraction: Establishing secure connections between Python environments and SQL databases to extract, clean, and merge disparate operational tables.
Advanced Feature Engineering: Calculating key customer metrics including operational tenure, historical churn velocities, billing variances, and customer lifetime value (CLV) aging.
Executive Reporting: Translating statistical models and data visualizations into high-impact, portfolio-ready business insights applicable across SaaS, Fintech, E-commerce, and Adtech ecosystems.


Exploratory Data Analysis: Key Observations by Risk Segment

A preliminary exploratory analysis was conducted using a multi-faceted scatter plot cross-referencing monthly_charges, plan_type, churn_risk, and gender. Due to a highly constrained initial sample size (~15–20 visible data points), these observations represent directional hypotheses rather than statistically validated conclusions.


Churn Risk Segment	Observed Billing & Plan Distributions	Key Findings & Vulnerabilities
Low Risk	• High concentration of Standard and Basic plans within the low-tier pricing band (~$10–$20/month).
• Basic plans occupy the absolute lowest cost floor ($5–$10/month).	• High-Value Retention: A notable Premium plan outlier maintains a high monthly spend (~$90) without demonstrating elevated risk indicators.
High Risk	• Dense concentration across all three major tiers (Basic, Standard, Premium) strictly bound within a narrow pricing corridor ($10–$25/month).	• Compressed Risk Band: High-risk accounts are heavily tightly packed; extreme pricing outliers are notably absent from this segment.
Mid Risk	• Severe data sparsity with only two recorded observations (one Standard plan, one Premium plan) falling between $15–$25/month.	• Sample Limitation: The segment is too sparse to establish valid behavioral patterns, indicating potential data filtering issues or severe class imbalance.


Preliminary Strategic Insights

Premium Tier Volatility Insulation: The presence of a high-value Premium outlier (~$90/month) within the low-risk segment tentatively indicates that top-tier billing levels do not automatically accelerate customer churn.
Basic Plan Price Insensitivity: Basic-tier subscribers cluster tightly at the lowest pricing thresholds across both high and low-risk segments. This indicates that monthly charge amounts alone are insufficient indicators for predicting churn within budget tiers.
Non-Linear Risk Correlations: Churn risk does not scale linearly with pricing. Significant overlap exists across all risk classifications within the core $10–$25 pricing spectrum.
Demographic Equity: Gender distributions appear uniformly distributed across all risk categories and subscription tiers, suggesting gender is not a primary driver of subscriber attrition at this scale.


Data Optimization & Next Steps

To transform these initial exploratory findings into an enterprise-grade predictive model, the following technical steps are required:

Dataset Scalability & Validation: Extract the complete relational database to validate counts, calculate precise churn percentages per segment, and calculate tight confidence intervals.
Segmented Retention Matrices: Construct comprehensive churn matrix tables tracking absolute counts and percentage distributions broken down by plan_type and churn_risk.
Feature Expansion: Integrate deeper behavioral features into the model pipeline, specifically subscriber tenure, contract structures, support ticket frequencies, and historical payment methods.
Statistical Modeling: Advance beyond bivariate visualizations by running rigorous statistical verification, including Chi-Square tests for categorical independence and Logistic Regression for directional risk modeling.
Class Imbalance Resolution: Audit the underlying data structure to determine if the sparsity of the Mid-Risk segment is an artifact of upstream data filtering or a true reflection of the population distribution.
Visualization Enhancement: Re-render the exploratory charts using point-jittering and alpha-transparency to eliminate overplotting and accurately display high-density data clusters.
