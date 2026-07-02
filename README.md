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
- ($\Delta NWC$) = Change in Net Working Capital  

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

- **Enterprise Value:** ~\$281B  
- **Equity Value:** ~\$251B  
- **Implied Share Price:** ~\$35.77  

Under conservative assumptions, the model suggests intrinsic value below the current market price, implying that the market may be pricing in higher long-term growth, lower cost of capital, or additional structural advantages.

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

# Model

<img width="1474" height="305" alt="image" src="https://github.com/user-attachments/assets/d0c33a22-da2b-4aea-a5c6-baf093e90b30" />
<img width="1023" height="419" alt="image" src="https://github.com/user-attachments/assets/63d5cf03-6db6-438c-8633-51973afe8d7a" />
<img width="446" height="361" alt="image" src="https://github.com/user-attachments/assets/fb4cdf1c-e0ff-476c-a1d3-d801eef2491a" />
<img width="877" height="731" alt="image" src="https://github.com/user-attachments/assets/a5dad067-4485-49af-bf99-bbd4308af29d" />
<img width="881" height="218" alt="image" src="https://github.com/user-attachments/assets/517efe48-f712-44e7-abc1-1558b79acc8e" />


---

# Financial Concepts Applied

- Time Value of Money  
- Capital Asset Pricing Model (CAPM)  
- Weighted Average Cost of Capital (WACC)  
- Free Cash Flow to Firm (FCFF)  
- Enterprise to Equity Bridge  
- Sensitivity Analysis  

---

# Disclaimer

This model was built for educational purposes only and does not constitute investment advice.​

​
