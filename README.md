# Inventory Planning Using Normal Distribution
### Estimating Safety Stock and Fill Rate Across Multiple Stores

This project demonstrates how to use the normal distribution and statistical tools from NumPy, SciPy, and Matplotlib to estimate inventory requirements needed to achieve a target fill rate across multiple retail stores.

The central question explored is:

**How much inventory should a retailer keep to guarantee a 95% fill rate across several stores with similar demand patterns?**

---

## Overview

Retail demand can often be modeled using a normal distribution, especially when aggregated over multiple stores. By using expected demand, mean, and variability, we can calculate:

- Probability Density Function (PDF)  
- Cumulative Distribution Function (CDF)  
- Percentile Point Function (PPF), the inverse CDF, used to determine required inventory for target service levels

The notebook provides a step-by-step process using examples with both 2 stores and 12 stores.

---

## What the Notebook Covers

### 1. Define Demand Variables
- Expected demand per store  
- Number of stores  
- Independent standard deviation  
- Number of simulation iterations  

### 2. Compute Inventory Distribution  
Using the following formulas:

Mean = Expected Demand × Number of Stores  
Standard Deviation = sqrt(Number of Stores) × Individual Standard Deviation

### 3. Plot the Probability Density Function  
A PDF curve is generated to visualize the distribution of total demand.

### 4. Compute Fill Rate Using the CDF  
The CDF evaluates the probability that guaranteed supply will meet customer demand.

### 5. Compute Required Inventory Using the PPF  
The PPF determines how much inventory is needed to cover 95 percent of demand.

### 6. Extend the Scenario  
The analysis is repeated for 12 stores to illustrate how total variability increases with the number of independent locations.

---

## Key Results

| Scenario | Stores | Guaranteed Supply | Fill Rate (CDF) | Required Inventory for 95% (PPF) |
|----------|--------|-------------------|------------------|----------------------------------|
| Case 1   | 2      | 2000 units        | Calculated in notebook | Calculated in notebook |
| Case 2   | 12     | 12000 units       | Calculated in notebook | Calculated in notebook |

As the number of stores increases, demand variability increases with the square root of the number of stores. This reduces the fill rate for a fixed amount of inventory and increases the required inventory needed to achieve a 95% service level.

---

## Conclusions

- Total demand across stores follows a normal distribution, making statistical modeling suitable.  
- The CDF provides the fill rate for any chosen level of inventory.  
- The PPF identifies the inventory level needed to reach a 95% service level.  
- Demand variability grows with the square root of the number of stores, not linearly.  
- This method provides a data-driven framework for warehouse inventory planning.

---

## Technologies Used

- Python 3  
- NumPy  
- SciPy (stats)  
- Matplotlib  
- Google Colab or Jupyter Notebook

---

## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/<repo-name>.git
