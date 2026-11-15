# Group 3 Final Project 5310

**Data 5310 Final Project, Seattle University **
Team: Njenga, Naomi, Prithika, Devlin

## Research question: 

Do countries with higher EV adoption have lower transport emissions, and does the cleanliness of their electricity matter? 

## Countries and years:

This project covers 10 countries ranging from 2010 to 2025. We hand-picked them to get a mix of different regions and their range of EV adoption levels

The 10 countries are: Norway, China, United States, Germany, United Kingdom, Brazil, Thailand, Japan, India, and South Africa

## Data

All four datasets came from [Our World in Data]. Each team member cleaned one dataset, and then they were merged into 'Ev_clean_energy_analysis.ipynb'

| Dataset | Column(s) | Unit | Years | File |
|---|---|---|---|---|
| Share of new cars sold that are electric | `ev_share` | % of new car sales | 2010–2025 | `ev_share_clean.csv` |
| CO₂ emissions from transport per capita | `transport_co2` | kg per person | 2010–2023 | `Emission_transport_cleaned.csv` |
| Fossil fuel consumption per capita | `gas_kwh`, `oil_kwh`, `coal_kwh`, `total_kwh`, `gas_share`, `oil_share`, `coal_share` | kWh per person; share of total | 2010–2025 | `fossil_fuel_data_cleaned.csv` |
| Share of electricity from renewables | `renewable_share` | % of electricity | 2010–2025 | `renewables_cleaned_1.csv` |


## Merged dataset

The four datasets were joined using 'Entity', 'Code', and 'Year'. Then they were limited to 20210-2025 year range. This resulted in about 160 rows and 13 columns.

Some values are missing; we are aware of them: 
- 'Transport_CO2' stops at 2023, so 2024-2025 will be empty (about 20 rows)
- 'Ev share' for South Africa starts in 2013, so 2010-2012 was empty (about 3 rows)

## Repository content
```
ev_clean_energy_analysis.ipynb     # loads, cleans and merges the four datasets
ev_share_clean.csv                 # EV share of new car sales
Emission_transport_cleaned.csv     # transport CO2 per capita
fossil_fuel_data_cleaned.csv       # fossil fuel consumption per capita
renewables_cleaned_1.csv           # renewable share of electricity
README.md
```

## How to run

1. Install Python 3 with `pandas` (and `altair` for the visualizations).
2. Put the four CSV files in the same folder as the notebook.
3. Open `ev_clean_energy_analysis.ipynb` and run all cells.

## Sources

Our World in Data, with data from the International Energy Agency (EV sales), Climate Watch (transport emissions), the Energy Institute *Statistical Review of World Energy* and the U.S. EIA (fossil fuels), and Ember and the Energy Institute (renewable electricity). See each chart's page on Our World in Data for full citations.
