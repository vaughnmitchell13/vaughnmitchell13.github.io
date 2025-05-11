---
title: Subway Ridership and NYC's Traffic Congestion Zone
layout: default
---

📁 [Original Repo](https://github.com/vaughnmitchell13/econ308-proj)\
📝 [Final Paper](https://github.com/vaughnmitchell13/vaughnmitchell13.github.io/raw/main/DID-ECON308/ECON308-Final%20Paper.pdf)\
🗣 [Final Presentation](https://github.com/vaughnmitchell13/vaughnmitchell13.github.io/raw/main/DID-ECON308/DID_Congestion_Relief_Zone.pdf)

## 💡 **Abstract**
On January 5th, 2025, New York City implemented a Congestion Relief Zone that tolls drivers
entering Manhattan south of 60th Street. The policy decision was intended to reduce traffic and
offer new revenue streams for the MTA to improve subways; as of FQ2025, the policy has
brought in nearly $160 million in revenue. While the status of the policy — in just three
months — seems precarious with the Trump administration calling the tolls illegal, there are
already valuable implications about the effects of this policy, namely on subway ridership. This
research project explores the change in subway ridership for stations inside and outside the zone,
before and after congestion pricing went into effect. Accordingly, we chose a difference-indifferences design to analyze subway ridership across stations in Manhattan. The State of New
York offers data on MTA subway ridership in both 2024 and 2025, all of which was cleaned into
a daily, by-station panel structure. Our first model utilizes simple OLS with both dummy
variables (time and treatment) as well as the interaction term; our second model clusters the
stations by standard error; and our third model, arguably the most improved and actionable,
controls for time-invariant characteristics like holidays or construction as well as station invariant characteristics like location and inherent busyness. Our fixed-effects model — the
strongest of the three — predicts an increase in 641 daily riders for stations inside
the congestion zone compared to stations outside the zone.

## 👾 **Data**
  - https://mega.nz/folder/S8o3iDQY#LB5H6vnRPKadVrwmf51e6g includes CSV files from the sources below.
  - [Source for 2025](https://catalog.data.gov/dataset/mta-subway-hourly-ridership-beginning-2025)
  - [Source for 2024](https://data.ny.gov/Transportation/MTA-Subway-Hourly-Ridership-2020-2024/wujg-7c2s/about_data)
  - Note: This is *raw* data, and it includes information about the station (ID and conventional name), transit date and time, lat/long coordinates, and ridership and transfer numbers. These datasets were used in [Data-Preprocessing.ipynb](./Data-Preprocessing.ipynb), which documents how this data was managed and prepared for further cleaning.
  - The CSV files containing "_w_dummy" were created in ArcGIS Pro in order to attribute whether or not the station was inside the congestion zone. Further steps are provided below.
 
## 🗺️ **ArcGIS Pro Documentation**
  - An [NYC roads layer](./data/tl_2023_36061_roads.shp) from [census.gov's](https://catalog.data.gov/dataset/tiger-line-shapefile-2023-state-new-york-primary-and-secondary-roads) TIGER/Line collection was loaded to set context of NYC and serve as a foundation for the map.
  - The projection for this data was NAD83(2011) / New York Long Island (ft).
  - Both `Manhattan_Subway_Ridership_2024.csv` and `Manhattan_Subway_Ridership_2025.csv` were loaded into ArcGIS Pro using the `XY Table to Point` tool.
  - A new layer called `Traffic Congestion Zone` was drawn to reflect Manhattan's current congestion relief area.
  - A new field called `inside_zone` was added to both attribute tables, using the `Select by Location` tool to fill in 1's or 0's if the station was inside the zone.
  - Both tables were exported for final revisions in [Data-Postprocessing.ipynb](./Data-Postprocessing.ipynb); the final datasets can be found [here](./data/).
  - The map below, although not exactly our intention with a difference-in-differences analysis, is still valuable to see the change in average ridership from 2024 to 2025.

## 🗒 **Further Notes**
  - Data cleaning and management notebooks can be found in the original repo, linked above.
  - This repo does *not* document all steps taken for the difference-in-differences analysis. See the final paper or presentation, linked above.


![Figure 1](https://raw.githubusercontent.com/vaughnmitchell13/vaughnmitchell13.github.io/main/DID-ECON308/parallel_trends.png)
![Figure 2](https://raw.githubusercontent.com/vaughnmitchell13/vaughnmitchell13.github.io/main/DID-ECON308/Layout.png)

