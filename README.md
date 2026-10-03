# Inventory Management Optimization Using Time Series Forecasting, Stochastic Modeling, and Operations Research

## 📌 Project Overview

Inventory management is a critical challenge for businesses because maintaining too much inventory increases holding costs, while insufficient inventory can lead to stockouts and lost sales.

This project develops an **inventory management framework** that combines:

* 📈 **Time Series Forecasting** for predicting future demand
* 🎲 **Stochastic Modeling** for incorporating demand uncertainty
* 📊 **Operations Research** for optimizing inventory decisions

The objective is to move beyond simply forecasting demand and use the forecasts to make **data-driven inventory decisions** that balance stock availability and inventory-related costs.

---

## 🎯 Objectives

The main objectives of this project are:

1. Forecast future product demand using historical sales data.
2. Analyze patterns and trends in demand over time.
3. Incorporate uncertainty in future demand using stochastic modeling.
4. Determine suitable inventory policies using Operations Research techniques.
5. Reduce the risk of stockouts while avoiding excessive inventory.
6. Demonstrate how statistical forecasting and optimization can work together in supply chain decision-making.

---

## 🔄 Project Workflow

The project follows the following pipeline:

```text
Historical Sales Data
        ↓
Data Preprocessing
        ↓
Exploratory Data Analysis
        ↓
Time Series Analysis
        ↓
Demand Forecasting
        ↓
Demand Uncertainty Modeling
        ↓
Inventory Optimization
        ↓
Optimal Inventory Policy
        ↓
Evaluation of Cost & Stockout Risk
```

---

## 📊 Methodology

### 1. Data Preparation

Historical sales data is first processed to ensure that it can be used for time series analysis.

The preprocessing stage includes:

* Handling missing values
* Checking data consistency
* Aggregating sales data over appropriate time intervals
* Identifying trends and seasonal patterns
* Visualizing historical demand

---

### 2. Time Series Forecasting

Historical demand is analyzed to identify underlying patterns and forecast future demand.

Depending on the characteristics of the data, time series forecasting techniques can be used to estimate:

$$
\hat{D}_{t+1}, \hat{D}_{t+2}, \ldots, \hat{D}_{t+h}
$$

where \(D_t\) represents demand at time \(t\).

Forecast accuracy is evaluated using appropriate forecasting metrics such as:

* MAE — Mean Absolute Error
* RMSE — Root Mean Squared Error
* MAPE — Mean Absolute Percentage Error

The forecast provides the expected future demand required for subsequent inventory optimization.

---

### 3. Stochastic Demand Modeling

Forecasts alone do not capture the uncertainty associated with future demand.

Therefore, the project incorporates stochastic modeling to represent demand as a random variable rather than a fixed quantity.

For example:

$$
D_t = \mu_t + \epsilon_t
$$

where:

* \(D_t\) = actual demand
* \(\mu_t\) = expected demand
* \(\epsilon_t\) = random demand variation

This allows the inventory system to account for situations where actual demand differs from the forecast.

---

### 4. Inventory Optimization

Operations Research techniques are then used to determine an appropriate inventory policy.

The optimization framework considers factors such as:

* Expected demand
* Demand variability
* Inventory holding cost
* Stockout/shortage cost
* Replenishment quantity
* Reorder point
* Lead time

A simplified inventory cost function can be represented as:

$$
\text{Total Cost}
=
\text{Holding Cost}
+
\text{Ordering Cost}
+
\text{Shortage Cost}
$$

The objective is to find an inventory policy that minimizes the expected total cost while maintaining an acceptable level of product availability.

---

## 🧮 Key Inventory Concepts

### Reorder Point

The reorder point determines when a new order should be placed.

A basic formulation is:

$$
ROP = \text{Expected Demand During Lead Time} + \text{Safety Stock}
$$

### Safety Stock

Safety stock provides protection against unexpected increases in demand or delays in replenishment.

A simplified formulation is:

$$
SS = z\sigma_L
$$

where:

* \(z\) = service-level factor
* \(\sigma_L\) = standard deviation of demand during lead time

