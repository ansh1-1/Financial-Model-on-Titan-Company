# 📊 Titan Company Ltd — Comprehensive Financial Model

> **Data Source:** Screener.in · **Model Version:** 2.1 · **Coverage Period:** FY2017–FY2024 (Annual) + FY2023–FY2025 (Quarterly)

---

## 🗂️ Table of Contents

1. [Project Overview](#project-overview)
2. [Model Architecture](#model-architecture)
3. [Sheet-by-Sheet Description](#sheet-by-sheet-description)
4. [Key Financial Trends](#key-financial-trends)
5. [Valuation Summary](#valuation-summary)
6. [Beta & Risk Analysis](#beta--risk-analysis)
7. [Peer Comparison](#peer-comparison)
8. [Assumptions & Methodology](#assumptions--methodology)
9. [How to Use This Model](#how-to-use-this-model)
10. [Limitations & Disclaimers](#limitations--disclaimers)

---

## 📌 Project Overview

This Excel-based financial model performs a **full-spectrum fundamental analysis** of **Titan Company Limited** (NSE: TITAN), one of India's largest lifestyle companies with dominant positions across watches, jewellery (Tanishq), eyewear, and accessories.

### What this model covers:
- 10-year historical Profit & Loss, Balance Sheet, and Cash Flow analysis
- Quarterly financial tracking (10 quarters)
- **Discounted Cash Flow (DCF) valuation** with intrinsic value per share
- **Weighted Average Cost of Capital (WACC)** using peer comparables
- **Beta regression analysis** (5-year monthly data) for Titan and five jewellery sector peers
- Operating & financial ratio trend analysis
- Best-case / worst-case revenue and profit scenarios

### Company Snapshot (as of model date):
| Metric | Value |
|---|---|
| Current Price | ₹4,246 |
| Market Capitalization | ₹3,76,912 Cr |
| Face Value | ₹1 |
| No. of Shares | ~88.77 Cr |
| Trailing EPS | ₹53.69 |
| Trailing P/E | 79.1x |

---

## 🏗️ Model Architecture

The workbook contains **12 active sheets** organized into four functional layers:

```
┌─────────────────────────────────────────────────────────────┐
│  RAW DATA LAYER                                             │
│  └── Data Sheet (master input) · Raw FS (raw financials)   │
├─────────────────────────────────────────────────────────────┤
│  HISTORICAL ANALYSIS LAYER                                  │
│  └── Profit & Loss · Quarters · Balance Sheet · Cash Flow  │
├─────────────────────────────────────────────────────────────┤
│  VALUATION LAYER                                            │
│  └── Intrinsic Growth · WACC · DCF                         │
├─────────────────────────────────────────────────────────────┤
│  MARKET & RISK LAYER                                        │
│  └── Titan Beta Regression · Bluestone · Kalyan J ·        │
│      Thangamayil J · P N Gadgil J Regression               │
└─────────────────────────────────────────────────────────────┘
```

---

## 📋 Sheet-by-Sheet Description

### 1. `Data Sheet` — Master Data & Control Hub
The backbone of the model. All financial data flows from here to other sheets. Contains:
- **Company metadata**: Name, model version, share count, face value, current price, market cap
- **Annual P&L data**: Sales, COGS breakdown (raw materials, power, employee cost, selling & admin), depreciation, interest, taxes, net profit, dividends, EBITDA — all across 10 fiscal years
- **Quarterly data**: 10 quarters of revenue, expenses, operating profit, net profit, and OPM
- **Balance sheet**: Equity capital, reserves, borrowings, other liabilities, net block, investments, inventory, receivables, cash
- **Cash flow**: Operating, investing, and financing activities by year
- **Price data**: Annual stock price per year

### 2. `Profit & Loss` — Annual P&L with Trend Analytics
Structured annual income statement with computed ratios and pre-built trend analytics:

| Column Block | Content |
|---|---|
| Historical (10 years) | Sales, Expenses, Operating Profit, Other Income, Depreciation, Interest, PBT, Tax, Net Profit, EPS, P/E, Price |
| Ratios | Dividend Payout Ratio, OPM (Operating Profit Margin) |
| Trend Block | Sales Growth CAGR, OPM, and P/E — across 10Y / 7Y / 5Y / 3Y / Recent / Best / Worst horizons |
| Forecasts | Trailing twelve months (TTM), Best Case, Worst Case for Sales and Net Profit |

### 3. `Quarters` — Quarterly P&L Tracker
Rolling 10-quarter income statement (Q1 FY23 through Q3 FY25) tracking:
- Sales, Expenses, Operating Profit
- Other Income, Depreciation, Interest
- PBT, Tax, Net Profit
- OPM (Operating Profit Margin) per quarter

### 4. `Balance Sheet` — 10-Year Balance Sheet Summary
Annual balance sheet with derived metrics:
- Liabilities: Equity capital, reserves, borrowings, other liabilities
- Assets: Net block, CWIP, investments, other assets
- **Efficiency Ratios**: Debtor Days, Inventory Turnover
- **Return Ratios**: Return on Equity (RoE), Return on Capital Employed (RoCE)

### 5. `Cash Flow` — Annual Cash Flow Statement
Three-section cash flow across 10 years:
- Cash from Operations
- Cash from Investing
- Cash from Financing
- Net Cash Flow

### 6. `Raw FS` — Detailed Raw Financial Statements
Granular 12-year financial data (older historical data pre-dating the main P&L sheet):
- Full asset and liability decomposition (land, building, plant, machinery, furniture, etc.)
- Individual inventory, receivable, and payable movements
- Full capex, investment flow, and financing activity detail

### 7. `Intrinsic Growth` — ROIC & Reinvestment Rate Analysis
Foundational inputs for the DCF growth rate:
- **Net Working Capital** calculation (current assets minus current liabilities, last 5 years)
- **Non-current asset composition** (gross block, accumulated depreciation, net block)
- **Invested Capital** = Net Working Capital + Net Non-current Assets
- **ROIC** (Return on Invested Capital) = EBIT(1-T) / Invested Capital
- **Reinvestment Rate** = (Net Capex + Change in WC) / EBIT(1-T)
- **Intrinsic Growth Rate** = ROIC × Reinvestment Rate
- Uses 4-year median (~10.2%) as the reinvestment rate input to DCF

### 8. `WACC` — Cost of Capital Estimation
Full bottom-up WACC build using peer comparables:

**Peer Beta Table (6 Indian jewellery companies):**
| Company | Levered Beta | Unlevered Beta | D/E Ratio |
|---|---|---|---|
| Titan Company | 1.195 | 1.168 | 3.3% |
| Kalyan Jewellers | 0.057 | 0.053 | 12.3% |
| Thangamayil Jewellery | 1.068 | 1.001 | 9.6% |
| P N Gadgil Jewellers | -0.423 | -0.380 | 16.3% |
| PC Jeweller | 2.541 | 2.194 | 22.6% |
| Bluestone Jewellery | -1.708 | -1.419 | 29.1% |

**WACC Calculation Summary:**
| Input | Value |
|---|---|
| Risk-Free Rate (10Y G-Sec) | 7.04% |
| Equity Risk Premium | 8.11% |
| Comps Median Unlevered Beta | 0.527 |
| Target D/E Ratio | 14.93% |
| Re-levered Beta (for WACC) | 0.661 |
| Cost of Equity | 12.40% |
| Pre-tax Cost of Debt | 8.40% |
| After-tax Cost of Debt | 5.88% |
| Equity Weight | 87.0% |
| Debt Weight | 13.0% |
| **WACC** | **11.56%** |

### 9. `DCF` — Discounted Cash Flow Valuation
5-year explicit forecast + terminal value model:

| Parameter | Value |
|---|---|
| Base EBIT | ₹5,488 Cr |
| Tax Rate | 25% |
| Expected Growth Rate (intrinsic) | 14.33% |
| Terminal Growth Rate | 6.50% |
| WACC | 11.56% |
| Reinvestment Rate (4Y median) | 10.23% |

**Valuation Bridge:**
| Component | Amount (₹ Cr) |
|---|---|
| PV of Explicit FCFFs (5 years) | 21,018 |
| PV of Terminal Value | 99,778 |
| Value of Operating Assets | 1,20,796 |
| (+) Cash | 1,584 |
| (−) Debt | 18,096 |
| **Equity Value** | **1,04,284 Cr** |
| **Intrinsic Value per Share** | **₹1,175** |
| Current Market Price | ₹4,246 |
| **Premium to Intrinsic Value** | **261% (2.61x)** |

> ⚠️ The stock is trading at a significant **premium to DCF intrinsic value**, suggesting the market is pricing in high long-term growth expectations beyond the model's 5-year horizon.

### 10–14. Beta Regression Sheets
Separate OLS regression sheets for each peer using 5-year monthly return data against Nifty 50:

| Sheet | Company | Observations | R² | Adj. Beta |
|---|---|---|---|---|
| Titan Beta Regression | Titan Company | 60 months | 0.402 | **1.146** |
| Bluestone Jewel Regression | Bluestone Jewellery | 9 months | 0.240 | -1.031 |
| Kalyan J Regression | Kalyan Jewellers | 57 months | 0.0002 | 0.293 |
| Thangamayil J Regression | Thangamayil Jewellery | 60 months | 0.075 | 1.051 |
| P N Gadgil J Regression | P N Gadgil Jewellers | ~12 months | 0.087 | -0.067 |

**Adjusted Beta formula used:** `Adjusted Beta = 0.75 × Raw Beta + 0.25 × 1`
This is the **Blume adjustment** method, which pulls betas toward the market mean of 1 over time.

---

## 📈 Key Financial Trends

### Revenue Growth
- Sales grew from **₹11,276 Cr (FY17)** to **₹60,456 Cr (FY24)** — a **~5.4x increase over 7 years**
- **10-Year Sales CAGR: ~20.5%**
- **5-Year Sales CAGR: ~23.5%** — acceleration driven by jewellery segment post-COVID
- **3-Year Sales CAGR: ~28.0%** — the strongest period, reflecting pent-up demand and Tanishq expansion
- Recent (trailing) sales reached **₹75,580 Cr**, suggesting continued strong momentum
- Quarterly data shows **₹25,416 Cr** in Q3 FY25 — the highest single quarter on record

### Profitability
- **Operating Profit Margin (OPM)** has been remarkably stable, ranging between **7.97% and 12.03%** over 10 years
- 10-year average OPM: **~10.26%** — consistent despite revenue scale-up
- Net profit grew from **₹675 Cr (FY17)** to **₹3,337 Cr (FY24)** — a **~4.9x increase**
- COVID year FY21 was a disruption: net profit fell sharply to **₹973 Cr** before recovering strongly
- EBITDA grew from **₹1,007 Cr to ₹6,181 Cr**, a near 6x expansion
- Trailing twelve-month net profit: **₹4,766 Cr**

### Earnings Per Share (EPS)
- EPS moved from **₹7.60 (FY17)** to **₹37.59 (FY24)** — ~**5x growth**
- Trailing EPS: **₹53.69** — highest on record
- Share count has remained virtually constant (~88.78 Cr shares), meaning EPS growth directly mirrors net profit growth with no dilution

### Valuation Multiple (P/E)
- Historical P/E has ranged between **44.6x (FY17) and 142x (FY21)**
- FY21 anomaly driven by COVID-depressed earnings with a recovering stock price
- P/E has stabilized in the **79x–97x** range in recent years (FY22–FY25)
- Current P/E: **~79x** — expensive by absolute standards but compressed from the 100x+ seen in FY22–FY23

### Balance Sheet Trends
- **Total assets** grew from **₹6,342 Cr (FY17)** to **₹40,645 Cr (FY24)** — a ~6.4x increase
- **Borrowings** have risen significantly: from **₹113 Cr (FY17)** to **₹20,777 Cr (FY24)**
  - This is primarily driven by short-term gold metal lease borrowings and lease liabilities (Ind AS 116), not traditional debt
- **Inventory** is by far the largest asset, growing from **₹4,447 Cr to ₹28,184 Cr** — reflects jewellery's gold-heavy, consignment-style business model
- **Reserves** grew from **₹3,418 Cr to ₹11,535 Cr**, indicating strong retained earnings accumulation

### Return Ratios
- **Return on Equity (RoE)** peaked at **37.2% in FY23** — exceptional for the sector
- RoE in FY24 was **28.7%** — moderating but still strong
- **Return on Capital Employed (RoCE)** ranged from **13.1% (FY21)** to **25.1% (FY22)**, currently at ~**19.1% (FY24)**
- The post-COVID recovery (FY22–FY23) saw the best return metrics in Titan's recent history

### Inventory & Debtor Efficiency
- **Debtor Days** have stayed remarkably low — between **5.4 to 7.8 days** — reflecting that most jewellery sales are cash/card transactions with minimal credit
- **Inventory Turnover** (Sales/Inventory) declined from **2.72x (FY17) to ~2.15x (FY24)**, suggesting slightly slower inventory rotation as the company holds more gold inventory
- This is not necessarily a concern; it reflects expansion of the retail footprint

### Cash Flow Trends
- Operating cash flow has been **volatile** due to large working capital swings driven by gold inventory build-up
- Notable negative OCF years: FY19 (-₹51 Cr), FY21 (-₹348 Cr), FY22 (-₹724 Cr), FY24 (-₹541 Cr)
- Large inventory investments in FY22 and FY24 drove negative OCF despite strong profits
- The business model is **capital-light on fixed assets** but **capital-intensive on working capital** (gold procurement)
- Investing activities fluctuate due to active treasury/investment management (gold investments, subsidiary investments)

### Dividend Trend
- Dividend payout ratio has been relatively consistent: **23–37% of net profit**
- FY24 dividend: ₹979 Cr on a net profit of ₹3,337 Cr (~29% payout)

---

## 💰 Valuation Summary

| Metric | Value |
|---|---|
| DCF Intrinsic Value per Share | ₹1,175 |
| Current Market Price | ₹4,246 |
| Premium to Intrinsic Value | ~261% |
| Trailing P/E | 79.1x |
| 10Y Sales CAGR | 20.5% |
| 10Y Earnings CAGR | ~17–18% |
| WACC | 11.56% |
| Terminal Growth Rate (assumed) | 6.50% |

The large gap between DCF value and market price is typical for quality consumer compounders in India. The market implicitly assigns Titan a much longer runway of high growth than the 5-year explicit period modeled here. An alternative interpretation is that the **terminal growth rate or WACC assumption would need to be significantly adjusted** to bridge the gap.

---

## 📉 Beta & Risk Analysis

### Titan (5-Year Monthly Regression vs. Nifty 50)
- **Raw Beta: 1.195** — slightly more volatile than the broader market
- **Adjusted Beta (Blume): 1.146** — modest reduction toward market mean
- **R² = 0.402** — about 40% of Titan's monthly return variance is explained by Nifty movements; remaining 60% is idiosyncratic (company-specific)
- **Beta is statistically significant** at <1% level (p-value: 5.33e-08; F-stat: 39.0)
- Beta drifting analysis confirms stability across 3 sub-periods (Beta 1 ≈ Beta 2 ≈ Beta 3 ≈ 1.195)

### Interpretation
Titan behaves as a **mildly high-beta consumer discretionary stock**. In bull markets it slightly outperforms Nifty; in downturns it falls slightly more. Its 40% R² is moderate — the business is exposed to macro cycles but also driven by its own brand, product launches, and jewellery demand cycles.

---

## 👥 Peer Comparison

| Company | Adj. Beta | R² | Data Period |
|---|---|---|---|
| Titan Company | 1.146 | 0.402 | 5 years |
| Thangamayil Jewellery | 1.051 | 0.075 | 5 years |
| Kalyan Jewellers | 0.293 | ~0.0002 | 5 years |
| P N Gadgil Jewellers | -0.067 | 0.087 | ~12 months |
| Bluestone Jewellery | -1.031 | 0.240 | ~9 months |
| PC Jeweller | 2.540 | — | 5 years |

Key observations:
- **Kalyan Jewellers** shows near-zero beta and negligible R², suggesting it trades independently of the market — possibly driven by promoter actions and sector-specific news
- **Bluestone** and **P N Gadgil** have very short data histories (newly listed), leading to unreliable beta estimates
- **PC Jeweller** has a very high beta (2.54) reflecting its high financial leverage and past governance issues
- **Titan** has the most robust and statistically meaningful beta among the peers

---

## ⚙️ Assumptions & Methodology

| Parameter | Value | Basis |
|---|---|---|
| Tax Rate | 25% (Marginal) | India corporate tax rate (new regime) |
| Risk-Free Rate | 7.04% | 10-year Indian Government Bond yield |
| Equity Risk Premium | 8.11% | Implied ERP for India (Damodaran methodology) |
| Beta (for WACC) | 0.661 | Re-levered at target D/E using comps median unlevered beta |
| Target D/E | 14.93% | Comps median |
| Cost of Debt (pre-tax) | 8.40% | Estimated from interest/borrowings |
| Expected Growth (Phase 1) | 14.33% | 4-year average intrinsic growth (ROIC × Reinvestment Rate) |
| Terminal Growth Rate | 6.50% | Long-run India nominal GDP growth proxy |
| Mid-year Convention | Applied | PV calculated at mid-year for realism |

---

## 🚀 How to Use This Model

1. **Start with `Data Sheet`** — all master inputs are here. Update price, share count, or financial data here and it propagates through the model.

2. **Review `Profit & Loss`** and `Balance Sheet` for historical context and trend ratios.

3. **Check `Intrinsic Growth`** to understand the ROIC/reinvestment dynamics driving the DCF growth assumption.

4. **Open `WACC`** to validate or adjust cost of capital inputs (risk-free rate, ERP, beta selection).

5. **Go to `DCF`** to see the final intrinsic value. Key levers to stress-test:
   - Change the **terminal growth rate** (currently 6.5%) — every 50bps changes intrinsic value significantly
   - Change the **WACC** — every 50bps change meaningfully moves the output
   - Adjust the **reinvestment rate** (currently using 4Y median of ~10.2%)

6. **Review regression sheets** for beta context when re-assessing the WACC beta input.

### Sensitivity Analysis (suggested additions):
- Build a 2D sensitivity table: Intrinsic Value vs. (Terminal Growth Rate × WACC)
- Create a Monte Carlo layer with distributions for growth rate and WACC
- Add a reverse DCF to calculate what growth rate the current market price implies

---

## ⚠️ Limitations & Disclaimers

- **This model is for educational and research purposes only.** It does not constitute investment advice.
- The intrinsic value per share (₹1,175) is **not a price target**. The large discount to market price reflects the model's conservative 5-year explicit period and does not account for Titan's brand optionality, new business segments (Caratlane, ABFRL partnership), or international expansion.
- **Beta estimates for recently-listed peers** (Bluestone, P N Gadgil) are based on very limited data (~9–12 months) and should be interpreted with caution.
- **Kalyan Jewellers' near-zero beta** may reflect trading dynamics specific to that stock rather than true market independence.
- Financial data sourced from **Screener.in** and may differ slightly from audited annual reports due to reclassifications.
- The model uses **consolidated financials** for Titan, which includes subsidiaries like Tanishq, Fastrack, Titan Eye+, Caratlane, etc.
- **Gold price risk**: A significant portion of Titan's balance sheet (inventory) is exposed to gold price movements, which is not explicitly modeled here.
- All figures are in **Indian Rupees (₹ Crores)** unless stated otherwise.

---

## 📁 File Structure

```
Titan_Company.xlsx
├── Data Sheet          ← Master input layer (do not delete formulas)
├── Profit & Loss       ← Annual P&L + Trend Analytics
├── Quarters            ← Quarterly P&L (10 quarters)
├── Balance Sheet       ← Annual Balance Sheet + Return Ratios
├── Cash Flow           ← Annual Cash Flow Summary
├── Raw FS              ← Detailed 12-year raw financials
├── Intrinsic Growth    ← ROIC, Reinvestment Rate, Intrinsic Growth
├── WACC                ← Full WACC build with peer comps
├── DCF                 ← DCF Valuation & Intrinsic Value per Share
├── Titan Beta Regression     ← 5Y OLS regression, Titan vs Nifty
├── Bluestone Jewel Regression
├── Kalyan J Regression
├── Thangamayil J Regression
└── P N Gadgil J Regression
```

---

## 📚 References & Further Reading

- Damodaran, A. — *Investment Valuation* (3rd Ed.) — DCF, WACC, Beta methodology
- Screener.in — Source of financial data
- Blume, M.E. (1971) — *"On the Assessment of Risk"*, Journal of Finance — Blume beta adjustment
- Ind AS 116 — Lease accounting standard (relevant to Titan's borrowings jump)
- NSE/BSE filings — Titan Company Annual Reports

---

*Model built using Screener.in data. Last updated as per model version 2.1.*
