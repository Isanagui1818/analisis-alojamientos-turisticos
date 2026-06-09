# 🏨 Tourism Accommodation Analysis — Gaia Travels
> Final project of the Business Simulator · IT Academy Barcelona Activa · Team 10

---

## 📋 Project overview

This project simulates the real work of a **Data Analytics Department** within a fictional tourism company called **Gaia Travels**. Over four sprints, the team conducted a comprehensive analysis of the Spanish tourism accommodation market: from data extraction and cleaning through to KPI generation, interactive visualisations, and a Power BI dashboard with actionable business proposals.

The project was developed within the framework of the **IT Academy Business Simulator (Barcelona Activa)**, a learning environment that replicates professional working dynamics — team meetings, agile management with a Kanban board, specialised roles, and weekly results presentations.

---

## 🎯 Objectives

- Apply a complete data analysis workflow (ETL → EDA → KPIs → Visualisation → Proposals)
- Analyse the behaviour of tourism accommodations in Spain: occupancy, overnight stays, traveller profile, and customer satisfaction
- Identify seasonality patterns, annual variations, and traveller origin
- Build an interactive Power BI dashboard to support business decision-making
- Develop concrete business proposals aligned with **Spain's Tourism Strategy 2030**

---

## ⚡ Weekly technology handicaps

One of the most distinctive features of the simulator was the introduction of a **technology handicap each week**, simulating real-world unexpected constraints. When new sprint data was released, the team received an additional technical restriction that required rethinking the approach and finding alternative solutions.

| Week | Simulated constraint | Solution adopted |
|---|---|---|
| Sprint 1 | No restriction — kick-off sprint | — |
| Sprint 2 | SQL server down — data inaccessible via database | Data delivered as CSV · direct load with pandas |
| Sprint 3 | Expired Power BI licences | Alternative visualisations with Plotly and matplotlib |
| Sprint 4 | Reduced deadline (Thursday delivery) + external benchmarking requirement | INE dataset integration · task prioritisation · intensive team coordination |

> Sprint 4 combined two simultaneous pressures: a shortened delivery deadline and a company request to benchmark internal data against real Spanish tourism market data. This required incorporating and cross-referencing external sources from the **National Statistics Institute (INE)** to contextualise Gaia Travels' KPIs within the real sector behaviour, grounding the strategic business proposals on objective data.

> This mechanism trained the team's ability to **adapt to resource-constrained environments**, make technical decisions under pressure, and find alternative solutions without compromising analysis quality — a skill directly transferable to a real professional environment.

---

## 🔄 Methodology: 4 Sprints

Each sprint was structured around a **business question** posed by Gaia Travels. The team had to answer it using the available data, respecting the week's technology handicap and delivering actionable results. Sprint 1 was the most demanding, combining the full ETL pipeline build with the first exploratory analysis. From Sprint 2 onwards, the ETL was maintained or updated only when the new sprint's data introduced structural changes, allowing the team to focus progressively on analysis and business conclusions.

### Sprint 1 — ETL + General EDA *(most demanding)*
**Business question:** What is the current state of the Spanish tourism accommodation market and which variables best explain supply behaviour?

Full ETL pipeline construction: connection to the MySQL database (`Tourist_Accommodation`) using SQLAlchemy and pandas, cleaning and transformation of variables (`bathrooms`, `bedrooms`, `beds`), null imputation by grouped medians. The resulting dataset was used for the general EDA with initial statistical and visual exploration using matplotlib and seaborn. This sprint established the clean dataset that all subsequent sprints would build upon.

### Sprint 2 — Department-level Analysis
**Business question:** What specific insights can each business area (marketing, operations, customer experience) extract to improve decision-making?

