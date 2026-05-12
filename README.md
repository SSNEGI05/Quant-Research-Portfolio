# Quant Research Portfolio

Quantitative research projects testing popular market narratives with statistical rigor. Each project follows a hypothesis-driven approach: frame the question, gather data, test statistically, check robustness, and present findings honestly.

All notebooks are self-contained — clone the repo, open in Google Colab, and run. No API keys, no paid data, no Google Drive mounting required.

**Author:** Shubham Negi

---

## Projects

### 01 — Rate Cuts and Banking Sector Returns
**Question:** Does the popular narrative "rate cuts are bullish for bank stocks" hold up statistically?

**Markets Tested:** India (RBI → Nifty Bank) and US (Fed → XLF Financials, KBE Pure Banks)

**Key Finding:** No statistical support in India (t=0.98, p=0.34). In the US, bank stocks significantly *underperform* after rate cuts — pure banks (KBE) show -6.93% abnormal return at 30 days (t=-3.29, p=0.004). The consensus narrative is wrong in both markets.

**Methods:** Event study, one-sample t-test, multi-window robustness (5/10/15/30/60 days), regime analysis (pre vs post 2010), proxy sensitivity (XLF vs KBE)

📓 [Notebook](01-rate-cuts-bank-stocks/rate_cuts_bank_stocks_v1.ipynb) · 📄 [Research Memo](01-rate-cuts-bank-stocks/quant_memo_rate_cuts_bank_returns.docx)

---

## Methodology

Every project follows this workflow:

1. **Hypothesis** — Convert market opinion into a testable statement with null and alternative hypotheses
2. **Data** — Free sources only (yfinance, FRED, RBI/Fed public data). All biases flagged (survivorship, look-ahead, selection, data snooping)
3. **Analysis** — Statistical testing with explicit significance thresholds (p < 0.05, t > 2.0)
4. **Robustness** — Multiple windows, time periods, proxies, and regime splits
5. **Conclusion** — Honest verdict with limitations stated upfront

---

## Tools

- **Python** (pandas, numpy, scipy, matplotlib)
- **Data:** yfinance, FRED API
- **Environment:** Google Colab (no setup required)
