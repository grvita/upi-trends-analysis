# UPI Trends Project: Roadmap

Tick each box as you finish it. Do the phases in order.

## Phase 0: Setup (Day 1)
- [ ] Create GitHub repo `upi-trends-analysis`
- [ ] Create the folder structure (`data/raw`, `data/clean`, `sql`, `powerbi`, `images`)
- [ ] Add README.md and ROADMAP.md, then make the first commit
- [ ] Install PostgreSQL, DBeaver and Power BI Desktop

## Phase 1: Collect data (Day 1-2)
- [ ] Download UPI monthly statistics from NPCI (all available months)
- [ ] Download app-wise monthly data
- [ ] Download bank-wise data (optional)
- [ ] Save raw files untouched in `data/raw/`
- [ ] Note source URL and download date in the README

## Phase 2: Clean data (Day 2-3)
- [ ] Standardize units (volume in millions, value in crores)
- [ ] Convert months to real dates
- [ ] Remove duplicates and footnote rows
- [ ] Standardize app names
- [ ] Check for missing months
- [ ] Save clean CSVs to `data/clean/` and log every fix in `DATA_NOTES.md`

## Phase 3: Metrics and SQL (Day 3-5)
- [ ] Create tables and load clean data
- [ ] Query: YoY and MoM growth
- [ ] Query: average ticket size
- [ ] Query: CAGR
- [ ] Query: seasonality (month-of-year averages)
- [ ] Query: app market share and top-2 share
- [ ] Save everything in `sql/02_analysis.sql` with comments

## Phase 4: Power BI dashboard (Day 5-9)
- [ ] Connect data and build the Date table
- [ ] Write DAX measures (volume, value, ticket, YoY, share)
- [ ] Page 1: Growth Overview
- [ ] Page 2: Behavior and Seasonality
- [ ] Page 3: Market Structure
- [ ] Add slicers, takeaway-style titles and a source footer
- [ ] Export screenshots to `images/`

## Phase 5: Insights (Day 9-10)
- [ ] Write 3 to 5 findings as Finding → Evidence → Implication
- [ ] Add 3 recommendations
- [ ] Fill the README with real numbers

## Phase 6: Publish (Day 10-11)
- [ ] Final README check (no placeholders left)
- [ ] Push everything to GitHub
- [ ] Add the project to your resume and LinkedIn
- [ ] Write a short LinkedIn post with one key chart

## Phase 7: Interview prep (Day 11-12)
- [ ] Explain each SQL query out loud
- [ ] Explain each DAX measure
- [ ] Answer: why YoY over MoM? What does a falling ticket size mean?
- [ ] Prepare "what I would do next" (failure rates, forecasting, RBI comparison)

## Stretch goals
- [ ] 6 to 12 month forecast with stated limits
- [ ] Compare UPI with cards and NEFT using RBI data
- [ ] Festive-season analysis