---

## 📈 Evaluation

The framework can be evaluated using both forecasting and inventory-management measures.

### Forecasting Metrics

| Metric | Purpose                                     |
| ------ | ------------------------------------------- |
| MAE    | Measures average absolute forecasting error |
| RMSE   | Penalizes larger forecasting errors         |
| MAPE   | Measures error relative to actual demand    |

### Inventory Metrics

| Metric               | Purpose                                     |
| -------------------- | ------------------------------------------- |
| Total Inventory Cost | Measures overall inventory-related cost     |
| Holding Cost         | Cost of maintaining inventory               |
| Shortage Cost        | Cost associated with insufficient inventory |
| Stockout Rate        | Frequency of inventory shortages            |
| Service Level        | Probability of meeting customer demand      |

---

## 💡 Business Problem Addressed

Traditional inventory systems may rely on fixed reorder rules or historical averages. Such approaches may not adequately account for changing demand and uncertainty.

This project attempts to address three major inventory problems:

### 📦 Excess Inventory

Holding more inventory than necessary increases storage and capital costs.

### ⚠️ Stockouts

Insufficient inventory can result in unmet customer demand and potential revenue loss.

### 💰 Inventory Costs

Businesses need to balance holding, ordering, and shortage costs when deciding how much inventory to maintain.

The proposed framework integrates forecasting and optimization to provide a more systematic approach to this trade-off.

---

## 🛠️ Technologies & Tools

* **Python**
* **Pandas** — Data manipulation
* **NumPy** — Numerical computation
* **Matplotlib / Seaborn** — Data visualization
* **Statsmodels** — Time series modeling
* **SciPy / Optimization libraries** — Optimization
* **Jupyter Notebook** — Development and analysis

---

## 📂 Project Structure

```text
Inventory-Management-Optimization/
│
├── data/
│   └── sales_data.csv
│
├── notebooks/
│   ├── 01_Data_Preprocessing.ipynb
│   ├── 02_Exploratory_Data_Analysis.ipynb
│   ├── 03_Time_Series_Forecasting.ipynb
│   ├── 04_Stochastic_Modeling.ipynb
│   └── 05_Inventory_Optimization.ipynb
│
├── src/
│   ├── forecasting.py
│   ├── stochastic_model.py
│   └── inventory_optimization.py
│
├── results/
│   ├── forecasts/
│   └── visualizations/
│
├── requirements.txt
└── README.md
```

---

## 🚀 Key Takeaways

This project demonstrates how different areas of Statistics and Computing can be integrated to solve a practical business problem.

The key idea is:

> **Forecast demand → Model uncertainty → Optimize inventory decisions**

Rather than treating forecasting and optimization as separate tasks, the project connects them into a single decision-making framework.

It demonstrates the practical application of:

* Time Series Analysis
* Stochastic Processes
* Statistical Modeling
* Operations Research
* Optimization
* Supply Chain Analytics

---

## 📚 Academic Context

This project was developed as part of my **M.Sc. Statistics and Computing** curriculum at **Banaras Hindu University (BHU)**.

The project was particularly motivated by concepts studied in:

* **Stochastic Processes**
* **Operations Research**
* **Time Series Analysis**
* **Statistical Modeling**

It provided an opportunity to apply these theoretical concepts to a practical supply-chain and inventory-management problem.

---

## 🔮 Future Improvements

Possible extensions include:

* Incorporating multiple products simultaneously
* Modeling variable lead times
* Comparing multiple forecasting models
* Developing multi-period inventory optimization
* Incorporating supplier constraints
* Adding dynamic pricing or demand-response effects
* Developing a simulation-based inventory policy
* Building an interactive dashboard for inventory decisions

---

## 👤 Author

**Prantik Dutta**
M.Sc. Statistics and Computing
Banaras Hindu University (BHU)

---

## 🏷️ Topics

`Statistics` `Time Series` `Stochastic Processes` `Operations Research` `Inventory Management` `Supply Chain Analytics` `Forecasting` `Optimization` `Python` `Data Science` `Machine Learning`
