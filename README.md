# Dynamic EV Charging Optimization with ML-Driven Pricing

This project combines machine learning and economic modeling to forecast electric vehicle charging demand and implement an intelligent pricing system that adapts in real-time. Developed by the Society of Business (SocBiz) - IIT Rookee Club, it tackles the challenge of optimizing EV charging infrastructure through data-driven decision making.

## Overview

The solution processes real-world charging transaction data, builds predictive models for demand forecasting, and deploys an intelligent pricing agent that dynamically adjusts rates based on network load. The goal: maximize infrastructure utilization, reduce peak congestion, and increase revenue through strategic tariff management.

---

## Results & Metrics

| Metric | Value | Notes |
| :--- | :--- | :--- |
| **Prediction Model Accuracy** | 74% ($R^2$) | Trained on urban public grid data |
| **Forecasting Error Rate** | ±6.3% (MAE: 0.0627) | Expected margin for demand predictions |
| **Wait Time Improvement** | 88.4% reduction | Through 4% load flattening during peaks |
| **Midday Utilization Lift** | +5% | Off-peak demand incentivized |
| **Revenue Impact** | +8.30% | Workplace charging scenarios |
| **Price Responsiveness** | -3.02% load shift | Elasticity coefficient: $\epsilon = -0.4$ |
| **System Efficiency Rating** | 7.5 / 10.0 | Workplace user behavior metric |

---

## How It Works: Four-Step Approach

**1. Data Transformation**
Raw transaction logs in JSON format are converted into time-series dataframes. Wide occupancy matrices representing multiple charging stations are pivoted into structured, analyzable rows using pandas reshaping utilities.

**2. Pattern Recognition & Analysis**
The data reveals distinct charging behaviors: commercial fleets charging heavily between midnight and 7 AM at public stations, while office locations experience peak usage during morning work hours (9-5). Statistical variance analysis shows that time-of-day is the dominant factor driving grid stress, not day-of-week variations.

**3. Predictive Modeling**
A Random Forest model learns station-specific patterns, enabling accurate demand forecasting across different locations. The model achieves around 6% prediction error, providing reliable input for the pricing engine.

**4. Autonomous Pricing Engine**
A rule-based agent automatically adjusts tariffs:
- Premium rates (₹19.50/kWh, +30%) activate when load exceeds 30%
- Discounted rates (₹11.25/kWh, -25%) apply when load drops below 23%
- The system continuously monitors performance and recalibrates thresholds to maintain operational targets

---

## Key Findings

**Daily Rhythm Dynamics:** Unlike traditional power grids, urban EV charging shows inverted patterns—nighttime peaks at public locations versus daytime peaks at workplaces. This asymmetry creates distinct optimization opportunities.

**Congestion Relief Through Peak Shaving:** Simple 4% load reduction during congestion periods triggers exponential improvements in wait times, demonstrating the non-linear benefits of demand management.

**Workplace Pricing Premium:** Employees charging at office locations show lower price sensitivity (they're captive to their work schedule), making workplace charging a high-margin, stable revenue stream compared to public infrastructure.

---

## Technical Stack

- **Core Language:** Python
- **Data Processing:** pandas, numpy, json
- **ML Framework:** scikit-learn (Random Forest Regressor)
- **Visualization:** matplotlib

## What's Included

- **`Project.ipynb`:** Complete, annotated Jupyter notebook with all analysis, models, and visualizations
- **`Datasets/`:** Source data files including transaction logs, occupancy records, and time-series information
- **`Submission_Outputs/`:** Processed results including simulation data and performance summaries