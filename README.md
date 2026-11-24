# UPI Growth and Trends Analysis

> Analysis of India's UPI payment growth, seasonality and market structure using NPCI public data.
> **Tools:** Excel · SQL (PostgreSQL) · Power BI

![Dashboard preview](images/dashboard_overview.png)
<!-- Add a screenshot after you build the dashboard -->

## 1. Business Problem

UPI is India's largest retail payment system. A fintech or bank analyst needs to know:

- How fast is UPI growing, and is the growth rate slowing?
- Is the average transaction getting smaller?
- Which months show seasonal spikes?
- How concentrated is the market among a few apps?

This project answers those questions using public NPCI data and turns the answers into recommendations.

## 2. Data Sources

| Dataset | Source | Period | Downloaded on |
|---|---|---|---|
| UPI monthly product statistics | NPCI (npci.org.in → Statistics → UPI Product Statistics) | `[start] to [end]` | `[date]` |
| UPI app-wise volume and value | NPCI | `[start] to [end]` | `[date]` |
| UPI bank-wise data (optional) | NPCI | `[start] to [end]` | `[date]` |

Raw files are in `data/raw/`. Cleaned files are in `data/clean/`.

## 3. Data Cleaning

Steps taken (fill in what you actually did):

- [ ] Standardized units: volume in millions, value in crores
- [ ] Converted month text into real dates (first day of month)
- [ ] Removed duplicate or footnote rows
- [ ] Standardized app names across years
- [ ] Checked for missing months: `[result]`

See `data/DATA_NOTES.md` for details.

## 4. Methodology

**Metrics calculated**

| Metric | Definition |
|---|---|
| Average ticket size | Value ÷ Volume |
| MoM growth | (Month − previous month) ÷ previous month |
| YoY growth | (Month − same month last year) ÷ same month last year |
| CAGR | (End ÷ Start)^(1/years) − 1 |
| Market share | App volume ÷ total volume |
| Average daily volume | Monthly volume ÷ days in month |

**Approach:** Excel for cleaning → SQL for analysis queries (`sql/`) → Power BI for the dashboard (`powerbi/`).

## 5. Key Findings

> Replace the placeholders with your real numbers.

1. **Growth:** UPI volume grew from `[X]` to `[Y]` between `[start]` and `[end]` (CAGR `[Z]%`).
2. **Growth is slowing:** YoY growth fell from `[A]%` to `[B]%`.
3. **Smaller payments:** Average ticket size moved from `₹[X]` to `₹[Y]`.
4. **Seasonality:** `[Month(s)]` consistently show the highest volumes.
5. **Concentration:** The top 2 apps hold `[X]%` of volume.

## 6. Recommendations

1. `[Recommendation tied to finding 1]`
2. `[Recommendation tied to finding 2]`
3. `[Recommendation tied to finding 3]`

## 7. Dashboard

| Page | What it shows |
|---|---|
| Growth Overview | KPIs, volume and value trend, YoY growth |
| Behavior and Seasonality | Average ticket size, month-of-year heatmap |
| Market Structure | App market share, bank breakdown |

## 8. Limitations

- Public data is aggregated, so user-level behavior cannot be analyzed.
- App-wise reporting may have changed over time: `[note anything you found]`.
- No failure or decline data was used: `[update if you add it]`.

## 9. How to Reproduce

1. Download the files listed in section 2 into `data/raw/`.
2. Run the cleaning steps in `data/DATA_NOTES.md`.
3. Load clean data into PostgreSQL using `sql/01_schema.sql`.
4. Run `sql/02_analysis.sql`.
5. Open `powerbi/upi_dashboard.pbix` and refresh the data source.

## 10. Repository Structure

```
upi-trends-analysis/
├── data/
│   ├── raw/
│   ├── clean/
│   └── DATA_NOTES.md
├── sql/
│   ├── 01_schema.sql
│   └── 02_analysis.sql
├── powerbi/
├── images/
├── README.md
└── ROADMAP.md
```

## 11. About

Built by `[Your Name]` · [LinkedIn](#) · [Email](#)

*Data source: National Payments Corporation of India (NPCI).*
