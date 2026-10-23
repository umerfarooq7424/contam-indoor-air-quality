# Indoor Air Quality from Cooking — CONTAM Ventilation Scenarios

> What does a 30-minute cooking session do to the air inside a home — and how much do the stove type and ventilation matter? Multizone simulations in **NIST CONTAM** of a real residential property (the Mravlag property), tracking CO₂, NO₂, ozone, PM2.5, and VOCs zone by zone.

## Headline results (30-minute cooking session, kitchen zone)

| Scenario | PM2.5 | NO₂ |
|---|---|---|
| **Gas stove**, windows closed, no range hood | **2,000–3,500 µg/m³** | **5.5–9.5 ppm** |
| **Electric stove**, windows closed, no range hood | 50–60% lower than gas | Not detectable |
| **Electric stove**, windows open + range hood on | **Below 100 µg/m³** | Eliminated |
| **Gas stove**, windows open + range hood on | Falls toward outdoor ambient levels | Falls toward outdoor ambient levels |

Unventilated gas cooking pushes PM2.5 and NO₂ far beyond safe indoor standards — a serious respiratory and cardiovascular risk for senior citizens and other sensitive occupants. Ventilation and electrification each cut exposure sharply; together they bring the kitchen close to outdoor air quality. Scenarios were also run against a **good outdoor-air day (26 Jun)** and a **bad outdoor-air day (4 Jul)** to separate indoor sources from outdoor infiltration.

## What's here

- `model/` — the CONTAM project (`CONTAM-Intro.prj`) with its contaminant-source, species, and filter libraries and schedules — open it in CONTAM and re-run the scenarios
- `outputs/` — hourly zone-level simulation output (kitchen ×2 runs, bedroom) with CO₂ [ppm], NO₂, ozone, PM2.5, VOC [kg/kg]
- `reports/` — the scenario write-up (`Working_on_the_Contam_Scenarios.docx`) and the chart reports plotting PM2.5 and NO₂ by stove, ventilation state, and outdoor-air day
- `data/Graphs.xlsx` — chart source data (June/July runs)

## Method

Multizone airflow and contaminant transport simulation in **NIST CONTAM**: the property is modelled as connected zones (kitchen, bedroom, …) with defined leakage paths, contaminant sources (stove emissions), schedules, and outdoor boundary conditions, then run across the scenario matrix above. Full scenario logic is in the write-up in `reports/`.

## Reference

Gould, Carlos F., et al. "Air Pollution Exposure When Cooking with Electricity Compared to Gas." *medRxiv*, Cold Spring Harbor Laboratory Press, 2023. https://www.medrxiv.org/content/10.1101/2023.04.10.23288249v1.full

## Author

**Umer Farooq** — Economic & Climate Risk Analyst · [LinkedIn](https://www.linkedin.com/in/umer-farooq-gojra/) · [GitHub](https://github.com/umerfarooq7424)

## License

MIT — see LICENSE. CONTAM is a product of the U.S. National Institute of Standards and Technology (NIST); this repository contains my project files and results, not the CONTAM software.
