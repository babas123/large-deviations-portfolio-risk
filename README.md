# Rare Chance-Constrained Portfolio Optimization using Large Deviations

This repository contains the implementation and empirical analysis of a
chance-constrained portfolio optimization framework for extreme downside risk,
inspired by Tong et al. (2022).

The project was developed as part of the course **IFT-6512 – Stochastic Programming**
(Master's in Mathematical & Computational Finance, Université de Montréal).

##  Objective

The goal is to analyze and control **systemic tail risk** in a portfolio of
AI-related stocks by combining:
- Large deviations theory
- Chance-constrained optimization
- Monte Carlo validation
- Dominating point analysis

##  Methodology

- Asset returns are modeled using a multivariate Gaussian distribution
  with empirical mean and Ledoit–Wolf shrinkage covariance.
- Rare loss probabilities are estimated using:
  - First-order large deviations approximation (P1)
  - Sample Average Approximation (SAA / Monte Carlo)
- Portfolio strategies compared:
  - Equal-weighted
  - Minimum variance
  - Maximum return
  - Optimal VaR under chance constraints (OptVaR)
- Tail risk metrics:
  - Value-at-Risk (VaR)
  - Conditional Value-at-Risk (CVaR)
- Geometric interpretation via dominating points.

##  Repository structure

- `report/` – Final PDF report and figures  
- `code/` – Julia implementations (Monte Carlo, LDT, optimization)  
- `data/` – Input financial data  
- `results/` – Tables and figures  

##  Technologies

- Julia
- JuMP
- Ipopt
- Distributions.jl
- LinearAlgebra, Statistics

## 📄 Report

The full report is available here:
👉 [IFT_6512_Programmation_stochastique_Projet_final_v2.pdf](https://github.com/user-attachments/files/24352138/IFT_6512_Programmation_stochastique_Projet_final_v2.pdf)

## 📌 References

Tong, X., Blanchet, J., & Glynn, P. (2022).  
*Optimizing rare-event probabilities under chance constraints.*
