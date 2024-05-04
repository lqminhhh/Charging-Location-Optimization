# Optimized Strategy for Electric Vehicle Charging Station Allocation
---
## 1. Background and Introduction
The adoption of electric vehicles (EVs) is increasing worldwide, mainly driven by growing awareness of environmental issues and technological advancements. These types of vehicles are now favored and recognized by the majority of consumers. With the increasing number of new energy electric vehicles, the demand for charging stations for these vehicles is also increasing. This makes the strategic placement of charging stations crucial, helping the government optimize infrastructure efficiency by minimizing the need for excessive stations. Finding the right locations for these stations is therefore important, ensuring they can provide convenient access for all EV users, while contributing to a more sustainable future of transportation.
For this project, we aim to optimize the allocation of electric vehicles charging stations locations that effectively minimize the number of stations. 

## 2. Dataset
Our primary dataset comprises registered Battery Electric Vehicles (BEVs) and Plug-in Hybrid Electric Vehicles (PHEVs) from the Washington State Department of Licensing (DOL) via data.gov and is intended for public access and use. This dataset provides valuable insights into vehicle distribution and usage patterns, crucial for optimizing charging station locations. The data contains **17 columns and 177,867 rows**. However, we plan to only use the following columns:
- *County*: Geographic region of a state that a vehicle's owner is listed to reside within
- *City*: City in which the registered owner resides.
- *Postal*: The 5 digit zip code in which the registered owner resides.
- *Electric Range*: Describes how far a vehicle can travel purely on its electric charge.
- *Vehicle Location*: The center of the ZIP Code for the registered vehicle.

In addition, we aim to gather data via energy.gov on the current locations of the charging stations in the area for model evaluation and improvement. We plan to get the data by requesting the API url with our own developer API key and the queried parameters related to electric vehicle stations. The following columns will be used for further analysis:
- *City*: City in which the station is placed
- *State*: State in which the station is placed
- *Latitude*: The latitude of the station
- *Longitude*: The longitude of the station

## 3. Methodology
1. Data Preprocessing: 
- Refine the dataset obtained from the Washington State Department of Licensing to extract necessary columns and focus on the Seattle metropolitan area.
- Clean the data to remove any inconsistencies or outliers that may affect the accuracy of the optimization model.
2. Model Formulation: 
- Formulate a linear optimization model to determine the optimal allocation of electric vehicle charging stations within the Seattle metropolitan area.
- Define decision variables, objective function, and constraints of the problem. Later, we will write a mathematical formulation to represent this model. 
3. Model Implementation: 
- Utilize the Gurobi optimization library and Python to implement the formulated optimization model.
- Develop efficient algorithms and scripts to solve the linear optimization problem and obtain the optimal solution for charging station locations.
4. Sensitivity Analysis: 
- Conduct sensitivity analysis to assess the robustness of the optimization model by using shadow prices and reduced costs.
- Evaluate the model's performance and stability by examining its response to changes in key parameters, such as the threshold for maximum driving distance 
5. Validation: 
- Assess the accuracy and effectiveness of the optimized charging station locations by comparing the model results obtained from the optimization process with real-world charging station locations.

## 4. Assumptions
To streamline our project, we make two key assumptions. Firstly, we assume uniform power consumption demand for each vehicle, approximating it based on the average power consumption of electric cars. Secondly, we consider the construction cost as well as the power capacity of a new station to be consistent across all locations and irrespective of demand variations.

## 5. Result
[Final Report](https://github.com/lqminhhh/Charging-Location-Optimization/blob/main/DA353_Final_Report.pdf)
## 6. Reference
Washington State Department of Licensing - Electric Vehicle Population Data. Retrieved
from: https://catalog.data.gov/dataset/electric-vehicle-population-data

Alternative Fuels Data Center (AFDC) - Electric Vehicle Charging Station Locator.
Retrieved from:
https://afdc.energy.gov/fuels/electricity-locations#/find/nearest?fuel=ELEC
