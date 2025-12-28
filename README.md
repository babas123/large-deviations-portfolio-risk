# Optimization under Rare Chance Constraints  
## Systemic Tail Risk Analysis of AI Equity Portfolios

This repository contains an academic project developed in the context of the course  
**IFT-6512 – Programmation stochastique** (Université de Montréal).

The objective of this work is to analyze **systemic tail risk** in portfolios composed of
major Artificial Intelligence (AI) equities, using an optimization framework under **rare
chance constraints**, inspired by the methodology proposed in **Tong et al. (2022)**.



##  Project Overview

Classical portfolio optimization techniques (mean–variance, maximum return, diversification)
are known to perform poorly in extreme market conditions.  
This project investigates tail risk behavior by:

- Formulating portfolio optimization problems under **rare-event probability constraints**
- Approximating extreme loss probabilities using **large deviations theory**
- Identifying **dominant points**, i.e. the most likely market shocks generating extreme losses
- Comparing classical portfolios to a **VaR-oriented optimal allocation**

The analysis focuses deliberately on a **sectorially homogeneous universe (AI equities)** in
order to isolate and study **systemic risk mechanisms**.


##  Methodology

### Modeling assumptions
- Weekly log-returns modeled as a **multivariate Gaussian distribution**
- Parameters estimated empirically:
  - Mean vector μ 
  - Covariance matrix Σ, estimated using **Ledoit–Wolf shrinkage**
- Portfolio is **long-only** and fully invested

### Risk measures
- **Value-at-Risk (VaR)**
- **Conditional Value-at-Risk (CVaR)**
- Rare-event probability approximations using **first-order large deviations (P1)**

### Optimization problem
The core problem maximizes the admissible extreme loss level z* subject to a
rare chance constraint:

P(F(u, ξ) ≥ z) ≤ α
where α ≪ 1 (e.g. 1%, 10−4).

##  Main Results

- The **OptVaR portfolio** consistently achieves the highest admissible extreme loss threshold
  z*, outperforming classical strategies in tail risk regimes.
- Monte Carlo estimates confirm that the large deviations approximation is **conservative**
  and reliable.
- Dominant point analysis reveals that **extreme losses are driven by coherent,
  joint shocks** across AI equities, confirming the **systemic nature of tail risk**.
- Diversification within a single highly correlated sector is shown to be **insufficient**
  to mitigate extreme risk.


  
The full report is available here:
👉 [IFT_6512_Programmation_stochastique_Projet_final_v2.pdf](https://github.com/user-attachments/files/24352138/IFT_6512_Programmation_stochastique_Projet_final_v2.pdf)

## 📌 References

Tong, X., Blanchet, J., & Glynn, P. (2022).  
*Optimizing rare-event probabilities under chance constraints.*
