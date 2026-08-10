# Retail-Campaign-Logistic-Regression
Predictive marketing analytics model using Logistic Regression and MLE to optimize campaign targeting under inflationary pressure.
# Predictive Retail Campaign Analytics & Inflation Modeling

## 📌 Business Challenge
In the retail sector, mistargeted marketing spend is highly costly, especially during economic downturns[cite: 18]. The business needed a data-driven method to predict individual customer response probabilities for a base of 500 customers before allocating campaign budgets[cite: 18]. Furthermore, leadership required visibility into how a macroeconomic shock (inflationary pressure) would alter customer behavior and campaign ROI[cite: 18].

## 🎯 Project Objective
Build a predictive marketing analytics model to rank customer response probability, establish baseline campaign KPIs (Revenue, CPA, Cost), and simulate an inflationary scenario to provide strategic, budget-defensive recommendations[cite: 18].

## ⚙️ Analytical Methodology
* **Logistic Regression:** Modeled the probability of response based on 10 behavioral and transactional variables (e.g., Average Order Value, Website Visits, Days Since Last Purchase)[cite: 18].
* **Maximum Likelihood Estimation (MLE):** Utilized Excel Solver to estimate model coefficients by maximizing total log-likelihood (-287.60), ensuring the model learns from historical evidence rather than assumptions[cite: 18].
* **Scenario Analysis:** Simulated an inflation shock by holding coefficients fixed and shocking customer inputs: **-15% Average Order Value**, **-10% Website Visits**, and **+20% Days Since Last Purchase**[cite: 18].

## 📊 Key Findings & Financial Impact
Comparing the Baseline model to the Post-Inflation scenario revealed critical business dynamics:
* **Compounding Revenue Erosion:** Total Expected Revenue dropped by **28.7%** (from $15,193 to $10,827)—falling much faster than the average response probability (-16.0%) due to the compounding effect of fewer conversions and lower basket sizes[cite: 18].
* **Audience Contraction:** The addressable audience (p > 0.5) shrank by 31.6%, reducing the targeted customer pool from 212 to 145[cite: 18].
* **Cost Efficiency Resilience:** Cost Per Acquisition (CPA) remained essentially flat (+0.3%, moving from $7.518 to $7.538)[cite: 18]. Because the targeting threshold automatically shrinks the pool, marketing costs fell in step with the audience, proving that inflation's damage is concentrated in revenue loss, not cost discipline[cite: 18].

## 💡 Strategic Recommendations
1. **Reallocate, Don’t Just Cut:** The $335 saved from the shrinking addressable audience should be reinvested into the highest-probability "core responders" rather than spread thinly across fence-sitters[cite: 18].
2. **Protect High-Coefficient Segments:** Loyalty members and highly engaged email/social customers carry the strongest positive influence on response probability; prioritize retention offers here[cite: 18].
3. **Counter Basket Compression:** Implement bundle offers and minimum-spend incentives to directly offset the 15% drop in Average Order Value[cite: 18].

## 📁 Repository Contents
* `RETAIL_ CAMPAIGN _SOLVED_2.xlsx`: The core analytical model featuring the dataset, MLE Solver setup, and scenario simulations.
* `retail_campaign_data_2.csv`: Raw transactional and behavioral dataset of 500 customers.
* `Retail_Campaign_Analytics_Presentation.pdf`: Executive-level slide deck translating statistical outputs into business strategy.