Each analyst addressed the question from their area of specialisation, diving deeper into the variables relevant to their domain. The ETL was updated to incorporate new data delivered as CSV following the SQL server outage (week's handicap).

### Sprint 3 — KPIs and Business Indicators
**Business question:** What are Gaia Travels' key performance indicators and how do they evolve?

Definition and calculation of the main KPIs: monthly occupancy rate, overall satisfaction index, highest-occupancy city, and highest-rated item. Given the expired Power BI licences (handicap), alternative interactive dashboards were generated in HTML using Plotly (`fig1_ocupacion`, `fig2_satisfaccion`, `fig3_ciudad`, `fig4_item`).

### Sprint 4 — External Benchmarking and Strategic Proposals
**Business question:** How does Gaia Travels compare to the real Spanish tourism market and where should it direct its strategy?

The company requested benchmarking internal data against real sector behaviour. **INE** datasets were integrated (travellers, overnight stays, average length of stay, annual variations by autonomous community and country of residence) to contextualise internal KPIs within the real market. The findings underpinned strategic business proposals aligned with **Spain's Tourism Strategy 2030**, all delivered under a reduced deadline (week's handicap).

---

## 📊 Tech stack

| Tool | Usage |
|---|---|
| **Python** | Data analysis, cleaning and visualisation |
| **pandas** | DataFrame manipulation and transformation |
| **matplotlib / seaborn** | Static visualisations and EDA |
| **Plotly Express** | Interactive charts exported as HTML |
| **SQLAlchemy** | MySQL database connection and querying |
| **MySQL** | Main database (`Tourist_Accommodation`) |
| **Power BI** | Final interactive dashboard |
| **Jupyter Notebook** | Development and documentation environment |
| **Git / GitHub** | Version control and team collaboration |

---

## 📁 Data sources

The data is **fictional**, generated for the simulator with a realistic structure based on the Spanish tourism accommodation market.

**Geographic coverage:** Barcelona · Girona · Madrid · Mallorca · Menorca · Sevilla · Valencia

- **MySQL database**: `Tourist_Accommodation` table containing tourism apartment data (id, name, description, room type, neighbourhood, host, bathrooms, bedrooms, beds, price, ratings, etc.)
- **INE (National Statistics Institute) datasets**:
  - Travellers and overnight stays by autonomous community and province
  - Travellers and overnight stays by tourist destination
  - Travellers and overnight stays by country of residence
  - Coefficient of variation for travellers and overnight stays
  - Annual variation in average stay, establishments, occupancy, and employees

---

## 📈 Key results

- **Power BI dashboard** with dedicated pages for occupancy, customer satisfaction, traveller profile, and temporal variations
- **KPIs tracked**: monthly occupancy rate, overall satisfaction index, city and item rankings
- **Business proposals** documented with strategic recommendations for Gaia Travels
- Trend analysis aligned with **Spain's Tourism Strategy 2030**
- External benchmarking with INE sources to validate internal data against real market figures
- Interactive Plotly charts in HTML ready to embed in presentations or web pages

---

## 👥 Team — Team 10

| Role | Area |
|---|---|
| **Customer Experience Analyst + Data Steward** ⬅️ *my role* | Satisfaction, ratings and reviews · Centralised ETL and dataset preparation for all departments |
| Marketing and Communications Analyst | Segmentation, positioning, trends |
| Customer Profile Analyst | Behaviour, ratings, typology |
| Operations Analyst | Inventory management, capacity, efficiency |
| Finance and Risk Analyst | Variations, economic KPIs |
| Repository Quality Manager *(rotating role)* | Review, merge, code standards |
| **Mentor / Department Director** | Technical facilitation and guidance |

### 🔧 My specific contribution

In addition to my customer experience analysis responsibilities, I took on the transversal role of **Data Steward** for the team. The original dataset contained a large number of columns and variables, and each sprint the different departments required different subsets. I coordinated this at the start of each sprint: identifying which variables each area needed, executing the cleaning and selection, and delivering optimised, analysis-ready datasets. This prevented every analyst from loading and processing the full dataset redundantly, reducing processing time and ensuring consistency in the starting data across the entire team.

---

*Project developed at IT Academy · Barcelona Activa · Business Simulator · 2025*
