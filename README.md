# Affirm BNPL Financial Performance & Credit Risk Dashboard

## 📌 Project Overview

This project analyzes **Affirm’s Buy Now, Pay Later (BNPL) financial performance, credit risk exposure, repayment behavior, and forecast-based valuation** using **Excel** and **Power BI**.

The project combines company-level financial data from **Affirm FY2022–FY2024 10-K filings** with a BNPL transaction dataset to build an end-to-end finance analytics dashboard. The final Power BI report includes executive KPIs, financial performance trends, customer credit risk analysis, provider/category risk, forecast analysis, DCF scenario valuation, and provider-level drill-through reporting.

---

## 🎥 Dashboard Demo

![Dashboard Demo](https://github.com/user-attachments/assets/1e168211-fc89-49f4-bc56-d74765fedfb9)

---

## 🎯 Business Problem

BNPL companies need to balance **growth, credit risk, profitability, and cash-flow recovery**. Strong GMV and revenue growth can create business value only if credit losses remain controlled and the company moves toward positive free cash flow.

This project answers the following business questions:

1. Is Affirm scaling GMV and revenue efficiently?
2. Are profitability and free cash flow improving over time?
3. Which customer credit segments create the highest default risk?
4. Which BNPL providers and purchase categories show higher repayment risk?
5. How sensitive is enterprise value under Bear, Base, and Bull DCF scenarios?

---

## 🛠️ Tools Used

| Tool            | Purpose                                                                    |
| --------------- | -------------------------------------------------------------------------- |
| **Excel**       | Financial model, source tracker, KPI tables, forecast and scenario tables  |
| **Power BI**    | Dashboard development, data modeling, DAX measures, slicers, drill-through |
| **Power Query** | Data cleaning and transformation                                           |
| **DAX**         | KPI calculations, default rate measures, dynamic titles, forecast ratios   |
| **GitHub**      | Project documentation and portfolio publishing                             |

---

## 🔄 Project Workflow

```text
1. Collected Affirm FY2022–FY2024 10-K filings
2. Extracted key financial, operating, funding, and profitability metrics in Excel
3. Built a structured Excel financial model with source page references
4. Cleaned and prepared BNPL transaction-level data
5. Imported Excel model and cleaned dataset into Power BI
6. Created DAX measures for KPIs, default rate, dynamic year selection, FCF margin, and drill-through titles
7. Built six Power BI report pages:
   - Executive Summary
   - Financial Performance
   - Credit Risk Analysis
   - Provider & Category Risk
   - Forecast & Scenario
   - Provider Detail Drill-through
8. Added slicers, conditional formatting, matrix heatmaps, scenario analysis, and provider drill-through
9. Documented assumptions, limitations, DAX measures, and data dictionary in GitHub
```

---

## 📂 Repository Structure

```text
affirm-bnpl-financial-credit-risk-dashboard/
│
├── data/
│   ├── raw/
│   │   ├── affirm_2022_10k.pdf
│   │   ├── affirm_2023_10k.pdf
│   │   ├── affirm_2024_10k.pdf
│   │   └── bnpl_dataset_v2.csv
│   │
│   └── processed/
│       └── bnpl_transactions_clean.csv
│
├── excel/
│   └── affirm_financial_model.xlsx
│
├── powerbi/
│   └── affirm_bnpl_financial_credit_risk_dashboard.pbix
│
├── assets/
│   ├── demo/
│   │   └── affirm_bnpl_dashboard_demo.mp4
│   │
│   └── screenshots/
│       ├── 00_excel_financial_model.png
│       ├── 01_executive_summary.png
│       ├── 02_financial_performance.png
│       ├── 03_credit_risk_analysis.png
│       ├── 04_provider_category_risk.png
│       ├── 05_forecast_scenario.png
│       └── 06_provider_detail_drillthrough.png
│
├── docs/
│   ├── dax_measures.md
│   ├── data_dictionary.md
│   └── assumptions_limitations.md
│
├── LICENSE
└── README.md
```

---

## 📊 Data Sources

This project uses two main data sources:

### 1. Affirm FY2022–FY2024 Financial Filings

Affirm’s annual reports were used to extract company-level financial and operating metrics, including:

* Gross Merchandise Volume (GMV)
* Revenue
* Take Rate
* Credit Loss Rate
* Operating Expenses
* Operating Income / Loss
* Net Income / Loss
* Free Cash Flow
* Assets, liabilities, and funding metrics

### 2. BNPL Transaction Dataset

The BNPL transaction dataset was used to analyze customer-level repayment and credit risk behavior, including:

* BNPL provider
* Purchase category
* Purchase amount
* Credit score band
* Income band
* Repayment status
* Default flag
* Late payment flag

> **Note:** Affirm financial metrics are based on company filings. The BNPL transaction dataset is used for customer-level repayment and credit risk analysis and may not represent actual Affirm internal customer records.

---

## 📘 Excel Financial Model

The Excel workbook was used as the financial modeling and data preparation layer before importing data into Power BI.

Key Excel work included:

* Extracted Affirm FY2022–FY2024 financial metrics from 10-K filings
* Built a structured source tracker with page references
* Created operating metrics, income statement metrics, balance sheet metrics, and funding metrics
* Prepared clean financial tables for Power BI
* Created forecast and DCF scenario input tables
* Used color coding to identify extracted values, reviewed inputs, and negative profitability metrics

![Excel Financial Model](assets/screenshots/00_excel_financial_model.png)

---

## 📈 Power BI Dashboard

The Power BI report contains six pages covering executive performance, financial analysis, credit risk, provider/category risk, forecasting, valuation, and drill-through analysis.

---

## 1. Executive Summary

This page summarizes Affirm’s key business and financial performance indicators across FY2022–FY2024.

### Key KPIs

* GMV
* Revenue
* Take Rate
* Credit Loss Rate
* Free Cash Flow
* Operating Margin
* Net Margin
* Debt-to-Assets

### Business Insight

Affirm showed strong platform scale, with GMV growing from **$15.5B in FY2022** to **$26.6B in FY2024** and revenue increasing from **$1.3B to $2.3B**. Take Rate recovered to **8.7%**, while Credit Loss Rate improved to **1.0%**, showing better monetization and controlled credit risk. However, Free Cash Flow remained negative, making cash generation a key area to monitor.

![Executive Summary](assets/screenshots/01_executive_summary.png)

---

## 2. Financial Performance

This page analyzes revenue growth, operating expenses, operating loss, and free cash flow trends.

### Key Analysis Areas

* Revenue vs Operating Expenses
* Operating Loss Trend
* Free Cash Flow Performance
* Year-wise KPI movement

### Business Insight

Revenue increased from **$1,349.3M in FY2022** to **$2,323.0M in FY2024**. Operating loss worsened to **-$1,200.9M in FY2023**, but improved sharply to **-$615.8M in FY2024**, showing better operating leverage and cost control.

![Financial Performance](assets/screenshots/02_financial_performance.png)

---

## 3. Credit Risk Analysis

This page analyzes repayment behavior, credit score risk, provider default rate, and customer-level risk segmentation.

### Key Analysis Areas

* Repayment status mix
* Default rate by credit score band
* Default rate by BNPL provider
* Customer credit behavior

### Business Insight

Poor credit score customers had the highest default risk at **14.3%**, far above other credit score bands, which stayed around **2.0%–2.4%**. This shows that credit score is one of the strongest drivers of default risk in the transaction dataset.

![Credit Risk Analysis](assets/screenshots/03_credit_risk_analysis.png)

---

## 4. Provider & Category Risk

This page compares provider-level exposure, purchase category default rates, and provider-category risk combinations.

### Key Analysis Areas

* Provider Risk vs Exposure
* Default Rate by Purchase Category
* Provider vs Category Risk Heatmap
* Risk pockets by provider and category

### Business Insight

Afterpay showed the highest provider-level default rate at around **10.0%**, while Sezzle had a lower default rate at around **7.8%** despite similar purchase exposure. Fashion had the highest category default rate at **8.79%**. The heatmap revealed important risk pockets such as **Afterpay + Fashion at 10.83%**, **Afterpay + Travel at 10.12%**, and **Afterpay + Home & Furniture at 10.09%**.

![Provider & Category Risk](assets/screenshots/04_provider_category_risk.png)

---

## 5. Forecast & Scenario Analysis

This page presents revenue forecast, free cash flow recovery, FCF margin improvement, and DCF enterprise value under Bear, Base, and Bull scenarios.

### Key Analysis Areas

* Revenue Forecast Trend
* Free Cash Flow Recovery
* FCF Margin %
* DCF Enterprise Value by Scenario

### Business Insight

Revenue is projected to grow from **$2.3B in FY2024A** to **$5.0B by FY2029F**. Free Cash Flow improves from **-$619.5M** to **+$94.6M**, with FCF Margin recovering from **-26.7%** to **1.9%**. DCF valuation is highly sensitive, ranging from **-$5.1B in Bear Case** to **$4.4B in Bull Case**.

![Forecast & Scenario](assets/screenshots/05_forecast_scenario.png)

---

## 6. Provider Detail Drill-through

This page provides interactive drill-through analysis for each BNPL provider.

Users can right-click a provider bubble on the Provider & Category Risk page and drill through into detailed provider-level analysis.

### Drill-through Features

* Dynamic provider title
* Provider-specific KPIs
* Default rate by purchase category
* Repayment mix by credit score band
* Default rate by credit score band
* Back button navigation

### Example Insight: Afterpay

For Afterpay, the dashboard showed **12,536 transactions**, **$7.1M purchase value**, **1,258 defaulted transactions**, and **10.04% default rate**. Risk was highest in **Fashion at 10.83%** and among **Poor credit score customers at 17.01%**.

![Provider Detail Drill-through](assets/screenshots/06_provider_detail_drillthrough.png)

---

## 🧮 Key DAX Measures

### Total Transactions

```DAX
Total Transactions =
COUNTROWS(fact_bnpl_transactions)
```

### Defaulted Transactions

```DAX
Defaulted Transactions =
CALCULATE(
    COUNTROWS(fact_bnpl_transactions),
    fact_bnpl_transactions[Repayment_Status] = "Defaulted"
)
```

### Default Rate

```DAX
Default Rate =
DIVIDE(
    [Defaulted Transactions],
    [Total Transactions]
)
```

### Dynamic Provider Drill-through Title

```DAX
Selected Provider Title =
"Provider Detail View: " &
SELECTEDVALUE(
    fact_bnpl_transactions[BNPL_Provider],
    "All Providers"
)
```

### FCF Margin %

```DAX
FCF Margin % =
DIVIDE(
    fact_forecast_dashboard[Free Cash Flow],
    fact_forecast_dashboard[Revenue]
)
```

📄 Full DAX documentation: [`docs/dax_measures.md`](docs/dax_measures.md)

---

## 💡 Key Business Insights

1. **Strong platform growth:** GMV increased from **$15.5B to $26.6B** between FY2022 and FY2024.
2. **Revenue growth:** Revenue increased to **$2.3B in FY2024**, showing strong top-line expansion.
3. **Improving credit control:** Credit Loss Rate improved to **1.0%** in FY2024.
4. **Profitability still under pressure:** Free Cash Flow remained negative despite revenue growth.
5. **Credit score is a major risk driver:** Poor credit score customers showed the highest default rate at **14.3%**.
6. **Provider-level risk matters:** Afterpay showed the highest default rate at around **10.0%**.
7. **Category-provider combinations reveal risk pockets:** Afterpay + Fashion showed the highest risk pocket at **10.83%**.
8. **Valuation is highly sensitive:** DCF enterprise value varies significantly across Bear, Base, and Bull scenarios.

---

## ✅ Business Recommendations

1. Monitor **Poor credit score customers** closely with stricter underwriting and risk controls.
2. Track **Afterpay** separately because it shows higher provider-level default risk.
3. Use provider-category heatmaps to identify early warning risk pockets.
4. Improve free cash flow conversion, as negative FCF remains a major financial risk.
5. Review forecast and DCF assumptions regularly because valuation is highly sensitive to margin expansion and cash-flow recovery.
6. Use provider-level drill-through reporting to support risk monitoring and portfolio-level decision-making.

---

## 📚 Documentation

Additional project documentation is available in the `docs/` folder:

* [`dax_measures.md`](docs/dax_measures.md) – key DAX formulas used in the dashboard
* [`data_dictionary.md`](docs/data_dictionary.md) – table and column definitions
* [`assumptions_limitations.md`](docs/assumptions_limitations.md) – project assumptions and limitations

---

## 🧠 Skills Demonstrated

### Excel

* Financial modeling
* 10-K data extraction
* Source tracking
* Structured financial tables
* Forecast and scenario tables
* KPI preparation

### Power BI

* Dashboard design
* Data modeling
* DAX measures
* Power Query transformation
* Slicers
* Conditional formatting
* Matrix heatmaps
* Drill-through navigation
* Dynamic titles

### Finance & Analytics

* GMV analysis
* Revenue analysis
* Take Rate analysis
* Credit Loss Rate analysis
* Operating margin and net margin analysis
* Free Cash Flow analysis
* DCF scenario valuation
* Credit risk segmentation
* Provider and category risk analysis

---

## ⚠️ Assumptions and Limitations

* Affirm financial metrics are based on FY2022–FY2024 reported financial data.
* BNPL transaction data is used for customer-level repayment and credit risk analysis.
* The BNPL transaction dataset may not represent actual Affirm internal customer-level records.
* Forecast and DCF outputs are analytical model assumptions created for portfolio demonstration.
* Provider-level risk analysis is based on the dataset used in this project, not official provider disclosures.
* This project is for learning and portfolio purposes and is not investment advice.

---

## 📌 Final Summary

This project demonstrates how Excel and Power BI can be used together to build a finance analytics solution covering financial performance, credit risk, provider exposure, customer repayment behavior, forecasting, and valuation scenario analysis.

The final dashboard helps stakeholders understand whether Affirm’s BNPL growth is supported by controlled credit risk, improving profitability, and long-term free cash flow recovery.

