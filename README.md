# 📊 Financial KPI Dashboard — End-to-End Business Intelligence Project

![Excel](https://img.shields.io/badge/Microsoft_Excel-217346?style=flat&logo=microsoft-excel&logoColor=white)
![Data Analysis](https://img.shields.io/badge/Analysis-Financial_KPI-blue)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)
![License](https://img.shields.io/badge/License-MIT-green)

> A production-grade financial analytics project covering **$62M+ in annual revenue** across 8 U.S. states — integrating Revenue, Expense, EBIT, Accounts Receivable, HR Workforce, Social Campaigns, and Customer Satisfaction into a unified executive KPI dashboard.
>
> 
![image alt](https://github.com/ParthPatilAnalyst/Financial-KPI-Dashboard-End-to-End-Business-Intelligence-Project/blob/1224c3695fbc5a177b581d61a4f59908222e0bda/Screenshot%202026-05-13%20095039.png)
---

## 📋 Table of Contents

- [Situation](#-situation)
- [Task](#-task)
- [Action](#-action)
- [Result](#-result)
- [Project Structure](#-project-structure)
- [Data Model](#-data-model)
- [Dashboard Modules](#-dashboard-modules)
- [Key Metrics Snapshot](#-key-metrics-snapshot)
- [Tech Stack](#-tech-stack)
- [Quick Start](#-quick-start)
- [Author](#-author)

---

## ⚙️ Situation

A multi-state organization operating across **8 U.S. states** (NY, VA, FL, KS, MI, TX, CO, NT) was managing its financial performance through disconnected spreadsheets with no single source of truth. The business faced four compounding problems:

- **No unified view** of Revenue, Expense, and EBIT against plan — leadership was flying blind on whether the $62M revenue target was being hit
- **Accounts receivable aging was unmonitored** — nearly **$9.89M sitting in 90+ day overdue buckets** with no visibility into collection risk by state
- **Workforce and campaign data was siloed** — 630 new hires and 286 terminations in 2022 were tracked in separate files with no link to financial performance
- **Customer satisfaction trends** across 4 years (2019–2022) and 8 states had never been connected to revenue or operational outcomes

Finance, HR, and marketing teams were each running their own reporting in isolation — creating conflicting numbers and delayed decisions.

---

## 🎯 Task

As the **lead data analyst**, the objective was to:

1. **Consolidate** 8 data streams — Current Year financials, Previous Year comparisons, Historical Revenue (2014–2021), Accounts Receivable aging, HR headcount, Social Campaign activity, and Customer Satisfaction scores — into a single structured data model
2. **Design a dynamic calculation layer** that powered Actual vs. Plan variance, YoY trends, and state-level drill-downs without manual refresh
3. **Build an interactive executive dashboard** with filterable KPIs so leadership could slice performance by state, metric type (Revenue / Expense / EBIT), and time period in real time
4. **Surface early warning signals** — identifying underperforming states, overdue AR risk, and satisfaction score gaps before they became financial incidents

---

## 🔧 Action

### Phase 1 — Data Architecture & Consolidation
Structured the workbook across **8 purpose-built sheets**, each with a clear responsibility:

| Sheet | Purpose |
|---|---|
| `CurrentYearData` | 2022 monthly Actual vs. Plan for Revenue, Expense, EBIT across 8 states |
| `PreviousYearData` | Department-level expenses by state (Operations, Strategy, Finance, Commercial, HR) |
| `HistoricalRevenue` | Actual vs. Budget revenue from 2014–2021 — 8 years of trend data |
| `Debtors` | AR aging buckets (0–30, 31–60, 61–90, 90+ days) across 12 months × 8 states |
| `HR & Campaign` | Monthly new hires, terminations, and social campaign counts per state |
| `Satisfaction` | Customer satisfaction scores (Poor/Fair/Good/Excellent) across 4 years (2019–2022) |
| `Calculations` | Dynamic engine feeding all dashboard visuals — isolates logic from raw data |
| `Dashboard` | Executive-facing interactive view — single pane of glass |

### Phase 2 — Calculations Layer Design
Built a **dedicated `Calculations` sheet** that acts as the model's engine:
- Revenue, Expense, and EBIT Actual vs. Plan variance calculations for all 8 states × 12 months
- Aggregated New Hires and Terminations net headcount change by state and month
- Expense trend derivations over time using structured reference logic
- All dashboard visuals reference `Calculations` — raw data sheets are never touched directly, ensuring auditability and refresh safety

### Phase 3 — Financial KPI Analysis
- Tracked **$62.01M Actual Revenue vs. $62.29M Plan** — a -0.4% variance requiring state-level investigation
- Computed **$16.23M EBIT at 26.2% margin** against plan, isolating where expenses were driving the gap
- Analysed **$45.78M Actual Expenses vs. $52.36M Plan** — a 12.5% underspend that improved EBIT but signalled possible under-investment
- Broke down performance by department category: Operations, Strategy, Finance, Commercial, HR — across Previous Year data

### Phase 4 — Accounts Receivable Aging Analysis
- Mapped **12 months of AR aging** across 8 states into 4 buckets: 0–30, 31–60, 61–90, 90+ days
- Identified **$9.89M in 90+ day overdue balances** — the highest-risk collection exposure
- Tracked AR deterioration trends month-over-month to flag states where collection cycles were lengthening

### Phase 5 — HR Workforce Tracking
- Consolidated **630 new hires and 286 terminations** across all 8 states for 2022
- Computed net headcount change by state and month — surfacing seasonal hiring patterns and turnover spikes
- Linked workforce changes to state-level revenue performance to identify capacity risk

### Phase 6 — Social Campaign & Satisfaction Analysis
- Tracked marketing campaigns across **3 social channels** (Facebook, Instagram, TikTok) across Q1 2022 for all 8 states
- Analysed **4 years of customer satisfaction trends (2019–2022)** across all states using Poor / Fair / Good / Excellent / Value scores vs. Target benchmarks
- Identified states where satisfaction scores were consistently below the 0.9 target threshold

### Phase 7 — Executive Dashboard Build
- Built a single-pane **interactive `Dashboard` sheet** with department-level Expenditure, PY vs. CY comparison, and Var % columns
- Designed the dashboard to be **driven entirely by the Calculations layer** — no hard-coded values, fully refreshable
- Applied consistent visual formatting and colour-coded variance indicators for at-a-glance executive consumption

---

## 📊 Result

| KPI | Value |
|---|---|
| Total CY Revenue (Actual) | **$62.01M** |
| Total CY Revenue (Plan) | **$62.29M** |
| Revenue vs Plan Variance | **-0.4%** |
| Total CY EBIT | **$16.23M** |
| EBIT Margin | **26.2%** |
| Total CY Expense (Actual) | **$45.78M** |
| Expense vs Plan | **12.5% underspend** |
| 90+ Day Overdue AR | **$9.89M** flagged for collection review |
| New Hires (2022) | **630** across 8 states |
| Terminations (2022) | **286** across 8 states |
| Historical Data Coverage | **2014–2022 (9 years)** |
| States Covered | **8** (NY, VA, FL, KS, MI, TX, CO, NT) |
| Dashboard Sheets | **8** purpose-built data + calculation layers |

### Top Business Insights Delivered

| # | Insight | Business Impact |
|---|---------|-----------------|
| 1 | Revenue within -0.4% of plan — but 3 states dragging the average | Targeted state-level intervention vs. broad action |
| 2 | Expenses 12.5% below plan — EBIT boosted but under-investment risk flagged | Finance team alerted to re-forecast Q4 capex |
| 3 | $9.89M in 90+ day AR — concentrated in specific states | Collections team prioritised by state exposure |
| 4 | Net +344 headcount in 2022 — but termination spikes in Q1 and Q4 | HR adjusted onboarding and retention programmes |
| 5 | Several states consistently below 0.9 satisfaction target | Customer success team re-allocated to at-risk states |

---

## 📁 Project Structure

```
financial-kpi-dashboard/
│
├── FinancialKPI_FINAL.xlsx          # Master workbook (all sheets below)
│   ├── CurrentYearData              # 2022 monthly Revenue / Expense / EBIT (Actual + Plan)
│   ├── PreviousYearData             # Dept-level expenses by state (PY)
│   ├── HistoricalRevenue            # 2014–2021 Actual vs Budget revenue
│   ├── Debtors                      # AR aging: 0-30 / 31-60 / 61-90 / 90+ days
│   ├── HR & Campaign                # Hires, terminations, social campaign counts
│   ├── Satisfaction                 # Customer satisfaction scores 2019–2022
│   ├── Calculations                 # Dynamic engine — all KPI derivations
│   └── Dashboard                    # Executive interactive view
│
└── README.md
```

---

## 🗂️ Data Model

```
CurrentYearData ──────────────────────┐
PreviousYearData ─────────────────────┤
HistoricalRevenue ────────────────────┤──► Calculations ──► Dashboard
Debtors ──────────────────────────────┤         │
HR & Campaign ────────────────────────┤         └──► KPI Cards
Satisfaction ─────────────────────────┘             Variance %
                                                     Trend Lines
                                                     AR Aging View
```

All raw sheets feed into `Calculations`. The `Dashboard` consumes only `Calculations` — keeping raw data immutable and the reporting layer fully dynamic.

---

## 📈 Dashboard Modules

| Module | Metrics |
|---|---|
| **Financial Summary** | Revenue / Expense / EBIT — Actual vs Plan, Var % |
| **Department Expenditure** | Operations, Strategy, Finance, Commercial, HR — PY vs CY |
| **Historical Revenue Trend** | 2014–2022 Actual vs Budget by state |
| **AR Aging** | 0–30 / 31–60 / 61–90 / 90+ day buckets — 12-month view per state |
| **Workforce Summary** | Monthly new hires vs terminations — net headcount by state |
| **Social Campaigns** | Facebook / Instagram / TikTok campaign counts by state |
| **Customer Satisfaction** | Poor / Fair / Good / Excellent / Value vs Target — 2019–2022 |

---

## 🔢 Key Metrics Snapshot

```
Revenue Performance
───────────────────────────────────────────
  Actual   :  $62.01M
  Plan     :  $62.29M
  Variance :  -0.4%  ⚠️  Slightly below target

EBIT Performance
───────────────────────────────────────────
  EBIT     :  $16.23M
  Margin   :  26.2%  ✅  Above typical industry benchmark

Expense Control
───────────────────────────────────────────
  Actual   :  $45.78M
  Plan     :  $52.36M
  Underspend: -12.5%  ℹ️  Review Q4 planned capex

Accounts Receivable Risk
───────────────────────────────────────────
  90+ Days :  $9.89M  🔴  Priority collection review

Workforce (2022)
───────────────────────────────────────────
  New Hires      :  630
  Terminations   :  286
  Net Headcount  : +344
```

---

## 🛠️ Tech Stack

| Tool | Usage |
|---|---|
| **Microsoft Excel** | Data architecture, calculation engine, dashboard design |
| **Structured Data Modelling** | 8-sheet model with separation of raw data, logic, and presentation |
| **Dynamic Formulas** | Variance calculations, YoY comparisons, AR aging trends |
| **Dashboard Design** | KPI cards, variance indicators, department scorecards |

---

## 🚀 Quick Start

### 1. Clone the repository
```bash
git clone https://github.com/yourusername/financial-kpi-dashboard.git
cd financial-kpi-dashboard
```

### 2. Open the workbook
```
Open FinancialKPI_FINAL.xlsx in Microsoft Excel (2016 or later recommended)
```

### 3. Navigate the workbook
```
Start on the Dashboard sheet for the executive view.
Use the Calculations sheet to trace any KPI back to its source.
Raw data sheets (CurrentYearData, Debtors, etc.) are read-only inputs.
```

### 4. Refresh / update data
```
Update values in the raw data sheets only.
All Calculations and Dashboard visuals refresh automatically.
Never edit the Calculations sheet formulas directly.
```

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

*If this project helped you, consider giving it a ⭐ on GitHub!*
