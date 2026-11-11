# Yelp New Orleans Restaurant Analysis

## View the full report

**[Open the rendered report](https://zararahim.github.io/yelp-new-orleans-project/yelp_new_orleans_project.html)**

The report contains all tables, maps, and code output. You don't need to run anything to view it.

## Research question

Where can someone find the best seafood restaurants in New Orleans, and do the geographic areas matter?

## Summary

I analyzed 331 New Orleans restaurants that are tagged as `seafood` or `oyster bars` in the Yelp Open Dataset. I joined them to 144,026 of their reviews, placed each restaurant inside official Census boundaries, and compared two geographic systems: ZIP Code Tabulation Areas (ZCTAs) and census tracts.

## Main findings

1. **ZIP areas give a more reliable comparison.** The 331 restaurants fall into 21 ZIP areas, averaging about 16 restaurants each. Census tracts split them into 89 areas, averaging about 3.6 each, so most tract averages rest on very few restaurants.
2. **Seafood restaurants cluster in a few areas.** ZIP 70130 has the most restaurants (93) with an average of 3.77 stars. Among areas with at least 10 restaurants, ZIP 70117 has the highest average (4.23 stars across 11 restaurants).
3. **Some restaurants fall outside the city limits.** Eleven restaurants list New Orleans as their Yelp city but sit in neighboring places such as Harahan, Jefferson, and Metairie. They are counted in the ZIP analysis but not in the tract analysis, which only covers Orleans Parish.

## Repository structure

- `README.md`: this file.
- `yelp_new_orleans_project.qmd`: the Quarto source file. It contains all code and text for Steps 1 through 6.
- `docs/yelp_new_orleans_project.html`: the rendered report published through GitHub Pages.
- `data/new_orleans/`: filtered data saved as compressed `.rds` files (New Orleans restaurants and their reviews).
- `data/boundaries/`: Census boundary files for places, census tracts, and ZCTAs.
- `yelp-new-orleans.Rproj`: the RStudio project file. Open this to work on the project.
- `.gitignore`: excludes the large raw Yelp files from GitHub.

The raw Yelp JSON files are stored in `data/raw/`. They are not included in this repository because they are too large for GitHub. To reproduce the analysis, download the files from the [Yelp Open Dataset](https://business.yelp.com/data/resources/open-dataset/) and place them in `data/raw/`.

## Where to find each step

- **Step 1:** Importing the large JSON files and the data-size table.
- **Step 2:** Filtering to New Orleans restaurants and saving the filtered data.
- **Step 3:** Choosing a related category group (seafood and oyster bars), with category counts and co-occurrence tables.
- **Step 4:** Joining restaurants to reviews (144,026 reviews).
- **Step 5:** Spatial join with the official New Orleans boundary, including the city-label check.
- **Step 6:** Comparing ZIP areas and census tracts, with a justification for the main system.

Steps 1 through 6 are all in `docs/yelp_new_orleans_project.html`.

## Large-data management

The review file is too large to load into memory at once, so the code reads it in pages and keeps only the selected restaurants' reviews. The full section is in the report under "Large-Data Management."

## Homework 6

[Add the location of the Homework 6 work here, such as a folder name or a link.]

## Data source

Yelp Open Dataset: https://business.yelp.com/data/resources/open-dataset/
