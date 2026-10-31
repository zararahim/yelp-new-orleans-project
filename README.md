# Yelp New Orleans Restaurant Analysis

## Homework 5 — Steps 1 and 2

This repository contains my work for Steps 1 and 2 of the Yelp New Orleans Restaurant Analysis project.

## View the Report

**[View the rendered HTML report](yelp_new_orleans_project.html)**

The report documents the process used to:

- Import the Yelp business and review JSON datasets
- Retain the variables needed for the project
- Filter the business dataset to New Orleans restaurants
- Check for missing latitude, longitude, and category values
- Save the filtered New Orleans restaurant data as a compressed RDS file

## Results

The original Yelp data contained:

- **150,346 businesses**
- **6,990,280 reviews**

After filtering for businesses located in New Orleans, Louisiana with `Restaurants` in their Yelp categories, the resulting dataset contains:

- **2,259 New Orleans restaurants**
- **0 missing latitude values**
- **0 missing longitude values**
- **0 missing category values**

## Repository Structure

```text
.
├── data/
│   └── new_orleans/
│       └── business_new_orleans.rds
├── yelp_new_orleans_project.qmd
├── yelp_new_orleans_project.html
├── yelp_new_orleans_project_files/
└── .gitignore
```

The original Yelp JSON files are stored locally in `data/raw/` and excluded from this repository through `.gitignore` because of their large file sizes.

## Data Source

The data comes from the official [Yelp Open Dataset](https://business.yelp.com/data/resources/open-dataset/).
