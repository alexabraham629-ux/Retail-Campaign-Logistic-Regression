# Retail Campaign Response Model & Inflation Scenario (Excel)

A logistic-regression model built in Excel, with coefficients estimated by maximum likelihood using Solver, that ranks 500 customers by their probability of responding to a campaign and stress-tests campaign economics under an inflation shock.

## Business challenge
Mistargeted campaign spend is costly, especially in a downturn. The business wanted each customer's response probability before allocating budget, and wanted to see how inflation would change response, revenue and cost per acquisition.

## Method
- **Logistic regression** on 10 behavioural and transactional variables (e.g. average order value, website visits, days since last purchase, loyalty membership, email and social engagement).
- **Maximum likelihood estimation in Excel Solver:** coefficients chosen to maximise total log-likelihood (final value −287.60).
- **Campaign KPIs:** expected revenue, campaign cost and cost per acquisition (CPA), targeting customers with p > 0.5.
- **Inflation scenario:** coefficients held fixed while customer inputs are shocked: **−15% order value**, **−10% website visits**, **+20% days since last purchase**.

## Key findings (baseline vs. post-inflation)
| Metric | Baseline | Inflation | Change |
|---|---|---|---|
| Expected revenue | $15,193 | $10,827 | **−28.7%** |
| Customers targeted (p > 0.5) | 212 | 145 | −31.6% |
| CPA | $7.518 | $7.538 | +0.3% |

- **Revenue falls faster than response:** average response probability drops 16.0%, but revenue drops 28.7% because fewer conversions and smaller baskets compound.
- **Cost discipline holds:** the p > 0.5 rule shrinks the target list automatically, so CPA stays flat. The damage is in revenue, not cost.

## Recommendations
1. **Reallocate rather than cut:** put the $335 saved into the highest-probability core responders.
2. **Protect high-coefficient segments:** loyalty members and highly engaged email / social customers.
3. **Counter basket shrinkage:** bundles and minimum-spend incentives to offset the 15% drop in order value.

## Repository structure
```
├── campaign_response_model.xlsx    # Data, Solver MLE setup, KPIs and scenario sheets
├── data/
│   └── retail_campaign_data.csv    # 500 customers, 10 predictors + response
└── reports/
    └── presentation.pptx           # Findings deck
```

## How to use
Open `campaign_response_model.xlsx` in Excel. To re-estimate the coefficients, enable the Solver add-in and re-run it on the log-likelihood cell.

## Tools
Microsoft Excel (Solver) · logistic regression · scenario analysis
