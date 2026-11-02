# NYC Yellow Taxi Operations Analysis

An exploratory analytics project using **2023 NYC Yellow Taxi trip records** to understand demand patterns, trip economics, geographic activity, and operational opportunities. The analysis combines data preparation, exploratory analysis, and geospatial visualization to develop recommendations for taxi operations.

## Project objectives

- Identify demand patterns across hours, weekdays, months, and pickup/drop-off zones.
- Examine fares, tips, trip distance, passenger counts, payment types, and vendor patterns.
- Explore pickup and drop-off hotspots and zone imbalances.
- Investigate route-speed and time-of-day patterns.
- Translate the analysis into operational recommendations for dispatching and fleet positioning.

## Data

**Source:** [NYC Taxi & Limousine Commission — Trip Record Data](https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page)

The notebook uses monthly Yellow Taxi CSV records from **2023** and samples the data to keep the analysis computationally manageable. It also uses NYC taxi-zone geographic reference data for spatial analysis.

The raw trip CSVs and zone shapefile are not included in this repository. Download the relevant 2023 Yellow Taxi files and the matching Taxi Zone lookup/shapefile from the TLC source, then update the notebook paths before execution.

Relevant fields include pickup and drop-off timestamps, trip distance, fare components, tips, passenger count, payment type, vendor, and pickup/drop-off zone identifiers.

## Methodology

### 1. Data preparation

- Load multiple monthly CSV files.
- Apply a fixed sampling approach and random seed to manage data volume.
- Combine the sampled monthly records.
- Parse timestamp columns and standardize column names and data types.

### 2. Data cleaning

- Reconcile duplicate or split fare fields, including airport fees.
- Handle missing values using domain-informed rules.
- Remove invalid records such as negative fares, distances, or tips.
- Review outliers and inconsistent trip records.

### 3. Exploratory analysis

- Hourly, weekday, monthly, and quarterly demand patterns.
- Fare, distance, trip duration, and tip relationships.
- Passenger-count, payment-type, and vendor comparisons.
- Revenue contribution and night-time activity.

### 4. Geospatial analysis

- Join trip zone identifiers to NYC Taxi Zone reference data.
- Map pickup and drop-off volumes.
- Identify high-activity zones and pickup/drop-off imbalances.
- Compare route and time-of-day patterns using average speed.

## Findings recorded in the analysis

- Demand varies across both the day and the week, with elevated activity around commute periods.
- Activity is concentrated in a subset of pickup and drop-off zones.
- Payment type, fare, distance, and vendor patterns provide additional context for operational analysis.
- Differences between pickup-heavy and drop-off-heavy zones suggest opportunities for fleet rebalancing.
- Night-time activity and airport/transit-related demand are useful dimensions for operational planning.

These observations are descriptive findings from the sampled 2023 records; they should not be interpreted as causal or as citywide estimates without checking the sampling design and representativeness.

## Business recommendations

- Position more vehicles near consistently high-demand zones and during observed peak periods.
- Rebalance vehicles from drop-off-heavy areas toward zones with persistent pickup demand.
- Review slow routes and trip-time patterns when designing dispatch strategies.
- Plan night-time coverage around observed demand hubs.
- Evaluate fare-per-mile and trip-duration patterns before making pricing changes.

## Tools and technologies

| Area | Tools |
|---|---|
| Data manipulation | Python, pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| Spatial analysis | GeoPandas |
| Workflow | Jupyter Notebook |

## Repository contents

```text
.
├── EDA_Assg_NYC_Taxi_piyush_sharma.ipynb
├── Report_NYC_Taxi_Operations_piyush_sharma.pdf
└── README.md
```

- [Open the analysis notebook](./EDA_Assg_NYC_Taxi_piyush_sharma.ipynb)
- [Open the project report](./Report_NYC_Taxi_Operations_piyush_sharma.pdf)

## How to run

Clone the repository:

```bash
git clone https://github.com/piyush0920/nycTaxiAssignment.git
cd nycTaxiAssignment
```

Install the main dependencies:

```bash
pip install pandas numpy matplotlib seaborn geopandas jupyter
```

Download the 2023 TLC Yellow Taxi CSV files and the matching taxi-zone geographic reference files. Update the input paths in the notebook, then run the cells in order.

## Limitations and next steps

- Results depend on the chosen sampling fraction and random seed.
- The raw CSV files and geospatial reference files are external inputs and are not committed.
- The analysis is descriptive; a predictive demand model or dispatch simulation would be a separate extension.
- Zone-level comparisons should account for sample coverage and the geographic context of each zone.

## Author

**Piyush Sharma**  
[GitHub](https://github.com/piyush0920) · [Portfolio](https://piyush0920.github.io/) · [LinkedIn](https://linkedin.com/in/piyush-sharma-6591171ba)
