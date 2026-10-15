# Life-cycle carbon footprint of wastewater treatment alternatives — open rebuild

**Status:** work in progress (started October 2026)
**Author:** Aya Ismail — environmental engineer, M.Sc. Water Resources & Environmental Management (Leibniz Universität Hannover)

## What this project is

An open, reproducible rebuild of a comparison I first carried out as a consultant in 2021: the carbon footprint of competing treatment alternatives for the upgrade of a large wastewater treatment plant in Cairo (Helwan: 550,000 → 800,000 m³/day, advanced treatment), covering **construction plus 20 years of operation**. The original assessment was prepared for the project's environmental and social impact assessment financed by the European Investment Bank (EIB register 142869432).

The original was built in spreadsheets with IPCC emission factors. This repository rebuilds the method in open LCA tools so that every assumption, emission factor and sensitivity is transparent and can be re-run.

## Method (following ISO 14040/44 principles)

- **Functional unit:** treatment of 1 m³ of municipal wastewater to the required effluent standard, and the plant total over 20 years.
- **System boundary:** construction materials (concrete, steel), electricity for operation, process chemicals, direct process emissions (N₂O from nitrogen removal, CH₄ from sludge handling), sludge treatment and disposal, biogas recovery credits.
- **Impact method:** global warming potential (kg CO₂-eq, IPCC AR6 GWP100).
- **Sensitivity:** grid carbon intensity, N₂O emission factor, biogas utilisation rate.

## Tools

- openLCA (desktop LCA software)
- Python with Brightway (scripted LCA, Monte-Carlo uncertainty)
- AI-assisted scripting (ChatGPT/Claude/Copilot) with every factor checked against IPCC/ISO sources

## Data

Only public or illustrative data are used here. Client data from the original consultancy are **not** included. Sources for every factor are listed in `data/sources.md`.

## Repository structure

```
data/          inventory template and data sources
notebooks/     Brightway analysis notebooks (in progress)
openlca/       openLCA model export (in progress)
results/       figures and tables (in progress)
```

## Roadmap

- [x] Project description and method (October 2026)
- [ ] Inventory filled with public/illustrative data
- [ ] openLCA model of two alternatives
- [ ] Brightway notebook with sensitivity and Monte-Carlo analysis
- [ ] Short write-up of results

## Related work

- M.Sc. thesis (2018), ISAH Leibniz Universität Hannover: *Model-based comparison of nitrogen-removal strategies for WWTPs in countries with high temperatures — energy demand and CO₂ footprint* (SIMBA#).

Contact: aya.ashraf.ismael@gmail.com · linkedin.com/in/aya-ismail-env
