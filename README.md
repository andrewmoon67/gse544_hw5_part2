# GSE 544 — Homework 5, Part 2

**A Copula/NCO Horse Race Under Realistic Constraints**
claude.ai and the 544_Notebooks were used to assist this homework.

## Contents

| File | Description |
|------|-------------|
| `hw5_part2.ipynb` | Main notebook — all four parts |
| `vmls_portfolio_returns.csv` | Return data (from class repo) |
| `copula_model.pkl` | Fitted copula model (from class repo or Part 1 output) |
| `requirements.txt` | Python dependencies |

## Setup

```bash
# 1. Clone the repo
git clone https://github.com/<your-username>/gse544-hw5-part2.git
cd gse544-hw5-part2

# 2. Copy in the data files from the class repo
cp /path/to/class/repo/vmls_portfolio_returns.csv .
cp /path/to/class/repo/copula_model.pkl .

# 3. Install dependencies (Anaconda recommended)
pip install -r requirements.txt

# 4. Open in Jupyter
jupyter notebook hw5_part2.ipynb
```

## Structure

- **Part (a):** Build NCO (Portfolio A), all-at-once (Portfolio B), and 1/N benchmark for γ=1 and γ=3
- **Part (b):** Out-of-sample wealth paths + log-growth histograms + summary table
- **Part (c):** Written explanation of the correlation distance metric
- **Part (d):** Synthesis — three horse-race questions answered using the results

## Key constraints vs. lecture notebook

- **No shorting:** `w_j ≥ 0` for all risky assets
- **No borrowing:** `Σw_j ≤ 1` (residual goes to risk-free at rf_bar)
- **Two regimes:** γ=1 (log utility / full Kelly) and γ=3 (CRRA)
- **Same MC draws** reused across both γ regimes for apples-to-apples comparison
