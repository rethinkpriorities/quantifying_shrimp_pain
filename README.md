# Quantifying shrimp pain

View the rendered methods document here: [https://rethinkpriorities.github.io/quantifying_shrimp_pain/](https://rethinkpriorities.github.io/quantifying_shrimp_pain/)

## About
This is the supplemental methods document and files for our report 'Quantifying and Prioritizing Shrimp Welfare Threats'. It contains all of the data and code used for the analyses in the report.
The files render a quarto book that details the method and code we used. The book has three chapters covering:
1.  Set up and data preparation
2.  Estimating the pain caused by welfare threats
3.  Results

We focus on penaeids in ongrowing farms and broodstock facilities.

## How to use
If you want to read through the methods document and see all of the code, view the [rendered methods document](https://rethinkpriorities.github.io/quantifying_shrimp_pain/).

If you would like to run the code yourself locally, download all of the files in the repository. Open the `quantifying_welfare_threats.Rproj` file to begin. This will automatically set the working directory and warn if any packages need to be installed.

## Folders
- `docs` contains the rendered html files and other site files.

- `chapters` contains the .qmd files (Quarto markdown files) where the method and code are written. This has one subfolder called `images` which has all of the Pain-Track's shown as tables in .png files.

- `data` contains the .RData and .csv data files used in the analyses.

- `results` contains the .csv results files calculated in the analyses.

### data files 
| File name ___________________________  | Description ____________________________________________________________________  |
|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| VN_clean.csv | Data from the [Shrimp Welfare Project's Vietnam Scoping Report](https://perma.cc/DQ63-TNAC) |
| allspecies_dof.RData     | Data calculated in the Set up and Data Preparation chapter for the number of shrimp that die on farms annually (including pre-slaughter mortality) |
| average_days_lived.RData | Data calculated in the Set up and Data Preparation chapter for the number of days lived on average for each life stage (larval, postlarval, juvenile-subadult), weighted by the probabilty of a shrimp being from a given species. |  
| female_broodstock_prop.RData | Data calculated in the Health chapter for the proportion of shrimp that are broodstock out of all shrimp that die on farms in the ongrowing stage (including both slaughter and pre-slaughter deaths. |
| die_on_farm_samples.csv | Raw [Guesstimate model](https://www.getguesstimate.com/models/21679) estimates (5000 samples) for the number of shrimp who die on farms (including pre-slaughter mortality) by species. Used to calculate  `allspecies_dof.RData` (above) |                                                                                      |
| monodon_days_lived.csv otherpen_days_lived.csv vannamei_days_lived.csv | Raw [Guesstimate model](https://www.getguesstimate.com/models/21679) estimates (5000 samples) for the number of days lived on average for each life stage (larval, postlarval, juvenile-subadult). Each species is in a separate file. Used to calculated `average_days_lived.RData' (above) |
| monodon_mortality_rates.csv otherpen_mortality_rates.csv vannamei_mortality_rates.csv  | Raw [Guesstimate model](https://www.getguesstimate.com/models/21679) estimates (5000 samples) for the mortality rates of each life stage (larval, postlarval, juvenile-subadult) of each species. Each species is in a separate file. Used to calculate `stage_probabilities.RData` (below) |
| prop_allspecies_dof.RData | Data calculated in the Set up and Data Preparation chapter for the proportion of farmed shrimp that come from each species (*P. vannamei*, *P. monodon*, and other penaeids) |
| slaughtered_samples.csv | Raw [Guesstimate model](https://www.getguesstimate.com/models/21679) estimates (5000 samples) for the number of shrimp slaughtered in 2020 by species. The file includes estimates for *Macrobrachium* but that data is not analyzed here.                                      |
| stage_probabilities.RData   | Data calculated in the Set up and Data Preparation chapter for the probability of a shrimp dying in each life stage, weighted by the proportion of farmed shrimp that comes from each species.                                                                                |
