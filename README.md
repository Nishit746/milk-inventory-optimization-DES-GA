# Simulation-Based Inventory Optimization for Perishable Milk Products

## Publication

This repository contains the implementation accompanying the research paper:

**Simulation Based Approach for Inventory Management of Packaged Milk at an Unorganized Indian Retailer: A Case Study**

Published in the Proceedings of the International Conference on Operations & Supply Chain Management (ICOSCM 2025).

---

## Overview

This project develops a simulation-based framework for inventory management of perishable milk products sold by small unorganized retailers.

The system models real-world inventory operations under stochastic demand and compares:

1. Traditional Fixed-Order Policy
2. Genetic Algorithm Optimized Base-Stock Policy

The objective is to reduce lost sales, manage perishability, and improve retailer profitability.

---

## Problem Statement

Small retailers typically rely on heuristic ordering rules and personal experience to manage inventory.

For perishable products such as milk, this often leads to:

- Demand uncertainty
- Stockouts
- Lost sales
- Product wastage
- Inefficient replenishment decisions

This project evaluates whether modern optimization techniques can improve inventory performance.

---

## Methodology

### 1. Demand Modelling

Demand for each SKU is represented using probability distributions derived from retailer data.

| Product | Distribution |
|----------|-------------|
| Milk A | Triangular (140,144,147) |
| Milk B | Uniform (70,74) |
| Milk C | Uniform (23,25) |

---

### 2. Discrete Event Simulation (DES)

The inventory system is simulated over a 120-day horizon.

Daily events include:

- Order arrival
- Demand generation
- FIFO inventory consumption
- Expiry handling
- Replenishment
- Profit computation

---

### 3. Inventory Policies

#### Existing Policy

Fixed daily order quantity equal to average demand.

#### Proposed Policy

Base-stock inventory policy optimized using a Genetic Algorithm.

---

### 4. Genetic Algorithm Optimization

The Genetic Algorithm determines optimal inventory multipliers by:

- Population initialization
- Tournament selection
- Uniform crossover
- Gaussian mutation
- Profit-based fitness evaluation

---

### 5. Statistical Validation

The results are validated using:

- Jarque-Bera Test
- Breusch-Pagan Test
- Paired t-Test
- Wilcoxon Signed-Rank Test

---

### 6. Sensitivity Analysis

Additional experiments evaluate the impact of increased demand variability on policy performance.

---

## Key Results

### Baseline Scenario

| Metric | Result |
|----------|----------|
| Profit Improvement | +0.33% |
| Lost Sales | Reduced |
| Expiry | Zero |
| Statistical Significance | Yes |

### Sensitivity Analysis Scenario

| Metric | Result |
|----------|----------|
| Profit Improvement | +1.14% |
| Lost Sales | Reduced |
| Robustness | Improved |

---

## Repository Structure

```text
milk-inventory-optimization-DES-GA
│
├── Milk_Inventory_Optimization_DES_GA.ipynb
├── README.md
├── requirements.txt
├── LICENSE
│
├── paper/
│   └── ICOSCM2025_Paper.pdf
│
├── images/
│   ├── policy_comparison.png
│   ├── sensitivity_analysis.png
│   └── results_table.png
│
└── data/
```

## Installation

```bash
pip install -r requirements.txt
```

## Running the Project

1. Open the notebook in Google Colab.
2. Upload the required Excel input file.
3. Run all notebook cells.
4. Review simulation outputs and policy comparisons.

---

## Technologies Used

- Python
- NumPy
- Pandas
- SciPy
- Statsmodels
- Matplotlib
- Google Colab

---

## Future Work

- Multi-echelon inventory optimization
- Reinforcement learning based ordering policies
- Real-time inventory dashboards
- Perishable inventory optimization for fruits and vegetables

---

## Author

Nishit Mehta

Dual Degree (B.Tech + M.Tech)

Indian Institute of Technology Kharagpur

Operations Research | Supply Chain Analytics | Optimization
