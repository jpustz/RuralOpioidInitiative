
<!-- README.md is generated from README.Rmd. Please edit that file -->

# Opioid Environment Program

This repository stores R scripts used to clean, join, and visualize data
for the CSDS opioid environment program. 

The data wrangled in this analysis will be further developed as a data and visualization product (Policy Scan) to characterize the multi-dimensional risk environment impacting the opioid crisis in the United States.

## Data Overview

++ to add grid of all datasets and scales included

We plan to source following data variables.

### Policy Variables
| Variable Construct | Variable Proxy | Source(s) | Metadata Document | Spatial Scale |
|-|-|-|-|-|
| Medicaid Expansion |  |  |  |  |
| Medicaid Expenditure |  |  |  |  | 
| Naloxone Access Laws |  |  |  |  |
| Good Samaritan Laws |  |  |  |  |
| Syringe Exchange,<br> Distribution, Possession Laws |  |  |  |  |
| Controlled Substance Laws |  |  |  |  |
| State & Local Govt. |  |  |  |  |
| Expenditure on health, public,<br> welfare, police, correction, etc. |  |  |  |  |

### Health Factors
| Variable Construct | Variable Proxy | Source(s) | Metadata Document | Spatial Scale |
|-|-|-|-|-|
| Access to MOUDs |  |  |  |  |
| Access to FQHC facilities |  |  |  |  |
| Access to Pharmacies |  |  |  |  |
| Access to Hospitals |  |  |  |  |
| Access to Mental Health <br> Practitioners |  |  |  |  |
| Primary Care Providers |  |  |  |  |
| Speciality Care Providers |  |  |  |  |
| Opioid overdose death rate |  |  |  |  |
| Hepatitis C infection rate |  |  |  |  |

### Demographic Factors
| Variable Construct | Variable Proxy | Source(s) | Metadata Document | Spatial Scale |
|-|-|-|-|-|
| Black, White percentage |  |  |  |  |
| Hispanic Percentage |  |  |  |  |
| Population with a Disability |  |  |  |  |
| College Aged |  |  |  |  |
| Population over 65 |  |  |  |  |
| Incarceration rates |  |  |  |  |
| SDOH Typologies |  |  |  |  |

### Economic Factors
| Variable Construct | Variable Proxy | Source(s) | Metadata Document | Spatial Scale |
|-|-|-|-|-|
| 'High Risk of Injury' jobs |  |  |  |  |
| Unemployment Rate |  |  |  |  |
| Poverty Rate |  |  |  |  |
| Per Capita Income |  |  |  |  |
| Population over 65 |  |  |  |  |
| Educational Attainment |  |  |  |  |
| Foreclosure Rate |  |  |  |  |
| Socioeconomic Disadvantage Index |  |  |  |  |
| Urban Core Opportunity |  |  |  |  |

### Physical Factors
| Variable Construct | Variable Proxy | Source(s) | Metadata Document | Spatial Scale |
|-|-|-|-|-|
| Urban/Suburban/Rural |  |  |  |  |
| Housing Occupancy Rate |  |  |  |  |
| Vacancy Rate |  |  |  |  |
| Long Term Occupancy |  |  |  |  |
| Mobile Home Structures |  |  |  |  |
| Rental Rates |  |  |  |  |
| Housing Unit Density |  |  |  |  |
| Alcohol Outlet Density |  |  |  |  |
| Hypersegregated Cities |  |  |  |  |
| Southern Black Belt |  |  |  |  |
| Native American Reservations |  |  |  |  |

### COVID Factors
| Variable Construct | Variable Proxy | Source(s) | Metadata Document | Spatial Scale |
|-|-|-|-|-|
| Historical Confirmed Case Count & Rate |  |  |  |  |
| Historical 7-day Average New Case Count & Rate |  |  |  |  |
| Statistical Hotspot/Coldspot |  |  |  |  |
| Spatiotemporal Profiles |  |  |  |  |
|  Non Pharmaceutical Interventions (NPI) |  |  |  |  |
| 'Essential worker' jobs |  |  |  |  |


## Data Wrangling

++ to add chart of data wrangling and cleaning scripts for data

## Access Calculations

| Input                                     | Script   | Output                                    | Purpose                                                                                                                                          |
| ----------------------------------------- | -------- | ----------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------ |
| data/\*                                   | R/01\_\* | data-output/01\_\*                        | Clean original data and get each into 3-column format with `name`, `category_service`, and `geometry`                                            |
| data-output/01\_\*                        | R/02\_\* | data-output/02\_\*                        | Combine datasets together to get combined point dataset (needed for map overlays), create point maps for each resource (for jurisdictional plan) |
| data-output/02\_\*                        | R/03\_\* | data-output/03\_\*                        | **(unused)** Create various buffers on point dataset, count buffers per zip                                                                      |
| data-output/01\_\*                        | R/04\_\* | data-output/min-dists-to-zip-centroid.csv | Calculate min distance from resources to zip centroids                                                                                           |
| data-output/min-dists-to-zip-centroid.csv | R/05\_\* | data-output/sum\_zscores.gpkg/.shp        | Convert centroid distances to summative z-scores                                                                                                 |
| data/carto….                              | R/99\_\* | data-output/carto…                        | One-off cleaning/joining scripts for manipulating CARTO datasets for collaborators                                                               |


## Team

Marynia Kolak (Lead), Qinyun Lin (Postdoc), Moksha Menghaney (Analyst), Angela Li (Analyst).
