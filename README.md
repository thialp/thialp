<div align="center">

## Hi, I'm Thiago Alpoin 👋

**People Analytics Manager · Austin, TX**<br/>
I build workforce, compensation and finance data products: SQL that reconciles to the cent, and dashboards leaders use to decide.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-thiagoalpoin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/thiagoalpoin)
[![Tableau Public](https://img.shields.io/badge/Tableau_Public-thialp-E97627?style=for-the-badge&logo=tableau&logoColor=white)](https://public.tableau.com/app/profile/thialp)
[![Figma](https://img.shields.io/badge/Figma-thialp-A259FF?style=for-the-badge&logo=figma&logoColor=white)](https://www.figma.com/@thialp)

</div>

Most of the hard work in enterprise analytics happens before anything reaches a dashboard: reconciling systems that disagree, untangling effective-dated history, making slow pipelines fast, and agreeing with Finance and HR on which number is actually right. **This GitHub is where I make that work visible.**

---

### ⭐ Start here: [People Analytics Warehouse](https://github.com/thialp/people-analytics-warehouse)

<a href="https://github.com/thialp/people-analytics-warehouse"><img src="https://raw.githubusercontent.com/thialp/people-analytics-warehouse/main/docs/brand/arcadia_logo_horizontal.svg" alt="Arcadia Systems" height="44"></a>

A complete HR data platform for **Arcadia Systems**, a made-up 42,000-person global company: two source systems, five years of history, one data model, seven case studies.

> [!NOTE]
> **Fictional company, real-world numbers.** Every person, office and salary is synthetic, generated with Claude Code from rules I designed. No employer data, logic or screenshots are used. The simulation is anchored on real public data: ECB exchange rates, researched employer costs by country, real postal codes.

| 👥 Employees | 🧰 Contractors | 🌍 Offices | 💱 Currencies | ✅ Automated tests |
|:---:|:---:|:---:|:---:|:---:|
| **30,014** | **11,941** | **35** in 22 countries | **17** | **81** |

```mermaid
flowchart LR
    BW["🟠 Supplier system<br/>contract orders, rates"]
    subgraph ARC["Arcadia"]
        KS["🔵 <b>Arcadia HR system</b><br/>system of record<br/>employees and contractors,<br/>an Arcadia ID and a PID each"]
        WH["🟣 Warehouse<br/>SQL · tests · reconciliation"]
        TAB["🔷 Tableau<br/>dashboards"]
    end
    PUB["🟢 Public data<br/>FX, employer costs"]
    DEC["⭐ Decisions"]
    BW -. "one-way feed" .-> KS
    KS ==> WH
    PUB --> WH
    WH --> TAB --> DEC
    BW -. "extract, to check the feed" .-> WH
    classDef hr fill:#dbeafe,stroke:#1d4ed8,color:#0f172a,stroke-width:3px
    classDef vms fill:#ffedd5,stroke:#c2410c,color:#0f172a,stroke-width:1px
    classDef pub fill:#dcfce7,stroke:#15803d,color:#0f172a,stroke-width:2px
    classDef wh fill:#ede9fe,stroke:#6d28d9,color:#0f172a,stroke-width:2px
    classDef tab fill:#cffafe,stroke:#0e7490,color:#0f172a,stroke-width:2px
    classDef dec fill:#fef9c3,stroke:#a16207,color:#0f172a,stroke-width:2px
    class KS hr
    class BW vms
    class PUB pub
    class WH wh
    class TAB tab
    class DEC dec
    linkStyle 0 stroke:#dc2626,stroke-width:2px
    linkStyle 5 stroke:#94a3b8,stroke-width:1px
```

### 📊 Seven case studies, one company

| | Case study | The question it answers | Status |
|---|---|---|---|
| 🪑 | **[Workforce Planning](https://github.com/thialp/people-analytics-warehouse#case-study-1-workforce-planning)** | How many positions (PIDs) do we hold, filled or vacant? Are we hiring into the ones we planned, and what did each look like before? | [![Live](https://img.shields.io/badge/Tableau-live-16a34a?logo=tableau&logoColor=white)](https://public.tableau.com/app/profile/thialp/viz/WorkforcePlanningArcadiaSystems/Dashboard) |
| 📈 | **[Headcount & FTE Walk](https://github.com/thialp/people-analytics-warehouse#case-study-2-headcount--fte-walk)** | Start + hires − leavers ± moves = end, for employees and contractors, for any team. Reconciled exactly, and fast at scale | [![Live](https://img.shields.io/badge/Tableau-live-16a34a?logo=tableau&logoColor=white)](https://public.tableau.com/app/profile/thialp/viz/arcadia_headcount_fte_walk/Dashboard) |
| 🗺️ | **[Global Workforce Footprint](https://github.com/thialp/people-analytics-warehouse#case-study-3-global-workforce-footprint)** | Where are our people, where are we growing, and who moves between offices? | ![Built](https://img.shields.io/badge/data-built-6d28d9) ![Dashboard](https://img.shields.io/badge/dashboard-coming_soon-eab308) |
| 💵 | **[Compensation Walk](https://github.com/thialp/people-analytics-warehouse#case-study-4-compensation-walk)** | Why did pay change: hires, promotions, tenure raises, employer costs or currency? | [![Live](https://img.shields.io/badge/Tableau-live-16a34a?logo=tableau&logoColor=white)](https://public.tableau.com/app/profile/thialp/viz/ArcadiaCompensationWalk/Dashboard) |
| 🧮 | **[Workforce Cost Bridge & Growth Mix](https://github.com/thialp/people-analytics-warehouse#case-study-5-workforce-cost-bridge)** | Did cost grow from more people, a different mix or pricier people? Split fairly with Shapley values, to the cent | ![Built](https://img.shields.io/badge/data-built-6d28d9) ![Dashboard](https://img.shields.io/badge/dashboard-coming_soon-eab308) |
| 🔍 | **[Contingent Workforce Reconciliation](https://github.com/thialp/people-analytics-warehouse#case-study-6-contingent-workforce-reconciliation)** | Do the HR system and the supplier system agree on who works here? Every disagreement found, explained and routed (100% of planted issues detected) | ![Built](https://img.shields.io/badge/data-built-6d28d9) ![Dashboard](https://img.shields.io/badge/dashboard-coming_soon-eab308) |
| 🔮 | **[PID Fill Forecast](https://github.com/thialp/people-analytics-warehouse#case-study-7-pid-fill-forecast-planned)** | How many PIDs will growth and attrition open, and how fast can we fill them? | ![Planned](https://img.shields.io/badge/status-planned-94a3b8) |

<a href="https://public.tableau.com/app/profile/thialp/viz/WorkforcePlanningArcadiaSystems/Dashboard"><img src="https://raw.githubusercontent.com/thialp/people-analytics-warehouse/main/docs/images/workforce_planning_dashboard.png" alt="Workforce Planning dashboard on Tableau Public" width="100%"></a>

<sub>Workforce Planning on Tableau Public. Click to open the interactive dashboard.</sub>

<a href="https://public.tableau.com/app/profile/thialp/viz/arcadia_headcount_fte_walk/Dashboard"><img src="https://raw.githubusercontent.com/thialp/people-analytics-warehouse/main/docs/images/headcount_fte_walk_dashboard.png" alt="Headcount & FTE Walk dashboard on Tableau Public" width="100%"></a>

<sub>The Headcount & FTE Walk on Tableau Public. Click to open the interactive dashboard.</sub>

<a href="https://public.tableau.com/app/profile/thialp/viz/ArcadiaCompensationWalk/Dashboard"><img src="https://raw.githubusercontent.com/thialp/people-analytics-warehouse/main/docs/images/compensation_walk_dashboard.png" alt="Compensation Walk dashboard on Tableau Public" width="100%"></a>

<sub>The Compensation Walk on Tableau Public. Click to open the interactive dashboard.</sub>

---

### 🧭 How I work

| | |
|---|---|
| 🧱 **Model first** | Get the grain, keys and effective dates right before building anything visual |
| ⚖️ **Reconcile everything** | If two numbers should match, there's a test that proves they do |
| ⚡ **Performance is part of correctness** | A correct pipeline that's too slow to refresh still has a problem to solve |
| 💬 **Explain the result** | Analytics only matters if a leader can act on it |

### 🛠️ Tools

![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square)
![SQL Server](https://img.shields.io/badge/SQL_Server-CC2927?style=flat-square&logo=microsoftsqlserver&logoColor=white)
![DuckDB](https://img.shields.io/badge/DuckDB-FFF000?style=flat-square&logo=duckdb&logoColor=black)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Tableau](https://img.shields.io/badge/Tableau-E97627?style=flat-square&logo=tableau&logoColor=white)
![Figma](https://img.shields.io/badge/Figma-A259FF?style=flat-square&logo=figma&logoColor=white)
![Claude Code](https://img.shields.io/badge/Claude_Code-D97757?style=flat-square&logo=anthropic&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![Workday](https://img.shields.io/badge/Workday-0875E1?style=flat-square&logo=workday&logoColor=white)
![Alteryx](https://img.shields.io/badge/Alteryx-0078C0?style=flat-square&logo=alteryx&logoColor=white)
![Jira](https://img.shields.io/badge/Agile_·_Jira-0052CC?style=flat-square&logo=jira&logoColor=white)
![PMP](https://img.shields.io/badge/PMP-certified-1f2937?style=flat-square)

ATS & VMS data · data modeling · effective-dated history · cross-system reconciliation · AI-assisted analytics development

### 🎓 Background

10+ years across people analytics, technology consulting (Protiviti) and BI. I taught Tableau to 500+ working professionals at Emory University. B.Sc. in Mathematics, Federal University of Rio de Janeiro.

🇺🇸 English · 🇧🇷 Português · 🇪🇸 Español
