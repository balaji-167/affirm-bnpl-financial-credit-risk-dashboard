# Data Dictionary

This document explains the main tables and fields used in the Affirm BNPL Financial Performance & Credit Risk Dashboard.

---

## fact_bnpl_transactions_clean

| Column | Description |
|---|---|
| Transaction_ID | Unique transaction identifier |
| Customer_Age | Customer age |
| Gender | Customer gender |
| Annual_Income | Customer annual income |
| Income_Band | Income segment |
| Credit_Score | Customer credit score |
| Credit_Score_Band | Credit score segment |
| BNPL_Provider | BNPL service provider |
| Purchase_Category | Purchase category |
| Purchase_Amount | Transaction purchase value |
| Device_Type | Device used during checkout |
| Connection_Type | Internet connection type |
| Checkout_Time_Seconds | Checkout completion time |
| Browser | Browser used |
| Repayment_Status | Paid On Time, Late Payment, or Defaulted |
| Default_Flag | 1 if transaction defaulted, else 0 |
| Late_Payment_Flag | 1 if transaction was late, else 0 |

---

## fact_financial_performance_trend

| Column | Description |
|---|---|
| Fiscal Year | Reporting year |
| Revenue | Total revenue in USD millions |
| Operating Expenses | Operating expenses in USD millions |
| Operating Loss | Operating income/loss in USD millions |
| Free Cash Flow | Free cash flow in USD millions |

---

## fact_forecast_dashboard

| Column | Description |
|---|---|
| Fiscal Year | Actual or forecast year |
| Revenue | Forecast revenue in USD millions |
| Free Cash Flow | Forecast free cash flow in USD millions |
| FCF Margin % | Free cash flow as percentage of revenue |

---

## fact_scenario_dashboard

| Column | Description |
|---|---|
| Scenario | Bear, Base, or Bull valuation case |
| Enterprise Value | DCF enterprise value in USD millions |
