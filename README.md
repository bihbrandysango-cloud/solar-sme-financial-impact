<div align="center">

# Solar for African SMEs

**Does off-grid solar pay for itself for small businesses in Africa, and how fast?**

[**▶ Watch every page (51 seconds)**](https://bihbrandysango-cloud.github.io/projects/solar/) · [**📄 Pitch deck (PDF)**](docs/Solar-Pitch-Deck.pdf)

</div>

[![Solar for African SMEs Overview page](docs/screenshots/power-bi/01-overview.jpg)](https://bihbrandysango-cloud.github.io/projects/solar/)

**Capstone project, Women Techsters Fellowship 2026 (Tech4Dev), Data Science and Engineering track.**

A five-page Power BI report that compares the cost, yearly savings, return and payback of four off-grid solar systems used by small and medium businesses in 49 African countries.

- 📊 [Power BI project](powerbi/) (open `Solar for African SMEs.pbip` in Power BI Desktop)
- 🗂️ [Dataset (CSV)](data/expanded_solar_financial_impact.csv), which GitHub previews as a table
- 📄 [Pitch deck (PDF)](docs/Solar-Pitch-Deck.pdf) · [PowerPoint](docs/Solar-Pitch-Deck.pptx)

---

## What is in the report

| Page | What it shows |
|---|---|
| Overview | Return, payback and savings, how long payback takes by region, and the Water Pump against Refrigeration gap in the 12 highest-return countries |
| Systems | Four clickable system cards, how savings add up to each price, the range of return and savings in every country |
| Countries | A clickable honeycomb map of 49 countries, highest and lowest returns, and the selected country's four systems |
| Regions | Return by region and system, stacked savings and every country as a dot |
| Simulator | Pick a subsidy and a change in savings to see payback, return and the subsidy each system needs for a two-year payback |

Each page has a dotted globe of Africa as its background, coloured from the data. A region filter carries across pages. Built with Power BI, DAX (58 measures), Power Query and Deneb.

---

## Headline findings

| Metric | Value | Note |
|---|---|---|
| Average return on investment | **34%** per year | Range 22.8% to 47.2% |
| Average payback period | **3.0 years** | Fastest 2.1 years, slowest 4.4 years |
| Average system price | **$742** | From $194 for a small home system to $1,261 for a water pump |
| Average yearly savings | **$254** per business | From $47 to $595 |
| Cases rated High or Very High benefit | **187 of 196** | 95% of all country and business combinations |

---

## The question

Diesel generators and unreliable grid power are a large running cost for small businesses across Africa. Solar systems cost more up front, so an owner needs to know two things before buying: how much the system saves each year, and how many years it takes to earn back its price.

This project answers that for four business types, four regions and 49 countries.

---

## Key insights

1. **The most expensive system pays back fastest.** Solar water pumps for agriculture cost the most ($1,261) but save $472 a year, which gives the best ROI (37.4%) and the shortest payback (2.7 years). Price alone is a poor guide to value.

2. **Small home systems are the cheapest way in.** At $194, a 3–49 Wp system for food retail returns 35.1% and pays back in 2.9 years. For a business with little cash, it is the lowest-risk start.

3. **Solar refrigeration has the weakest case, and it still pays.** Cold storage systems return 30.7% and pay back in 3.3 years. That is the slowest of the four, and it still earns back its price in under four years.

4. **West Africa gets the best returns.** West Africa averages 35.5% ROI and a 2.8-year payback. Southern Africa is lowest at 31.0% and 3.3 years.

5. **Only 9 of 196 cases are "Moderate".** Those average a 4.2-year payback. Every other case is High or Very High.

6. **A partial subsidy goes a long way.** A 20% subsidy cuts the average payback from 3.0 to 2.4 years, at about $148 per system. A water pump needs about 25% to pay back in two years; refrigeration needs about 39%.

| System | Business type | Price | Yearly savings | ROI | Payback |
|---|---|---|---|---|---|
| Solar Water Pump | Agriculture | $1,261 | $472 | 37.4% | 2.7 yrs |
| Small SHS (3–49 Wp) | Food Retail | $194 | $68 | 35.1% | 2.9 yrs |
| Larger SHS (50 Wp+) | Small Manufacturing | $572 | $187 | 32.6% | 3.1 yrs |
| Solar Refrigeration | Cold Storage | $941 | $289 | 30.7% | 3.3 yrs |

---

## Recommendations

| Priority | Action | Expected impact |
|---|---|---|
| High | Lead lending and grant programmes with solar water pumps for farms | Highest savings per business and the fastest payback |
| High | Offer small home systems to cash-poor retailers on pay-as-you-go terms | Low entry price, 2.9-year payback |
| Medium | Pair solar refrigeration with longer loan terms | Its 3.3-year payback is the slowest of the four |
| Medium | Study why Southern Africa returns less | 4.5 points of ROI behind West Africa |

---

## Pages

### 1. Overview

![Overview](docs/screenshots/power-bi/01-overview.jpg)

### 2. Systems

![Systems](docs/screenshots/power-bi/02-systems.jpg)

### 3. Countries

![Countries](docs/screenshots/power-bi/03-countries.jpg)

### 4. Regions

![Regions](docs/screenshots/power-bi/04-regions.jpg)

### 5. Simulator

![Simulator](docs/screenshots/power-bi/05-simulator.jpg)

---

## Data

**Where the data comes from.** The dataset combines public benchmark data with a transparent return model. I compiled it in February 2026 with the help of Manus, an AI research agent, in two steps.

1. **Benchmarks.** Price, savings, return and payback figures for four systems in Nigeria, Kenya, Rwanda and South Africa, plus three sub-Saharan averages, drawn from public energy-access, solar-cost, productive-use and tariff reports (see [Sources](#sources)). They are in the `Benchmark_Data` sheet of [`solar_financial_impact.xlsx`](data/solar_financial_impact.xlsx).
2. **Modelled estimates for 49 countries.** The benchmarks were extended to every country with a simple model: yearly savings come from the energy a system replaces and local power costs, payback is price ÷ yearly savings, and return is yearly savings ÷ price.

None of the source organisations published a 49-country table of SME returns. They supplied the cost, appliance, tariff and market inputs. **Every row in the final dataset is a modelled estimate**, including the four benchmark countries, whose values were adjusted during modelling.

System prices are the same in every country. Savings vary by country, so return and payback do too.

The final dataset has 196 rows: 49 countries × 4 system types. Each row is one country and one business type.

| Column | Description |
|---|---|
| `Country` | One of 49 African countries |
| `Region` | West, East, Central or Southern Africa |
| `SME_Type` | Agriculture, Food Retail, Small Manufacturing or Cold Storage |
| `System_Type` | The solar system used by that business type |
| `Avg_System_Price_USD` | Average purchase price of the system |
| `Annual_Savings_USD` | Average yearly saving against the business's previous energy cost |
| `ROI_Percent` | Yearly savings as a percentage of the system price |
| `Payback_Period_Years` | System price divided by yearly savings |
| `Financial_Benefit_Level` | Moderate, High or Very High |

The Power BI model adds three small lookup files built from the dataset: `geography.csv` (region, short name and map position for each country), `systems.csv` (short name and business type for each system) and `levels.csv` (benefit level order).

---

## Method

1. **Load and check.** Power Query reads the CSV and sets a type for each column. All 196 rows load with no missing values, so no rows were dropped or filled in.
2. **Model.** One fact table (`SolarCases`, one row per country and system) joins three small lookup tables: `Geography`, `Systems` and `Levels`. This star schema lets one region filter work across every page.
3. **Return and payback.** Return is yearly savings divided by system price, times 100. Payback is system price divided by yearly savings. I checked the dataset's own `ROI_Percent` and `Payback_Period_Years` columns against these formulas, and every row matches to within 0.01.
4. **Averages.** Each country and system pair counts once, so the averages are simple means across cases. They are not weighted by how many businesses use each system.
5. **Benefit levels.** In the data, Moderate means a return below 25%, High means 25% to 35%, and Very High means 35% or more.
6. **Simulator.** For a subsidy *s* and a change in savings *c*, payback for each case is price × (1 − *s*) ÷ (savings × (1 + *c*)), averaged across cases. The subsidy a system needs for a two-year payback is 1 − 2 × savings × (1 + *c*) ÷ price.

All 58 measures are in [`_Measures.tmdl`](powerbi/Solar%20for%20African%20SMEs.SemanticModel/definition/tables/_Measures.tmdl), so the numbers can be checked or reproduced.

---

## Repository structure

```
solar-sme-financial-impact/
├── README.md
├── LICENSE
├── data/
│   ├── expanded_solar_financial_impact.csv   Full 196-row dataset
│   ├── geography.csv, systems.csv, levels.csv   Lookup tables for the model
│   └── solar_financial_impact.xlsx           Source workbook
├── docs/
│   ├── Solar-Pitch-Deck.pdf                  Pitch deck, renders inline on GitHub
│   ├── Solar-Pitch-Deck.pptx                 Editable PowerPoint
│   └── screenshots/power-bi/                 One picture per page
└── powerbi/
    ├── Solar for African SMEs.pbip            The Power BI project (current report)
    ├── Solar for African SMEs.Report/
    ├── Solar for African SMEs.SemanticModel/
    └── Financial_Impact_Dashboard.pbix       First version of the report
```

## Run it locally

1. Clone or download this repository.
2. Open `powerbi/Solar for African SMEs.pbip` in Power BI Desktop (free from Microsoft). Power BI Desktop loads the Deneb visual from AppSource the first time you open it.
3. The saved data opens straight away. To refresh it, set the `DataFolder` parameter (Transform data › Edit parameters) to this repository's `data\` folder, ending with a backslash.

The first version of the report is kept as `powerbi/Financial_Impact_Dashboard.pbix`.

---

## Limitations

- **Each business type uses one system.** Agriculture always uses a water pump, food retail always a small home system, and so on. Business type and system type can't be compared separately.
- **System prices are the same in every country.** Only the savings change by country, so the regional differences come from savings alone. Real prices vary with import duties and local suppliers.
- **No financing costs.** ROI and payback ignore loan interest, maintenance and battery replacement, so real payback will be longer.
- **Unweighted averages.** Every country counts the same, whether it has many small businesses or few, so the averages describe the cases rather than the whole market.
- **All rows are modelled estimates.** Country and regional rankings, such as West Africa leading, show what the model implies, not measured results. The figures should be read as scenarios.
- **Tariff inputs may be dated.** One tariff source, the World Bank's brief on nonresidential tariffs, uses schedules from July 2014. Current national regulator tariffs would make the savings more accurate.
- **One point in time.** The data has no dates, so it can't show how prices or savings change over the years.

---

## Sources

Reports that supplied the benchmark inputs and context. None of them publishes the dataset's row-level figures directly.

| # | Source | What it supports |
|---|---|---|
| 1 | World Bank / GOGLA, [Off-Grid Solar Market Trends Report 2024](https://documents1.worldbank.org/curated/en/099090225151516968/pdf/P507761-4ff9bd3f-07b5-4717-bf77-63494281e461.pdf) | Productive-use appliance sales and prices, including water pumps and cold storage |
| 2 | IRENA, [Renewable Power Generation Costs in 2023](https://www.irena.org/-/media/Files/IRENA/Agency/Publication/2024/Sep/IRENA_Renewable_power_generation_costs_in_2023.pdf) | Solar installed-cost and cost-trend benchmarks |
| 3 | Efficiency for Access / CLASP, [The State of the Off-Grid Appliance Market](https://efficiencyforaccess.org/wp-content/uploads/Clasp-SOGAM-Report-final.pdf) | Off-grid refrigerator and productive-use evidence |
| 4 | Efficiency for Access, [Exploring the Holistic Impact of Clean Energy-Powered Cold Chain](https://efficiencyforaccess.org/updates/exploring-the-holistic-impact-of-clean-energy-powered-cold-chain/) | The business case for cold storage |
| 5 | World Bank, [Electricity Tariffs for Nonresidential Customers in Sub-Saharan Africa](https://documents1.worldbank.org/curated/en/489411494351752887/pdf/114848-BRI-PUBLIC-LWLJfinalOKR.pdf) | Commercial tariffs in 38 countries (2014 schedules) |
| 6 | IFC, [Climate Investment Opportunities in Emerging Markets](https://www.ifc.org/content/dam/ifc/doc/mgrt/3503-ifc-climate-investment-opportunity-report-dec-final.pdf) | Investment context for Kenya, Nigeria and South Africa |
| 7 | AfDB, [Electricity Regulatory Index for Africa 2022](https://africa-energy-portal.org/sites/default/files/2023-02/ERI%202022_AFDB%20EN.pdf) | Tariff-setting and regulatory context |

Current tariffs for a future version: [NERC](https://nerc.gov.ng/media/multi-year-tariff-order-myto-2024/) (Nigeria), [EPRA](https://www.epra.go.ke/electricity-tariff-registers) (Kenya), [RURA](https://www.rura.rw/publications/tariffs) (Rwanda) and [NERSA](https://www.nersa.org.za/electricity/pricing) (South Africa).

### Further reading

- GOGLA, [Global Off-Grid Solar Market Report 2026](https://gogla.org/wp-content/uploads/2026/06/GOGLA_Global-Off-Grid-Solar-Market-Report_2026_DEF3.pdf)
- Lighting Global (World Bank), [The Market Opportunity for Productive Use Leveraging Solar Energy (PULSE) in Sub-Saharan Africa](https://www.lightingglobal.org/wp-content/uploads/2019/09/PULSE-Report.pdf), 2019
- Efficiency for Access, [Solar Water Pump Outlook 2019](https://efficiencyforaccess.org/publications/solar-water-pump-outlook-2019-global-trends-and-market-opportunities/)

---

## Tech stack

| Layer | Tool |
|---|---|
| Data preparation | Excel, Power Query |
| Modelling and measures | Power BI, DAX (58 measures) |
| Visualisation | Power BI Desktop, Deneb (Vega-Lite) |

---

## License

Released under the MIT License. See [LICENSE](LICENSE).

---

**Built by Bih Brandy Sango** · Data Scientist and BI Analyst
