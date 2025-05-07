# Coupon Acceptance Analysis

This project explores patterns in coupon acceptance using visualizations from a dataset that includes demographic, behavioral, and income-related variables.

---

## Findings

- Education Level
  - Highest coupon acceptance observed among individuals with *some college* or *no degree*.
  - Graduate degree holders show the lowest overall response.
  - Balanced behavior found among Bachelor's and Associate's degree holders.

- Age Distribution
  - Coupon acceptance peaks in the 21–26 age group.
  - Non-acceptance is more evenly distributed across all age groups.
  - Younger individuals (especially under 30) are more likely to accept coupons.

- Income Level
  - Strongest coupon acceptance among those earning $50,000–$87,000.
  - Notably high acceptance in the lowest income group (<$12,500).
  - High-income earners ($100,000+) tend to decline coupons more often.

- Gender & Destination
  - Females are more likely to accept coupons than males.
  - Respondents with no urgent destination show the highest acceptance.
  - Acceptance is relatively similar across Home and Work destinations.

---

## Next Steps

- Education
  - Calculate and visualize coupon acceptance rate (%) by education level.
  - Group educational levels into broader categories (e.g., Low, Medium, High).

- Age
  - Bin age into ranges (e.g., <25, 25–40, 40–60, 60+) for clearer analysis.
  - Run a chi-squared test or logistic regression to assess statistical significance.

- Income
  - Normalize bar plots to show percentage acceptance by income bracket.
  - Include a predictive model (e.g., logistic regression) to quantify the effect of income.

- Gender & Destination
  - Investigate interaction effects (e.g., gender * destination).
  - Use grouped or faceted plots to explore overlaps between variables.

- General Enhancements
  - Create a correlation heatmap for one-hot encoded categorical variables.
  - Build a predictive model (logistic regression or decision tree).
  - Develop an interactive dashboard using Streamlit or Plotly Dash.
