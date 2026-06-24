# Methodology

This document explains how the performance metrics, session classifications, and dashboards in this project are calculated. It serves as a reference for replicating or extending the analysis.

---

## Performance Metrics

### Win Rate
- Formula:  
  `Win Rate = (Number of Winning Trades ÷ Total Trades)`

### Average Profit/Loss
- Formula:  
  `Average P/L = SUM(Pips) ÷ Total Trades`

### Expectancy
- Formula:  
  `Expectancy = (Win% × AvgWin) – (Loss% × AvgLoss)`

### Sharpe Ratio
- Formula (approximation in Excel):  
  `Sharpe = AVERAGE(Returns) ÷ STDEV(Returns)`  
  - Returns can be measured in pips or % change per trade.

### Max Drawdown
- Method:
  - Track cumulative equity curve.
  - Calculate running peak equity.
  - Measure largest drop from peak to trough.

---

## Session Definitions (GMT +2)

Sessions are classified based on trade execution time:

- **Asian Session** → 01:00 – 09:00 (XM time) : (00:00 – 08:00 SAST in winter, 01:00 – 09:00 SAST in summer)
- **London Session** → 09:00 – 17:00 (XM time) : (08:00 – 16:00 SAST in winter, 09:00 – 17:00 SAST in summer)
- **New York Session** → 15:00 – 23:00 (XM time) : (14:00 – 22:00 SAST in winter, 15:00 – 23:00 SAST in summer)

---

## Weekday Performance

- Derived from the `Date of execution` column using:  
  `=TEXT(Date,"dddd")`
- Aggregated with PivotTables to show average P/L and win rate by weekday.

---

## Equity Curve

- Cumulative sum of trade results (`Pips`) over time.
- Formula example:  
  `=SUM($H$2:H2)`  
  (assuming column H contains Pips).

---

## Dashboards

Dashboards combine:
- Equity curve line chart
- Bar charts for weekday and session performance
- KPI cards for Win Rate, Avg P/L, Expectancy, Sharpe Ratio, Max Drawdown
- Slicers for filtering by session, weekday, or trade direction

---

##  Notes
- All calculations are performed in Excel using formulas, PivotTables, and charts.
- Definitions may be updated as the project evolves.
