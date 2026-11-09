# Yelp New Orleans Restaurant Analysis

## Homework 5 — Steps 1 and 2

This repository contains my work for Steps 1 and 2 of the Yelp New Orleans Restaurant Analysis project.

### [View the Full Report](https://zararahim.github.io/yelp-new-orleans-project/)

## Overview

For this assignment, I used the official Yelp Open Dataset to prepare the data for the New Orleans restaurant analysis. I imported the large Yelp business and review JSON files into R, filtered the business data to New Orleans restaurants, and saved the resulting dataset as a compressed RDS file for use in later stages of the project.

## Results

The original Yelp datasets contained:

- **150,346 businesses**
- **6,990,280 reviews**

After filtering for businesses located in New Orleans, Louisiana with `Restaurants` in their Yelp categories:

- **2,259 New Orleans restaurants** remained
- **0** missing latitude values
- **0** missing longitude values
- **0** missing category values

## Repository Files

- `index.html` — rendered report published through GitHub Pages
- `yelp_new_orleans_project.qmd` — Quarto source code for the analysis
- `data/new_orleans/business_new_orleans.rds` — filtered New Orleans restaurant dataset
- `yelp_new_orleans_project_files/` — supporting files for the rendered HTML report
- `yelp-new-orleans-project.Rproj` — RStudio project file
- `.gitignore` — excludes the large raw Yelp JSON files from GitHub

## Data Management

The original Yelp JSON files are stored locally in `data/raw/` and are not included in this repository because of their large file sizes. The `data/raw/` directory is excluded using `.gitignore`.

The filtered New Orleans restaurant data is saved as a compressed RDS file so that the full Yelp business dataset does not need to be imported again during later stages of the project.

## Data Source

Data was obtained from the official [Yelp Open Dataset](https://business.yelp.com/data/resources/open-dataset/).
