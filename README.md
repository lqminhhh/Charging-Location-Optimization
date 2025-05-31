# ⚡ Optimized Strategy for Electric Vehicle Charging Station Allocation

Authors: Minh Le & Yen Nguyen
Courses: DA353 - Advanced Prescriptive Methods | Denison University
---
## 🔍 Overview
With the surge in electric vehicle (EV) adoption, optimal placement of charging stations has become critical. This project aims to strategically allocate EV charging stations in the Seattle metropolitan area to cover the largest number of vehicles while minimizing the number of stations needed.

## 🗂 Project & Structure
```
├── data/
│   ├── electric_stations.csv            # Location data of existing stations
│   └── Electric_Vehicle_Population.csv  # Registered EVs in WA State
├── data_collection.ipynb                # API data collection and preprocessing
├── data_modeling.ipynb                  # Optimization model implementation
├── Final_Presentation.pdf               # Summary presentation
├── Final_Report.pdf                     # Detailed project report
└── README.md                            # This file
```

## 🛠 Methodology
1. Data Preprocessing

- Filtered EV data to Seattle area; cleaned missing and invalid entries.

- Collected current station data using energy.gov API.

2. Model Formulation

- Built a linear optimization model in Python with Gurobi.

- Objective: minimize the number of stations while ensuring maximum vehicle coverage.

3. Model Solving & Validation

- Conducted sensitivity analysis (e.g., max driving distance, shadow price).

- Compared optimized locations with actual station map for accuracy.

## 🔁 Reproducibility
- Install dependencies listed in the notebooks.

- Run `data_collection.ipynb` to gather & clean data.

- Execute `data_modeling.ipynb` to build and solve the optimization model.

## 📈 Key Findings
- The model covers ~75.5% of total EVs using a reduced number of strategically placed stations.

- Coverage includes users with limited home-charging access.

- Majority of high-demand zones align with current real-world station clusters.

## Reference
- https://catalog.data.gov/dataset/electric-vehicle-population-data
- https://afdc.energy.gov/fuels/electricity-locations#/find/nearest?fuel=ELEC
- https://www.kingcountymetrozefleet.com/?lng=en
- [https://kingcounty.gov/en/legacy/depts/finance-business-operations/procurement/for-government/environmental-purchasing_guide/vehicles](https://kingcounty.gov/en/legacy/depts/finance-business-operations/procurement/for-government/environmental-purchasing/purchasing_guide/vehicles)

## 📬 Contact
- Minh Le – le_m2@denison.edu

- Yen Nguyen – Contact info available on request