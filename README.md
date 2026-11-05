# Tesla (TSLA) Discounted Cash Flow (DCF) Valuation Model

[![Excel](https://img.shields.io/badge/Model-Microsoft_Excel-green.svg)](https://microsoft.com/excel)
[![Financial Modeling](https://img.shields.io/badge/Domain-Corporate_Finance_%26_Valuation-blue.svg)](#)

## Executive Summary

This repository contains a dynamic, multi-scenario **Discounted Cash Flow (DCF) Valuation Model** for **Tesla, Inc. (NASDAQ: TSLA)**. The model projects 5-year Unlevered Free Cash Flows (UFCF) based on historical financial performance, automotive unit delivery estimates, energy segment expansion, and margin trajectories. 

The primary objective of this project is to estimate the intrinsic value per share of TSLA using both the **Terminal Growth Rate (Gordon Growth)** approach and the **Exit Multiple (EV/EBITDA)** approach, factoring in multi-scenario sensitivity analyses.

---

## Key Valuation Highlights & Outputs

* **Valuation Methodology:** 2-Stage Unlevered DCF Model (5-Year Forecast Period + Terminal Value)
* **Base Case Implied Share Price:** `[e.g., $245.00]`
* **Current Trading Price (as of Model Date):** `[e.g., $210.00]`
* **Implied Upside / (Downside):** `[e.g., +16.7%]`
* **Weighted Average Cost of Capital (WACC):** `[e.g., 9.5%]`
* **Terminal Growth Rate:** `[e.g., 3.0%]`
* **Exit EV/EBITDA Multiple:** `[e.g., 18.0x]`

---

## Model Architecture & Methodology

The model is built with strict adherence to financial modeling best practices, separating inputs, historical data, core schedules, and valuation outputs.

### 1. Revenue Drivers & Operating Assumptions
* **Automotive Revenue:** Modeled bottom-up using projected vehicle deliveries across legacy models (Model 3/Y), scaling platforms (Cybertruck, Next-Gen Vehicle), and average selling prices (ASPs).
* **Energy Storage & Services:** Projected separately based on megawatt-hour (MWh) deployment growth rates and long-term margin stabilization.
* **Cost Structure:** COGS and Operating Expenses (R&D, SG&A) modeled as a percentage of revenue, accounting for scale efficiencies over the forecast horizon.

### 2. Capital Structure & Cost of Capital (WACC)
* **Cost of Equity ($K_e$):** Calculated via the Capital Asset Pricing Model (CAPM) using current Risk-Free Rate, Beta ($\beta$), and Equity Risk Premium (ERP).
* **Cost of Debt ($K_d$):** Derived from effective interest rates and tax-adjusted ($K_d \times (1 - t)$).
* **Capital Weights:** Dynamic weighting based on current market enterprise values.

### 3. Cash Flow Projections (UFCF)
* **NOPAT:** Calculated as $\text{EBIT} \times (1 - \text{Effective Tax Rate})$.
* **Reinvestments:** Non-cash Depreciation & Amortization added back, adjusted for Capital Expenditures (CapEx) and changes in Net Working Capital (NWC).
$$\text{UFCF} = \text{NOPAT} + \text{D\&A} - \text{CapEx} - \Delta\text{NWC}$$

### 4. Valuation & Terminal Value
* **Gordon Growth Method:**
$$\text{Terminal Value} = \frac{\text{UFCF}_n \times (1 + g)}{\text{WACC} - g}$$
* **Exit Multiple Method:**
$$\text{Terminal Value} = \text{EBITDA}_n \times \text{Target EV/EBITDA}$$

---

## Scenario & Sensitivity Analysis

To account for market volatility and variance in EV adoption, the model incorporates three operational scenarios:

| Metric / Driver | Bear Case | Base Case | Bull Case |
| :--- | :---: | :---: | :---: |
| **5-Yr Revenue CAGR** | `10.0%` | `18.0%` | `25.0%` |
| **Terminal Operating Margin** | `10.0%` | `14.5%` | `18.0%` |
| **WACC** | `10.5%` | `9.5%` | `8.5%` |
| **Terminal Growth Rate** | `2.0%` | `3.0%` |
