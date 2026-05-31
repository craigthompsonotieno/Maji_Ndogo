# Maji Ndogo — Water Access Analysis

> End-to-end data analysis of water infrastructure, service delivery, and operational inefficiencies across the fictional Maji Ndogo region — completed as part of the ALX Africa Data Science programme.

---

## Overview

Maji Ndogo is a fictional country facing a serious water crisis. This project simulates the role of a data analyst embedded within a water utility, using SQL, Python, and Power BI to turn a 60,000-record database into actionable insights for infrastructure repair and resource allocation.

The project was completed in four progressive parts, each building on the last — from basic database exploration to predictive prioritisation and stakeholder dashboards.

---

## Project Structure

```
Maji_Ndogo/
├── Scripts/              # SQL queries and Python analysis scripts
├── Data/                 # Raw and processed datasets (gitignored)
├── Visualisations/       # Power BI dashboard
├── .gitignore
└── README.md
```

---

## What the Analysis Covers

### Part 1 — Database Exploration
Explored the `md_water_services` MySQL database containing 60,000+ records across interconnected tables covering employees, water sources, visit logs, household records, and location data. Used basic SQL queries to understand table structure, variable definitions, and data relationships.

### Part 2 — Data Cleaning & Clustering
Cleaned and standardised the dataset — correcting employee records, generating email addresses, standardising phone numbers, and resolving inconsistencies in source type coding. Clustered water sources by usage patterns and queue time behaviour to identify operational bottlenecks.

### Part 3 — Analysis & Insights
Conducted in-depth analysis across five key dimensions:

- **Water source distribution** — breakdown of source types (shared taps, wells, rivers, taps in homes) by province and town
- **Queue time patterns** — average queue times by day of week, hour, and location type; identified peak demand periods and understaffed sites
- **Pollution & water quality** — mapped contamination severity across 20+ sources; flagged sources requiring urgent intervention
- **Population served** — ranked sources by number of people depending on them, accounting for shared-tap multiplier effects
- **Employee performance** — identified top-performing field surveyors and flagged data integrity issues in survey records

### Part 4 — Repair Prioritisation & Dashboards
Built a composite repair priority score combining pollution severity, population served, and access coverage. Prioritised 15+ wells for immediate intervention. Delivered findings through interactive Power BI dashboards for stakeholder reporting.

---

## Key Findings

- **Shared taps** are the dominant water source for the majority of the population, yet have the longest average queue times — up to 120+ minutes during peak hours
- **Queue time varies significantly by day of week** — Saturdays show the highest demand, while midweek periods are underutilised
- **Pollution hotspots** are concentrated in specific provinces; biological contamination is more widespread than chemical contamination
- **Rural areas** have disproportionately poor access to clean water relative to urban centres
- **15+ wells** were prioritised for repair based on combined pollution severity and population impact scores

---

## Tools & Stack

| Tool | Purpose |
|---|---|
| SQL (MySQL) | Database querying, data cleaning, aggregation |
| Python (pandas, Matplotlib) | Data processing, statistical analysis, visualisation |
| Jupyter Notebooks | Interactive analysis and documentation |
| Power BI | Stakeholder dashboards and KPI reporting |
| MySQL Workbench | Database management and query execution |

---

## Getting Started

### Prerequisites

```bash
pip install pandas matplotlib jupyter pymysql sqlalchemy
```

You will also need:
- **MySQL Workbench** with the `md_water_services` database loaded locally
- **Power BI Desktop** to open the dashboard files in `Visualisations/`

> ⚠️ The notebooks connect to a local MySQL database. They will not run on Google Colab or any environment without a local MySQL instance and the `md_water_services` database installed.

### Run the Analysis

```bash
git clone https://github.com/craigthompsonotieno/Maji_Ndogo.git
cd Maji_Ndogo
jupyter notebook
```

Open the notebooks in the `Scripts/` folder and run cells sequentially. Ensure your MySQL connection credentials are set correctly before running database-connected cells.

---

## Data

The raw data (`Data/`) is gitignored as it is proprietary to the ALX Africa Data Science programme. The dataset consists of the `md_water_services` MySQL database — a simulated but realistic water utility database with 60,000+ records.

---

## Author

**Craig Thompson Omondi Otieno**
BSc Statistics, Jomo Kenyatta University of Agriculture and Technology
[GitHub](https://github.com/craigthompsonotieno) · [LinkedIn](https://www.linkedin.com/in/craigthompsonotieno/) · [Email](mailto:craigthompsonotieno@gmail.com)
