# Project 2 - Liquor Sales & Linear Regression

Michael Schillawski, February 9, 2018

General Assembly, Data Science Immersive

## Table of Contents

- [Repository Contents](#repository-contents) - Description of this repository's files
- [Data Description](#data-description) - Description of the Iowa liquor dataset
- [Project Overview](#project-overview) - Summary of the project's goals
- [Analysis Explanation](#analysis-explanation) - Explanation of project's methods and analysis
- [Project Concepts](#project-concepts) - Skills and concepts demonstrated

## Repository Contents

| FILENAME |     DESCRIPTION    |
|:-------------:|:--------------:|
|  [README](./README.md) | Project description |
| [2016-Iowa-Liquor-Sales-Projections](https://git.generalassemb.ly/mjschillawski/project-2/blob/master/code/2016%20Iowa%20Liquor%20Sales%20Projections.ipynb) |    Jupyter notebook with core project code    |
| [Process-2014-Data](https://git.generalassemb.ly/mjschillawski/project-2/blob/master/code/Process%202014%20Data.ipynb) | Jupyter notebook to process supplemental 2014 IA liquor data |
| [starter-code-mjs](https://git.generalassemb.ly/mjschillawski/project-2/blob/master/code/starter-code-mjs.ipynb) | Jupyter notebook with initial EDA |
|   [Presentation_Deck](https://docs.google.com/presentation/d/1S3uBMU3Wlp9ag-wdU-VGkqcJtDwohhdLDl2nD33hLXg/edit?usp=sharing)    |    Results slide deck    |

## Data Description

The Iowa liquor dataset provides transaction details of liquor purchase orders by holders of "Class E" liquor licenses in the state of Iowa. Liquor sales are controlled by the state, so licensess must purchase their inventory through the Alcohol Beverages Division. Class E licenses (for grocery, liquor, and convenience stores) allows commercial establishments to sell liquor for off-premises consumption.

Each order that a licensee places is recorded in that dataset, indexed by transaction ID. Details include the store name and location; county; details on the purchases item (type of liquor, vendor, bottle size, state cost, retail cost, and sale cost).

More details are available [here](https://data.iowa.gov/Economy/Iowa-Liquor-Sales/m3tr-qhgy).

## Project Overview

The goal of this project was to (1) understand the patterns of Iowa liquor sales in 2015 and (2) predict 2016 liquor sales from 2016 Q1 sales data.

My analysis showed that stores in a 7 counties accounted for nearly 50 percent of annual liquor sales, corresponding with population centers. Further, quarterly sales had a nearly perfect linear relationship with annual sales. 

I modeled the relationship between sales in the first 3 months of the year and total annual sales at the store level. Then I rolled the data forward to 2016 to predict 2016 annual sales, and aggregated individual store predictions at both the county and statewide level. I predict that 2016 liquor sales will exceed 2015 annual sales.

## Analysis Explanation

My exploratory data analysis revealed that all the variables had extremely close relationships with annual sales, both at the county and store level of analysis. Since my ultimate goal is to forecast 2016 annual sales, I looked for variables with the strongest relationship to it. This was monthly sales. I assumed that relationships between variables would be similiar in 2016 as in years past.

My testing set was constrained to transaction data from the only the first 3 months of 2016, so I built and evaluated a series of regressions that modeled the sales data differently. These ranged from single variable (first quarter sales) to multiple variables (sales in each of the first 3 months of the year), to model annual sales, fitting the models solely with 2015 sales data (and using 2014 sales data as an additional holdout) and fitting models with combined 2014 and 2015 liquor transaction data.

After evaluating the models on a variety of metrics including cross-validated $R^2$, mean squared error, and median absolute error, I used the fitted model with 3 months of sales and interactions effects to predict 2016 annual sales. I predict that 2016 liquor sales will exceed 2015 levels.

## Project Concepts

Single linear regression; multiple linear regression; interaction effects; missing data; imputation; hotdecking; exploratory data analysis; correlation; groupby; reshaping; regression metrics; cross-validation.