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
| [starter-code-mjs](https://git.generalassemb.ly/mjschillawski/project-2/blob/master/code/starter-code-mjs.ipynb) | Jupyter notebook with inital EDA |
|   [Presentation_Deck](https://docs.google.com/presentation/d/1S3uBMU3Wlp9ag-wdU-VGkqcJtDwohhdLDl2nD33hLXg/edit?usp=sharing)    |    Results slide deck    |

## Data Description

The Iowa liquor dataset provides transaction details of liquor purchase orders by holders of "Class E" liquor licenses in the state of Iowa. Liquor sales are controlled by the state, so licensess must purchase their inventory through the Alcohol Beverages Division. Class E licenses (for grocery, liquor, and convenience stores) allows commercial establishments to sell liquor for off-premises consumption.

Each order that a licensee places is recorded in that dataset, indexed by transaction ID. Details include the store name and location; county; details on the purchases item (type of liquor, vendor, bottle size, state cost, retail cost, and sale cost).

More details are available [here](https://data.iowa.gov/Economy/Iowa-Liquor-Sales/m3tr-qhgy).

## Project Overview

ipso

## Analysis Explanation

My exploratory data analysis revealed that all the variables had extremely close relationships with annual sales, both at the county and store level of analysis. My ultimate goal is to forecast 2016 annual sales using only transaction data from the first 3 months of 2016. 

I assumed that relationships between variables would be similiar in 2016 as in years past. I designed a series of linear regressions, ranging from single (first quarter sales) to multiple variables (sales in each of the first 3 months of the year), to model annual sales, fitting the models based 2014 and 2015 liquor transaction data.

After evaluating the models on a variety of metrics, I used the fitted model to predict 2016 annual sales. I predict that 2016 liquor sales will exceed 2015 levels.

## Project Concepts

Single linear regression; multiple linear regression; interaction effects; missing data; imputation; hotdecking; exploratory data analysis; correlation; groupby; reshaping; regression metrics; cross-validation.