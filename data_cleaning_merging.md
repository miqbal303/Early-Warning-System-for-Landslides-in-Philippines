# Data Cleaning & Merging Process

This document outlines the steps taken to clean and merge the datasets for analysis, focusing on removing unnecessary data, merging relevant datasets, and extracting critical geospatial information.

## 1. Dropping Unnecessary Columns

In the initial step of data cleaning, the following columns were removed due to their lack of significant information and the presence of a large number of missing values:

- **Unnamed: 6-9** from **rainfall_advisories_excel.xls** datasets.  
  These columns were found to be irrelevant, and their removal helped streamline the datasets.

## 2. Merging Datasets

To unify the heavy rainfall reports from multiple sources, the two datasets (**HeavyRainfallPH.csv** and **rainfall_advisories_excel.xls**) were merged using the `pd.concat()` method. This allowed for a consolidated dataset that encompasses all rainfall data in one place for further analysis.

## 3. Dropped Dataset

The **Landslide_Database_Philippines.csv** dataset was excluded from the analysis due to its lack of critical geospatial information, specifically latitude and longitude columns, which are necessary for performing geospatial analysis and mapping. This decision was made to focus on datasets with complete geographical data.

## 4. Extracting Geospatial Data

For geospatial analysis, latitude and longitude information was extracted from the `WKT` (Well-known text) column in the following datasets:

- **city_dataset.csv**
- **barangays_dataset.csv**

This step ensured that all necessary geospatial information was available for mapping and spatial analysis tasks, facilitating further insights into geographical distributions of the data.

---

By following these data cleaning and merging steps, the datasets were prepared for more robust analysis, particularly geospatial mapping and trend identification across cities, barangays, rainfall, and other related factors.
(Continue....)
