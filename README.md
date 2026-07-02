# Multi-Currency FX Risk Management Analysis

This project presents a complete financial risk management analysis for a multi-currency investment exposure. It combines two related studies:

1. Forward contract analysis for hedging FX risk
2. Options pricing analysis using the Garman-Kohlhagen model

The work is designed to support a presentation and discussion on how firms can manage foreign exchange exposure for international investments.

---

## 1. Project Objective

The objective of this assignment is to evaluate alternative hedging strategies for a USD 1 billion investment spread across four Asian markets:

- India: USD 250 million
- China: USD 250 million
- South Korea: USD 250 million
- Japan: USD 250 million

The study compares:

- No hedge
- Forward contract hedge
- Put option hedge

The goal is to assess which strategy offers the best balance between risk protection and cost.

---

## 2. Forward Contract Analysis

### Purpose
The forward contract analysis evaluates whether locking in exchange rates through forward contracts can reduce FX risk for the portfolio.

### Methodology
- Load FX spot and forward data from the case study workbook
- Use the latest available FX quotes for each currency pair
- Estimate implied foreign interest rates using Interest Rate Parity (IRP)
- Compare portfolio outcomes under different FX scenarios

### Key Inputs
- Spot rate
- 1-year forward rate
- Investment amount in USD
- Expected asset return assumption

### Key Findings
- Forward contracts provide certainty by locking in the future exchange rate
- They eliminate FX volatility risk, but also remove upside participation if the currency moves favorably
- The hedge is effective in adverse scenarios because the gain on the forward contract offsets losses from currency depreciation

### Presentation Takeaway
Forward contracts are useful when the firm wants certainty and wants to protect the portfolio from unfavorable FX moves.

---

## 3. Options Pricing Analysis

### Purpose
The options pricing analysis evaluates whether purchasing currency put options provides a more flexible form of protection.

### Model Used
The Garman-Kohlhagen model was used to price European currency put options.

### Methodology
- Load FX data and estimate interest rates using IRP
- Price put options for each currency pair
- Compare the cost of protection with the potential loss under adverse FX movements
- Analyze the sensitivity of option prices using Greeks such as Delta, Gamma, Vega, and Theta

### Key Findings
- Put options provide downside protection while still allowing upside participation if the currency moves favorably
- The cost of the hedge is relatively small compared with the protection provided
- The strategy is especially attractive in situations where the firm wants insurance against large FX losses without fully giving up upside potential

### Presentation Takeaway
Put options are a flexible and efficient hedging tool, especially when the company wants protection but still wants to benefit from favorable currency movements.

---

## 4. Comparative Insight

### Strategy A: No Hedge
- Maximum upside potential
- Very high risk of large losses under adverse FX movements

### Strategy B: Forward Contracts
- Gives certainty and protection
- Removes upside potential
- Best when predictability matters more than flexibility

### Strategy C: Put Options
- Offers protection against downside risk
- Preserves upside potential
- Best when the firm wants a balanced, insurance-like hedge

### Overall Recommendation
For this case study, put options appear to be the most attractive hedging strategy because they provide strong protection with flexibility and a relatively modest premium cost.

---

## 5. Key Results Summary

### Forward Contract Analysis
- The latest forward analysis produced the following implied foreign rates from the workbook data:
  - USDINR: 1.0063%
  - USDCNH: 6.8365%
  - USDJPY: 7.1743%
  - USDKRW: 4.8210%
- The forward hedge locks in a fixed USD outcome and removes FX volatility for the covered exposure.

### Options Pricing Analysis
- The verified put-option hedge costs from the current analysis are:
  - USDINR: $49,395.82
  - USDCNH: $31,706.06
  - USDJPY: $78,650.84
  - USDKRW: $89,472.57
  - Total: $249,225.29
- This equals about 0.02% of the $1 billion total investment, making the premium cost modest relative to the portfolio size.
- The strategy protects the portfolio from adverse FX moves while preserving upside participation when the currency moves favorably.

---

## 6. Files in the Project

- ForwardContractAnalysis/forward_contract_analysis.py
- OptionsPricing/analyze_options.py
- OptionsPricing/garman_kohlhagen.py
- ForwardContractAnalysis/forward_contract_analysis_results.xlsx
- OptionsPricing/options_pricing_results.xlsx
- Casestudy_Data.xlsx

---

## 7. How to Run the Analysis

### Prerequisites
```bash
pip install -r requirements.txt
```

### Forward Contract Analysis
```bash
python ForwardContractAnalysis/forward_contract_analysis.py
```

### Options Pricing Analysis
```bash
python OptionsPricing/analyze_options.py
```

### Run Both Analyses Together
```bash
python run_analysis.py
```

### Run the Regression Test
```bash
python -m pytest -q
```

---

## 8. Conclusion

The verified analysis supports the use of put options as the most balanced hedging approach for this portfolio. Forward contracts provide certainty, but they eliminate upside participation. Put options offer downside protection while still allowing participation in favorable currency moves, and the premium cost is low relative to the size of the investment.
