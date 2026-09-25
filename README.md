# churn_analysis
Churn analysis of the customer stopping buying/ stopping subscription of a product or service.

Churn Analysis & Customer Intelligence

1. The Business ChallengeIn the hyper-competitive OTT landscape (Netflix, Hotstar, Prime), retention is the only way to act as a Data Analyst tasked with identifying high-risk subscribers using a multi-dimension demographics, Subscription tiers, and Support escalations).

2. Core Tech StackSQL & Python Integration (numpy, pandas, sqlite3, matplotlib, seaborn), Performance cleaning, feature engineering, analytics), Behavioral Visualization, Writing Actionable.

3. Project MilestonesRelational Data Extraction: Connecting Python to SQL databases to pull multi-table datasets.Advanced Feature Engineering: Data imports, calculating tenure, churn rates, and customer aging.Executive Reporting: Translating technical findings into billion-dollar business insights.Note: This isn't just a coding exercise, it's a business solution. You'll leave with a portfolio-ready project applicable to E-commerce, SaaS, Fintech and Adtech industries.



Observations by Churn Risk Segment

Low Churn Risk
• Points cluster at the lower end of monthly_charges (~10-20) for Standard and Basic plans.
• Premium plan customers in this facet show one clear high outlier (~$90/month) alongside a tighter cluster
around $20-25.
• Basic plan customers here have the lowest charges observed in the entire chart (~$5-10).
High Churn Risk
• Charges are more evenly spread across Standard, Premium, and Basic plans, roughly in the $10-25 range.
• No extreme outliers are visible in this facet - high-risk customers appear concentrated in a narrower charge
band than low-risk customers.
• Both plotted genders appear represented across Standard and Basic plans in this segment.
Mid Churn Risk
• Sparsest facet - only two points are visible (one Standard, one Premium), both in the $15-25 range.
• Too few points to draw any pattern; likely an artifact of how few customers fall into this segment, or a small
overall sample.
Preliminary Insights
1 Premium-plan volatility: The one high-value outlier (~$90) sits in the Low churn-risk facet on a Premium
plan - tentatively suggesting higher-spend Premium customers are not automatically higher churn risks.
This is a single data point, not a trend.
2 Basic plan = lowest spend, mixed risk: Basic-plan customers appear at the lowest charge levels in both
Low and High risk facets, suggesting monthly_charges alone may not strongly separate Basic-plan churn
risk.
3 No obvious linear relationship: Higher monthly_charges doesn't consistently track with higher or lower
churn risk - risk segments overlap substantially in the same charge range ($10-25).
4 Gender split: Both colors (genders) appear in most facets without one dominating a particular risk level,
though the sample is too small to confirm this holds at scale.
5 Mid-risk underrepresentation: The Mid-risk facet has visibly fewer points than Low or High - worth
checking whether this reflects true class balance or a filtering artifact.
Recommended Next Steps
• Export the full dataset (not just the chart) and re-run this analysis with actual counts, churn rate %, and
confidence intervals.
• Add a churn rate by segment table (count and % of customers who churned, by plan_type and churn_risk).
• Bring in additional features - tenure, contract length, support interactions, payment method.
• Run a proper statistical test (chi-square or logistic regression) instead of relying on a single scatter plot.
• Check class balance across churn_risk categories - the Mid-risk facet looks sparse relative to Low/High.
• Re-generate this chart with jitter or point transparency (alpha) to reduce overplotting on the real dataset.


Summary
The available chart shows customer monthly_charges split by plan_type, churn_risk, and gender, but reflects
only ~15-20 visible data points - not enough to draw statistically sound churn conclusions. What can be said
directionally: churn risk levels overlap heavily in the same charge range, Basic-plan customers cluster at the
lowest spend regardless of risk level, and one Premium-plan outlier suggests spend alone doesn't cleanly
predict risk. To turn this into an actionable churn analysis, the next step is pulling the full underlying dataset and
re-running the analysis with actual churn rates, sample sizes, and additional behavioral features rather than a
single bivariate chart
