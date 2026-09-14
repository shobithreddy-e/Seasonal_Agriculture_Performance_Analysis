# Seasonal Agriculture Performance Analysis

**VOIS AICTE Batch1 2026-2027 — Major Project**

## Problem Statement

Agricultural activities are influenced by seasonal variations in environmental conditions, farming practices, resource availability and market conditions. As a result, agricultural performance may differ from one season to another. This project analyzes a multi-season farm-level dataset to investigate seasonal differences in agricultural performance by identifying meaningful patterns, trends, relationships and variations within the data.

## Dataset

- 4,000 farm-level records across 28 columns
- Spans 3 seasons (Kharif, Rabi, Zaid), 8 Indian states, 10 districts, 8 crops, and 4 irrigation methods
- Includes environmental readings (rainfall, temperature, humidity, soil moisture/pH, NPK), farm inputs (fertilizer, pesticide, seed quality, water used), and economic outcomes (yield, production, cost, revenue, profit)

## Analytical Questions

1. How does crop yield vary across seasons, and is the difference statistically significant?
2. How does economic performance (cost, revenue, profit) vary across seasons?
3. How does irrigation method efficiency change across seasons?
4. What environmental factors actually relate to yield, and how do they shift across seasons?
5. How does disease/pest risk vary across seasons, and does it affect outcomes?
6. Which states/regions perform best across seasons?

## Methodology

- **Data cleaning:** missing values in Rainfall, Soil Moisture and Yield imputed using contextually relevant medians (season-wise / crop+season-wise); Yield outliers capped using the IQR method
- **Feature engineering:** profit margin %, cost per hectare, loss-making flag
- **Exploratory analysis:** season/crop distribution, yield and economic performance comparisons, irrigation efficiency heatmaps, correlation analysis, disease/pest risk patterns, state-wise performance
- **Statistical testing:** one-way ANOVA (yield across seasons) and Kruskal-Wallis test (profit across seasons)

## Key Findings

1. Yield does **not** differ significantly across seasons (ANOVA p = 0.23), but profit does, dramatically (Kruskal-Wallis p < 0.001).
2. Median profit falls from +₹38.8k (Kharif) to -₹3.2k (Rabi) to -₹62.1k (Zaid); the share of loss-making farms rises from 42% to 64%.
3. Environmental readings (rainfall, temperature, humidity, soil moisture) barely correlate with yield; market price does, negatively (-0.38) — a supply-glut effect.
4. Rainfed irrigation is the most water-efficient method in every season, though this reflects lower water input rather than higher output.
5. Disease/pest risk peaks in Kharif (monsoon) but doesn't suppress Kharif's yield or profit advantage.
6. Telangana, Karnataka and Punjab post the highest median profits; Andhra Pradesh and Madhya Pradesh are the only states with negative median profit overall.

## Recommendations

- Explore staggered selling, storage, or contract farming in Rabi/Zaid to avoid selling into lower-price windows
- Prioritize drip irrigation in Zaid, where water efficiency is lowest across all methods
- Sustain current pest/disease management spend in Kharif rather than cutting back
- Investigate state-level cost/market-access drivers in Andhra Pradesh and Madhya Pradesh
- Use profit — not yield — as the primary KPI for seasonal planning

## Tools & Technologies

- Python — Pandas & NumPy for data cleaning and analysis
- Matplotlib & Seaborn for visualization
- SciPy for statistical testing (ANOVA, Kruskal-Wallis)
- Jupyter Notebook for end-to-end documentation

## Repository Contents

```
├── Seasonal_Agriculture_Performance_Analysis.ipynb   # Full analysis notebook
├── seasonal_agriculture_performance_dataset.xlsx     # Source dataset
├── VOIS_Major_Project_PPT_Submission.pptx            # Project presentation
└── README.md
```
