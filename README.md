# Equity Portfolio Tracker

Multi-portfolio Indian equity tracker with FIFO cost basis, live NSE prices, P&L, and Excel export.

## Local Setup

```bash
pip install -r requirements.txt
streamlit run app.py
```

Open http://localhost:8501 in your browser.

## Deploy to Streamlit Cloud (Free, Shareable URL)

1. Push this folder to a GitHub repository (can be private)
2. Go to https://share.streamlit.io
3. Click "New app" → connect your GitHub repo
4. Set Main file path: `app.py`
5. Click Deploy → get a public URL like `https://yourname-portfolio-tracker.streamlit.app`

Share the URL with anyone — no Python install needed.

## CSV Format

| Column    | Format       | Example          |
|-----------|--------------|------------------|
| Portfolio | Text         | FamilyPortfolio  |
| Date      | DD/MM/YY     | 15/01/24         |
| Ticker    | NSE symbol   | RELIANCE         |
| Action    | BUY or SELL  | BUY              |
| Quantity  | Number       | 50               |
| Price     | Number (₹)   | 2400.00          |

## Features

- FIFO cost basis calculation
- Live NSE prices via yfinance (refreshed every 5 min)
- Unrealized P&L per stock and portfolio total
- Transaction history per portfolio
- Export to formatted multi-sheet Excel
