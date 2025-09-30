# India Airbnb Market Analysis using Python

## 🎯 Project Overview

This project conducts an in-depth **Exploratory Data Analysis (EDA)** and **Geospatial Analysis** of the Airbnb market across India. The goal is to uncover key market trends, identify high-demand regions, analyze pricing strategies, and understand the distribution of different listing types and their features based on a dataset of top listings.

This analysis provides valuable insights for potential hosts looking to enter the Indian market, existing hosts aiming to optimize their listings, and travelers seeking an understanding of accommodation options.

---

## 📁 Dataset

The analysis is based on a dataset of **500 top-performing Airbnb listings** across India.

### Key Data Features
The dataset contains crucial columns for market analysis, including:

* **`name`**: Name of the listing.
* **`address`**: Full geographical address (used for splitting location).
* **`location/lat`**, **`location/lng`**: Geographical coordinates for mapping.
* **`isHostedBySuperhost`**: Boolean indicating if the host is a Superhost.
* **`roomType`**: Type of accommodation (e.g., Entire Home, Private Room, Entire Villa, Farm Stay).
* **`numberOfGuests`**: Maximum capacity of the listing.
* **`pricing/rate/amount` (renamed to `price`)**: Price per night.
* **`stars`**: Guest rating.

## 💡 Key Findings and Metrics

The initial analysis of the top 500 listings revealed:

* **Total Market Capacity:** The collective capacity of these listings is **5,780** guests.
* **Geographical Spread:** The top listings are distributed across **217 unique destinations** within India.
* **Top 5 Destinations by Listing Count:**
    1.  Candolim, Goa
    2.  New Delhi, Delhi
    3.  Lonavla, Maharashtra
    4.  Anjuna, Goa
    5.  Jaipur, Rajasthan

## 🛠️ Methodology and Analysis Steps

The project followed a standard data science pipeline:

1.  **Data Loading & Inspection:** Loaded the raw data and inspected column types, non-null counts, and memory usage.
2.  **Data Cleaning & Preprocessing:**
    * Handled missing values, particularly in the `stars` column.
    * Renamed the price column from `pricing/rate/amount` to `price` for better readability.
    * Feature Engineering: The multi-component `address` column was split to extract distinct **`location`**, **`state`**, and **`country`** columns to facilitate state-wise and city-wise segmentation.
3.  **Exploratory Data Analysis (EDA):** Calculated summary statistics for key metrics like guest capacity, unique stays, and geographical distribution.
4.  **Geospatial Analysis:** Used geographic data to create a **HeatMap** overlay of the listings, showing the concentration and density of high-priced listings across India using the `folium` library.
5.  **Feature Relationship Analysis:** Analyzed the relationship between pricing, room type, number of guests, and Superhost status.

## 💻 Technology Stack

* **Language:** Python
* **Core Libraries:**
    * `pandas` (for data manipulation and cleaning)
    * `numpy` (for numerical operations)
* **Visualization:**
    * `folium` (for interactive geospatial mapping and HeatMap generation)
    * `tabulate` (for clean console output of location counts)
    * `matplotlib` / `seaborn` (for additional visualizations)
* **Environment:** Jupyter Notebook (`.ipynb`)
