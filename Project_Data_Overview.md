# Project Data Overview

This repository contains multiple datasets related to cities, landslides, soil moisture, rainfall, and earthquakes in the Philippines. Below is a detailed description of each dataset, including the types of columns, the number of missing values, and whether the columns are numerical or categorical.

---

## 1. city_dataset.csv
**Shape:** (1444, 5)  
This dataset contains information about different cities in the Philippines.

### Columns:
- `city`: (Categorical) City name.
- `region`: (Categorical) Region of the city.
- `province`: (Categorical) Province of the city.
- `city_code`: (Categorical) Code assigned to each city.
- `WKT`: (Geospatial) Well-known text format describing the geometry of the city.

**Missing Values:**  
- No missing values.

---

## 2. barangays_dataset.csv
**Shape:** (42,058, 7)  
This dataset provides details about barangays (small administrative districts) in the Philippines.

### Columns:
- `WKT`: (Geospatial) Well-known text format for barangay boundaries.
- `region`: (Categorical) Region of the barangay.
- `province`: (Categorical) Province of the barangay.
- `city_code`: (Categorical) City code.
- `city`: (Categorical) City name.
- `barangays`: (Categorical) Barangay name.
- `geometry`: (Geospatial) Geometrical data of the barangay.

**Missing Values:**  
- No missing values.

---

## 3. philippines_landslides.shp
**Shape:** (675, 33)  
This shapefile contains geospatial data for landslides that occurred in the Philippines.

### Columns:
- Multiple columns related to landslide events including `source_nam`, `event_date`, `event_titl`, `fatality_c`, `injury_cou`, and geospatial columns like `longitude`, `latitude`, `geometry`.

**Missing Values:**  
- Columns with missing values include:
  - `source_lin`: 9 missing values.
  - `event_time`: 453 missing values.
  - `event_desc`: 4 missing values.
  - `fatality_c`: 118 missing values.
  - `injury_cou`: 502 missing values.
  - `storm_name`: 429 missing values.
  - `photo_link`: 654 missing values.
  - `admin_divi`: 12 missing values.

---

## 4. monthly_median_soil_moisture_with_coords_city_year_month_2015_2024.csv
**Shape:** (316,492, 9)  
This dataset contains monthly median soil moisture data for various cities in the Philippines from 2015 to 2024.

### Columns:
- `system:index`: (Categorical) System-generated index.
- `city`: (Categorical) City name.
- `closest_city`: (Categorical) Closest major city.
- `latitude`: (Numerical) Latitude of the location.
- `longitude`: (Numerical) Longitude of the location.
- `month`: (Numerical) Month of the measurement.
- `soil_moisture_am`: (Numerical) Soil moisture value.
- `year`: (Numerical) Year of the measurement.
- `.geo`: (Geospatial) Geospatial information.

**Missing Values:**  
- No missing values.

---

## 5. HeavyRainfallPH.csv
**Shape:** (4736, 6)  
This dataset contains information about heavy rainfall reports in the Philippines.

### Columns:
- `Report No.`: (Numerical) Report identifier.
- `Date`: (Categorical) Date of the report.
- `Time of Report`: (Categorical) Time when the report was made.
- `Region`: (Categorical) Region affected by the rainfall.
- `Weather System`: (Categorical) Type of weather system.
- `Effects`: (Categorical) Effects of the rainfall.

**Missing Values:**  
- No missing values.

---

## 6. earthquake_ph_list_2018-Aug2024.csv
**Shape:** (89,205, 6)  
This dataset lists earthquakes that occurred in the Philippines from 2018 to August 2024.

### Columns:
- `Datetime`: (Categorical) Date and time of the earthquake.
- `Latitude`: (Numerical) Latitude of the earthquake epicenter.
- `Longitude`: (Numerical) Longitude of the earthquake epicenter.
- `Depth`: (Numerical) Depth of the earthquake.
- `Magnitude`: (Numerical) Magnitude of the earthquake.
- `Location`: (Categorical) Location description.

**Missing Values:**  
- `Datetime`: 718 missing values.
- `Latitude`: 718 missing values.
- `Longitude`: 723 missing values.
- `Depth`: 721 missing values.
- `Magnitude`: 1,293 missing values.

---

## 7. Landslide_Database_Philippines.csv
**Shape:** (2,141, 7)  
This dataset contains details of landslide events in the Philippines.

### Columns:
- `Year(YYYY)`: (Numerical) Year of the landslide.
- `LANDSLIDE CATEGORY`: (Categorical) Category of the landslide.
- `LANDSLIDE TRIGGER`: (Categorical) Trigger of the landslide.
- `REGION`: (Categorical) Region where the landslide occurred.
- `PROVINCE`: (Categorical) Province affected.
- `MUNICIPALITY`: (Categorical) Municipality affected.
- `GENERAL SOURCES`: (Categorical) Sources of the landslide data.

**Missing Values:**  
- `LANDSLIDE CATEGORY`: 111 missing values.
- `LANDSLIDE TRIGGER`: 100 missing values.
- `MUNICIPALITY`: 317 missing values.
- `GENERAL SOURCES`: 1 missing value.

---

## 8. rainfall_advisories_excel.xls
**Shape:** (16,442, 10)  
This dataset contains rainfall advisories.

### Columns:
- `Report No.`: (Numerical) Report number.
- `Date`: (Categorical) Date of the advisory.
- `Time of Report`: (Categorical) Time of the advisory.
- `Region`: (Categorical) Region affected.
- `Weather System`: (Categorical) Weather system in place.
- `Effects`: (Categorical) Effects of the rainfall.
- `Unnamed: 6-9`: (Unused) Empty columns with no significant data.

**Missing Values:**  
- `Report No.`: 1 missing value.
- `Date`: 231 missing values.
- `Time of Report`: 296 missing values.
- `Region`: 344 missing values.
- `Weather System`: 384 missing values.
- `Effects`: 487 missing values.
- Columns `Unnamed: 6-9` have over 16,000 missing values, as they are not used.

---

### Summary of Column Types:
- **Numerical Columns:**
  - Depth (earthquake), Magnitude (earthquake), Latitude, Longitude, Month, Year, Soil Moisture (soil_moisture_df), Report No., and more.

- **Categorical Columns:**
  - City, Region, Province, Weather System, Effects, Location, Municipality, LANDSLIDE CATEGORY, and more.

---

### Notes:
- Many datasets contain geospatial columns (`WKT`, `geometry`, `.geo`), which require special handling for mapping and geospatial analysis.
- Missing values vary by dataset, with some columns having significant amounts of missing data. The missing values should be carefully handled during preprocessing.
- Peak Ground Acceleration dataset(.kmz data) does not have relative info(attributes) so i simply drop it 
