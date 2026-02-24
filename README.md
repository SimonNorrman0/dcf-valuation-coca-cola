# Coca-Cola DCF Valuation Model

## Overview

This repository contains a full **Discounted Cash Flow (DCF)** valuation model of **The Coca-Cola Company (KO)** built from scratch in Excel.

The model includes:

- Historical financial analysis  
- 5-year operating forecast (2026–2030)  
- Free Cash Flow to Firm (FCFF) calculation  
- WACC estimation using CAPM  
- Enterprise to Equity bridge  
- 2D sensitivity analysis (WACC vs Terminal Growth)  

All financial figures are presented in **USD millions** unless otherwise stated.

---

# Valuation Framework

The valuation is based on projecting operating cash flows and discounting them to present value using the firm’s weighted average cost of capital.

---

## 1) Free Cash Flow to Firm (FCFF)

Free Cash Flow to Firm is calculated as:

```math
FCF = NOPAT + D\&A - CapEx - \Delta NWC
```

Where operating profit after tax is defined as:

```math
NOPAT = EBIT \times (1 - T)
```

Definitions:

- \(EBIT\) = Earnings Before Interest and Taxes  
- \(T\) = Effective tax rate  
- \(D\&A\) = Depreciation & Amortization  
- \(CapEx\) = Capital Expenditures  
- \(\Delta NWC\) = Change in Net Working Capital  

---

## 2) Terminal Value (Gordon Growth Model)

The terminal value at the end of the forecast period (2030) is calculated using the Gordon Growth Model:

```math
TV = \frac{FCF_{2030} \cdot (1 + g)}{WACC - g}
```

Where:

- \(g\) = Terminal growth rate  
- \(WACC\) = Weighted Average Cost of Capital  

The terminal value is then discounted back to present value:

```math
PV(TV) = \frac{TV}{(1 + WACC)^5}
```

---

## 3) Weighted Average Cost of Capital (WACC)

WACC is calculated as:

```math
WACC = \frac{E}{V} R_e + \frac{D}{V} R_d (1 - T)
```

### Cost of Equity (CAPM)

```math
R_e = R_f + \beta \cdot ERP
```

Where:

- $R_f$ = Risk-free rate  
- $\beta$ = Levered beta  
- $ERP$ = Equity risk premium  
- $R_d$ = Pre-tax cost of debt  
- $T$ = Corporate tax rate  
- $\frac{E}{V}, \frac{D}{V}$ = Capital structure weights  

---

## 4) Enterprise Value

Enterprise value is calculated as:

```math
EV = \sum_{t=1}^{5} \frac{FCF_t}{(1 + WACC)^t} + \frac{TV}{(1 + WACC)^5}
```

---

## 5) Equity Value and Implied Share Price

```math
Equity\ Value = EV - Net\ Debt
```

```math
Implied\ Share\ Price = \frac{Equity\ Value}{Shares\ Outstanding}
```

---

# Key Assumptions (Base Case)

<div style="margin-bottom: 20px;">
 <img width="294" height="146" alt="image" src="https://github.com/user-attachments/assets/71f9f277-ab68-4f54-ba51-b93c9515a0bd" />
</div>

<div style="margin-bottom: 20px;">
  <img width="294" height="145" alt="image" src="https://github.com/user-attachments/assets/ccc662ef-f2af-456e-9c8f-6093a920e5d5" />
</div>


---

# Valuation Results (Base Case)

- **Enterprise Value:** ~\$236B  
- **Equity Value:** ~\$206B  
- **Implied Share Price:** ~\$29  

Under conservative assumptions, the model suggests intrinsic value below the current market price, implying that the market may be pricing in higher long-term growth, lower cost of capital, or additional structural advantages.


---

## Conclusion

Using the base-case assumptions (**4% revenue growth**, **28% EBIT margin**, **23% tax rate**, **WACC = 6.85%**, **terminal growth (g) = 2.5%**), the DCF implies an intrinsic value of approximately **$29.29 per share**.

This value should be interpreted relative to the current market price:
- If the market price is **above** $29.29, the market is effectively pricing in **higher growth**, **higher margins**, and/or a **lower cost of capital** than the base case.
- If the market price is **below** $29.29, the market is pricing in **lower growth**, **lower margins**, and/or a **higher cost of capital** than the base case.

### Sensitivity / Key Drivers
The valuation is highly sensitive to **WACC** and **terminal growth**, as shown in the sensitivity table. Small changes in either assumption lead to large changes in implied share price, which is typical for DCF models where a significant portion of value comes from the terminal value.

### Takeaway
Overall, the DCF suggests that Coca-Cola’s implied valuation is driven primarily by long-term assumptions about:
- sustainable growth (**g**),
- required return (**WACC**),
- and operating profitability (EBIT margin).

Therefore, the model’s output should be viewed as a range rather than a single “correct” price, with the sensitivity analysis providing the most realistic view of valuation outcomes.

---



# Sensitivity Analysis

A 2-dimensional sensitivity table is included to evaluate valuation across different combinations of:

- \(WACC\)
- Terminal Growth Rate \(g\)

Because terminal value typically accounts for the majority of total firm value, small variations in these assumptions materially affect intrinsic valuation.

Mathematically, sensitivity is driven by:

```math
TV = \frac{FCF_{2030}(1+g)}{WACC - g}
```

As:

- $WACC \downarrow$ → valuation increases  
- $g \uparrow$ → valuation increases  

---

# Model Structure

The Excel model is organized as:


- Cover
- Assumptions
- Historical Financials
- Forecast
- Free Cash Flow
- WACC
- DCF & Sensitivity


The structure ensures:

- Clear separation between operating forecast and valuation mechanics  
- No hardcoded valuation outputs  
- Transparent assumption linking  
- Fully dynamic sensitivity analysis  

---

# Financial Concepts Applied

- Time Value of Money  
- Capital Asset Pricing Model (CAPM)  
- Weighted Average Cost of Capital (WACC)  
- Free Cash Flow to Firm (FCFF)  
- Enterprise to Equity Bridge  
- Sensitivity Analysis  

---

# What This Project Demonstrates

- Ability to build a complete DCF model from scratch  
- Understanding of valuation mechanics  
- Proper structuring of financial assumptions  
- Awareness of sensitivity and model risk  
- Analytical reasoning behind intrinsic value estimation  

---

# Potential Extensions

Future enhancements could include:

- Multi-stage growth modeling  
- Scenario analysis (Bear / Base / Bull)  
- Comparable company valuation  
- Football-field valuation analysis  
- Market-implied growth reverse engineering  

---

# Disclaimer

This model was built for educational purposes only and does not constitute investment advice.​

​
