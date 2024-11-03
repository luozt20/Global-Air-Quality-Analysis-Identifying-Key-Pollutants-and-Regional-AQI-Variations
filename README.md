# Air Quality Analysis

## Project Overview

This project, **Mapping the Polluted Skies: Analyzing Air Quality Metrics**, investigates global air pollution patterns using air quality index (AQI) data. The main goal is to explore relationships between different pollutants and AQI metrics, identify highly polluted regions, and evaluate potential correlations among various pollutants. Specific focus was placed on the pollutants PM2.5, CO, NO2, and Ozone. Additionally, a case study on India provides insights into regional air quality variations, influenced by factors such as the monsoon season.

## Dataset

The dataset used for this project includes AQI data from multiple cities around the world. It contains 23,463 records and focuses on eight main variables:

- **Country**: Name of the country
- **City**: Name of the city
- **AQI**: Overall AQI value (numerical)
- **AQI Category**: Overall AQI category (from "Good" to "Hazardous")
- **CO**: Carbon Monoxide AQI value
- **Ozone**: Ozone AQI value
- **NO2**: Nitrogen Dioxide AQI value
- **PM2.5**: Particulate Matter AQI value (diameter ≤ 2.5 micrometers)

## Analysis Overview

1. **Exploratory Data Analysis (EDA)**:
   - Provided a global overview of average AQI values, highlighting regions with high pollution levels, specifically in Asia and Africa.
   - Used ridgeline charts to show pollutant AQI values across different AQI categories.

2. **Statistical Analysis**:
   - Conducted Tukey's HSD test to compare mean AQI values for pollutants, revealing significant differences for CO but limited variation for NO2 in some AQI categories.
   - Calculated correlations among pollutant AQI values, identifying PM2.5 as a primary contributor to overall AQI.

3. **Model Building & Diagnostics**:
   - Applied K-means clustering, finding limited clustering potential among pollutant AQI values.
   - Built a linear regression model to estimate PM2.5 levels based on CO, NO2, and Ozone values. A Box-Cox transformation was applied to address right-skewed data distribution.

4. **Case Study on India**:
   - Examined AQI distribution within India, finding an increasing AQI trend from south and east towards the northwest, likely influenced by the monsoon season.

## Key Findings

- **PM2.5 Dominance**: PM2.5 was found to be the most significant contributor to overall AQI.
- **Geographical Patterns**: Asia and Africa were identified as regions with high pollution, with substantial variability in AQI across different countries.
- **Challenges in Clustering and Modeling**: Data did not group well for clustering, and linear regression modeling indicated heteroskedasticity and non-linear relationships in a global context.
- **Regional Insights**: Analyzing AQI within a single country (India) allowed for better model fit, providing clearer regional patterns.

## Future Directions

- Conduct more localized analyses for improved interpretability.
- Incorporate additional variables like economic, geographic, and policy data for more comprehensive insights.
- Explore time-series analysis to monitor AQI trends over time.
