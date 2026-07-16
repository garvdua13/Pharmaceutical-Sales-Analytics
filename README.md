Pharmaceutical Sales Analysis

![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Python](https://img.shields.io/badge/Python-EDA-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Status](https://img.shields.io/badge/Status-Placement%20Ready-2E7D32?style=for-the-badge)

Power BI and Python case study for analyzing pharmaceutical wholesale and retail sales across distributors, customers, products, cities, channels, and sales teams.

<img src="images/pharma-title-image.png" width="1000" height="500" alt="Pharmaceutical sales analysis title image" />

## Resume-ready Summary

Built an end-to-end pharmaceutical sales analytics project using **Power BI, Power Query, DAX, Python, and pandas**. The project analyzes **254,078 transactions** and **$11.80B** in net sales from **2017-2020**, identifies top revenue drivers, validates data quality, and presents executive-ready dashboard pages for business decision-making.

## Key Skills Demonstrated

- Power BI dashboarding
- Power Query transformation
- Star-schema data modeling
- DAX measure design
- Python EDA with pandas
- Data quality validation
- Business KPI analysis
- Sales performance analytics
- Dashboard storytelling
- Git-based project organization

## Business Problem

A pharmaceutical manufacturer sells through distributors instead of selling directly to end customers. The business needs visibility into distributor sales data to understand performance by product, customer, geography, channel, and sales team.

## Key Results

| Metric | Result |
|:--|:--|
| Clean transactions | 254,078 |
| Total sales | $11.80B |
| Period covered | 2017-2020 |
| Countries | 2 |
| Products | 240 |
| Customers | 751 |
| Top product class | Analgesics |
| Top product | Ionclotide |
| Top city | Butzbach |
| Top sales team | Delta |

## Project Structure

```text
.
├── app.py
├── data/
│   ├── raw/pharma-data.csv
│   ├── processed/pharma-data-clean.csv
│   └── README.md
├── docs/
│   ├── dashboard-guide.md
│   ├── data-model.md
│   ├── dax-measures.md
│   ├── power-query-transformations.md
│   └── streamlit-app.md
├── images/
├── reports/
│   ├── case-study.md
│   ├── data-quality-report.md
│   └── *.csv
├── scripts/
│   └── build_project_artifacts.py
├── data-exploration.ipynb
├── pharma-analysis.pbix
├── INSIGHTS.md
├── PROJECT_ANALYSIS.md
└── README.md
```

## Streamlit App

This project also includes a working Streamlit dashboard for interactive portfolio review.

### Quick Start

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
streamlit run app.py
```

Open the local app at `http://localhost:8501`.

The app includes sidebar filters, KPI cards, trend charts, revenue-driver analysis, sales-team comparison, map-based geography analysis, data-quality checks, recommendations, and filtered CSV download.

## Power BI Dashboard Pages

### Executive Summary

Shows total sales performance, product/product-class contribution, trend analysis, channel split, and geography. This page supports leadership review and high-level business monitoring.

Key insight: **Analgesics** is the leading product class.

<img src="images/exec-summary-page.png" alt="Executive summary report page" />

### Distributor & Customer Analysis

Shows distributor, customer, product, city, channel, and sub-channel performance. This page supports account planning and distributor relationship decisions.

Key insight: **Gerlach LLC** is the top distributor and **Mraz-Kutch Pharma Plc** is the top customer.

<img src="images/dist-cust-analysis-page.png" alt="Distributor and customer analysis report page" />

### Sales Team Performance

Shows sales contribution by team, manager, representative, product, and product class. This page supports performance review, coaching, and incentive planning.

Key insight: **Delta** is the top sales team.

<img src="images/sales-team-perform-page.png" alt="Sales team performance report page" />

## Data Quality Summary

| Check | Result |
|:--|:--|
| Missing values | 0 |
| Duplicate rows in raw data | 4 |
| Invalid prices | 0 |
| Negative quantity/sales rows | 2,633 |
| Sales formula mismatches | 0 |

Analyst decision: negative quantities and sales are retained as returns/reversals because every row still satisfies `Sales = Quantity * Price`.

## How To Reproduce

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
python scripts/build_project_artifacts.py
```

Then open:

- `app.py` with `streamlit run app.py` for the interactive web dashboard
- `data-exploration.ipynb` for the Python EDA workflow
- `pharma-analysis.pbix` for the interactive Power BI dashboard
- `INSIGHTS.md` for business findings
- `reports/case-study.md` for the presentation-style case study

## Power BI Version Note

PBIX metadata indicates the report was created from Power BI Desktop release **2022.10**. Use a current Power BI Desktop version to open and review the report.

## Limitations And Future Work

- Add margin, cost, inventory, and target data for profitability and target-attainment analysis.
- Add return reason codes to distinguish returns from corrections.
- Add automated dashboard refresh if this becomes a production workflow.
- Add market-specific views for Germany and Poland.

## Dataset Credit

Dataset credit: [Foresight BI practice data](https://foresightbi.com.ng/practice-data/3-datasets-for-your-portfolio/).
