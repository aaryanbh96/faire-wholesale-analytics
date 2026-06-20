# Faire Wholesale Channel Analytics

End-to-end analysis of a specialty manufacturer's wholesale channel on [Faire](https://www.faire.com/) — turning raw order exports into decisions about which products to bundle, which retailers to re-engage, and where the channel is growing.

**[▶ View the rendered analysis](https://rearyan.com/faire-analysis.html)** · [rearyan.com](https://rearyan.com)

---

## What this is

A working analysis built to run a real wholesale channel, not a tutorial dataset. It starts from a raw Faire order export and produces the segmentation, basket, and retention analysis behind real merchandising and outreach decisions.

> **Note on data:** This repository runs on **synthetic data** generated to mirror the real channel's structure — order cadence, retailer mix, product co-occurrence, geographic spread. All revenue is shown as an **index** (mean order = 100), never absolute currency, and no confidential figures or retailer names are included. The analytical methods are unchanged from the production version.

## Highlights

- **Basket / co-occurrence analysis** — surfaced a trio of products appearing together in ~43% of orders, which became a bundle strategy.
- **RFM segmentation** — scored every retailer on Recency, Frequency, and Monetary value, bucketing them into *At Risk · Promising · Top Retailer* to prioritize outreach.
- **Cohort retention** — tracked whether each monthly cohort of new retailers kept ordering.
- **Overdue-reorder flagging** — learned each repeat retailer's own reorder cadence and flagged who was past due.
- **Retailer-type segmentation** — classified retailers (co-op, cafe, bottle shop, etc.) and analyzed what each type buys and how often they repeat.
- **Pareto / concentration, seasonal index, day-of-week, scenario modeling** — channel-health and what-if analysis.

## From analysis to action

| Finding | Decision it drove |
|---|---|
| A product trio co-occurs in ~43% of orders | Developed a bundle strategy to lift attach rate and AOV |
| RFM + overdue-reorder flags | Prioritized re-engagement of at-risk and past-due retailers |
| Repeat-rate and category mix by retailer type | Tailored which products to pitch to cafes vs. co-ops vs. bottle shops |
| Pareto concentration + cohort retention | Monitored over-reliance on top accounts; tracked new-cohort stickiness |

## Stack

`Python` · `pandas` · `numpy` · `matplotlib` · `seaborn` · `plotly` · `itertools` / `collections`

## Running it

```bash
pip install pandas numpy matplotlib seaborn plotly openpyxl
jupyter notebook Faire_Wholesale_Analytics_Portfolio.ipynb
```

The notebook is self-contained — the first cell generates the synthetic dataset, so it runs top to bottom with no external files. To run on real data, replace that cell with `pd.read_csv(...)`.

## Files

- `Faire_Wholesale_Analytics_Portfolio.ipynb` — the notebook (run / edit this)
- `Faire_Wholesale_Analytics_Portfolio_EXECUTED.ipynb` — pre-run version with all charts saved
- `faire-analysis.html` — standalone rendered report (also hosted at [rearyan.com/faire-analysis.html](https://rearyan.com/faire-analysis.html))

---

Built by **Aryan Bhardwaj** — operator who builds. [rearyan.com](https://rearyan.com) · [github.com/aaryanbh96](https://github.com/aaryanbh96)
