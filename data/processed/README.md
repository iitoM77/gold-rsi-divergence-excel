# Processed data 
This folder contains cleaned versions of the raw backtest results exported from MetaTrader.

##Files
-'backtest_results.xslx' - Processed dataset used for Excel analysis.

##cleaning steps
- made correction to column names i.e column G: Risk/Result > Risk/Reward
- fixed the column I: Pips > was 100 more than it should've been, made a new column for the calculation then replaced the old 1
- deleted all trades that risked below 150 pips. calculated pips risked [@[Entry price]]-[@Stop loss] then filtered to assolate then deleted them
- 

##Usage
Use this file as the input for:
- Performance metrics calculations
- Equity curve chart
- PivotTables for weekday/session analysis
- Dashboards in Excel
