# Solar for African SMEs: Financial Impact

**Does off-grid solar pay for itself for small businesses in Africa, and how fast?**

A Power BI capstone project that compares the cost, yearly savings, return on investment and payback period of four off-grid solar systems used by small and medium businesses in 49 African countries.

- 📊 [Power BI file](powerbi/Financial_Impact_Dashboard.pbix) (downloads when clicked, opens in Power BI Desktop)
- 🗂️ [Dataset (CSV)](data/expanded_solar_financial_impact.csv), which GitHub previews as a table

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

| System | Business type | Price | Yearly savings | ROI | Payback |
|---|---|---|---|---|---|
| Solar Water Pump | Agriculture | $1,261 | $472 | 37.4% | 2.7 yrs |
| Small SHS (3–49 Wp) | Food Retail | $194 | $68 | 35.1% | 2.9 yrs |
| Larger SHS (50 Wp+) | Small Manufacturing | $572 | $187 | 32.7% | 3.1 yrs |
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

## Data

The dataset has 196 rows: 49 countries × 4 system types. Each row is one country and one business type.

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

---

## Repository structure

```
solar-sme-financial-impact/
├── README.md
├── LICENSE
├── data/
│   ├── expanded_solar_financial_impact.csv   Full 196-row dataset
│   └── solar_financial_impact.xlsx           Source workbook
└── powerbi/
    └── Financial_Impact_Dashboard.pbix       The Power BI report
```

## Run it locally

1. Clone or download this repository.
2. Open `powerbi/Financial_Impact_Dashboard.pbix` in Power BI Desktop (free from Microsoft).
3. If Power BI asks for the data location, point it to the `data/` folder.

---

## Limitations

- **Each business type uses one system.** Agriculture always uses a water pump, food retail always a small home system, and so on. Business type and system type can't be compared separately.
- **System prices are the same in every country.** Only the savings change by country, so the regional differences come from savings alone. Real prices vary with import duties and local suppliers.
- **No financing costs.** ROI and payback ignore loan interest, maintenance and battery replacement, so real payback will be longer.

---

## Tech stack

| Layer | Tool |
|---|---|
| Data preparation | Excel, Power Query |
| Modelling and measures | Power BI, DAX |
| Visualisation | Power BI Desktop |

---

## License

Released under the MIT License. See [LICENSE](LICENSE).

---

**Built by Bih Brandy Sango** · Data Scientist and BI Analyst
