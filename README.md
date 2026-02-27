# Customer Targeting Optimisation

Built a logistic regression model to identify profitable customers for a targeted marketing campaign, optimising ROI by mailing only to customers whose predicted response probability exceeds the break-even threshold.

---

## Problem Statement

A subscription-based business wants to acquire new customers through direct mail marketing. Blanket marketing (mailing everyone) is expensive and often unprofitable. The goal is to build a predictive model that identifies which customers are likely to subscribe, so marketing spend is focused only on profitable segments.

**Key question:** Which customers should receive a marketing offer to maximise return on investment?

---

## Approach

### 1. Break-Even Analysis
- Calculated the **break-even response rate** — the minimum subscription probability needed for a mailing to be profitable
- Cost per offer: £1.50 | Profit per subscriber: £6.99
- **Break-even rate: 21.46%** — only mail customers with predicted probability > 21.46%

### 2. Blanket Marketing Baseline
- Evaluated ROI of mailing to all 5,000 customers
- Result: **-21.9% ROI** — blanket marketing loses money
- Total cost (£7,500) exceeds revenue from subscribers (£5,858)

### 3. Predictive Targeting Model
- Built a **logistic regression model** to predict individual subscription probability
- Features: customer demographics, purchase history, engagement metrics
- Applied the break-even threshold as a decision rule:
  - **P(subscribe) > 21.46%** → Send offer
  - **P(subscribe) ≤ 21.46%** → Don't send

### 4. Results
- Targeted marketing significantly outperformed blanket approach
- Reduced wasted spend by mailing only to high-probability segments
- Demonstrated the business value of predictive analytics in marketing decisions

---

## Key Concepts Demonstrated

| Concept | Application |
|---------|-------------|
| Logistic Regression | Predicting binary subscription outcome |
| Break-even Analysis | Financial threshold for marketing decisions |
| ROI Calculation | Comparing blanket vs targeted campaign profitability |
| Lift Analysis | Measuring how much better the model performs vs random |
| Confusion Matrix | Evaluating prediction accuracy (true/false positives) |

---

## Tech Stack

- **Language:** R
- **Libraries:** dplyr, broom, ggplot2
- **Techniques:** Logistic Regression, Break-even Analysis, ROI Optimisation
- **Environment:** RStudio / Quarto

---

## Project Structure

```
customer-targeting-optimisation/
├── README.md
├── analysis.qmd                # Full analysis in Quarto format
├── analysis.R                  # Standalone R script
├── .gitignore
└── images/
    ├── roi_comparison.png
    └── lift_chart.png
```

---

## Business Impact

This project demonstrates a core analytics consulting skill: **translating a predictive model into a financial decision framework**. Rather than just building a model and reporting accuracy, the analysis shows exactly how much money the business saves by switching from blanket to targeted marketing — the kind of insight that drives real business decisions.

---

## Author

**Morvica Purohit** — MSc Business Analytics, UCL  
[LinkedIn](https://www.linkedin.com/in/morvica-purohit/L) · [Email](mailto:morvicapurohit2000@gmail.com)
