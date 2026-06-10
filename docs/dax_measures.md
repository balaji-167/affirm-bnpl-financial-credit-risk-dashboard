# DAX Measures

This document contains key DAX measures used in the Affirm BNPL Financial Performance & Credit Risk Dashboard.

---

## Transaction Measures

### Total Transactions

```DAX
Total Transactions =
COUNTROWS(fact_bnpl_transactions)
```

### Total Purchase Amount

```DAX
Total Purchase Amount =
SUM(fact_bnpl_transactions[Purchase_Amount])
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

## Dynamic Provider Drill-through Measures

### Selected Provider Title

```DAX
Selected Provider Title =
"Provider Detail View: " &
SELECTEDVALUE(
    fact_bnpl_transactions[BNPL_Provider],
    "All Providers"
)
```

## Forecast Measure

### FCF Margin %

```DAX
FCF Margin % =
DIVIDE(
    fact_forecast_dashboard[Free Cash Flow],
    fact_forecast_dashboard[Revenue]
)
```
