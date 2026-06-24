# gold-rsi-divergence-excel

This project analyzes backtest results from MetaTrader using **Microsoft Excel**.  
It replicates the workflow I previously built in Python/Jupyter(gold-rsi-divergence), but now in a spreadsheet environment for easier visualization and dashboarding.

---

## 📊 Project Goals
- Calculate key **performance metrics**:
  - Win rate
  - Average profit/loss
  - Expectancy
  - Sharpe ratio
  - Max drawdown
- Evaluate **weekday performance** (Monday–Friday).
- Assess **session performance** (Asian, London, New York).
- Build an **equity curve chart** to track cumulative results.
- Create interactive **Excel dashboards** with slicers and charts.

---

## 📂 Repo Structure
- `data/` → Raw backtest CSV files.
- `analysis/` → Excel workbooks with formulas, PivotTables, and charts.
- `docs/` → Documentation of methodology and session definitions.
- `visuals/` → Exported charts and dashboard screenshots.
- `README.md` → Project overview and instructions.

---

## 🚀 Getting Started
1. Clone the repo:
   ```bash
   git clone https://github.com/iitoM77/gold-rsi-divergence-excel.git
