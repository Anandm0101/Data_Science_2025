# Chicago Roads: Safer or Riskier?

![Chicago Traffic](https://img.shields.io/badge/Chicago-Traffic%20Analysis-blue)
![Python](https://img.shields.io/badge/Python-3.x-success)
![Data Science](https://img.shields.io/badge/Data%20Science-Analysis-orange)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Models-brightgreen)

## 📊 Project Overview

Motor‑vehicle collisions are one of the leading causes of injury and property loss in Chicago. This project analyzes the City of Chicago's Traffic Crashes data to understand where, when, and why these incidents occur. The aim is to provide evidence-based insights that can help make Chicago roads safer for drivers, cyclists, and pedestrians alike.

- According to the latest figures, Chicago logged about 112,000 crash reports in 2024, and nearly 30,000 additional crashes by the first week of April 2025
- This project leverages the publicly available Traffic Crashes dataset from the City of Chicago Data Portal
- Our analysis includes crash records from 2020 onwards, focusing on recent patterns and trends

## 🎯 Project Goals

- Determine whether Chicago roads are becoming safer or riskier over time
- Identify key drivers of crash severity and frequency
- Analyze trends by time, location, weather, vehicle type, speed limits, and driver behavior
- Track injury and fatality patterns to inform safety measures
- Provide actionable insights to city planners, policymakers, and the public

## 📝 Research Questions

1. **Spatial Risk Hotspots** – Which Chicago neighborhoods and street types experience the highest crash densities, and how do these patterns evolve over time?
2. **Temporal Patterns** – Are certain months, days of the week, or hours of the day consistently associated with elevated crash severity?
3. **Environmental & Roadway Factors** – How do weather conditions, lighting, and roadway characteristics influence the likelihood of severe outcomes?
4. **Predictive Modeling** – Can machine‑learning models reliably predict crash severity categories and help prioritize high-risk locations?
5. **Policy Simulation** – What potential reduction in injuries could be achieved under hypothetical interventions?

## 🧩 Data Preparation & Analysis Methods

### ETL Pipeline

Our custom ETL (Extract, Transform, Load) pipeline processes the raw Chicago Traffic Crashes dataset through several key steps:

1. **Data Loading & Sampling** – Flexible loading with optional sampling for rapid iteration
2. **Data Cleaning** – Removing duplicates, handling missing values, standardizing date formats
3. **Feature Engineering** – Creating derived features such as:
   - Temporal dimensions (year, month, day, hour, day of week, weekend indicator, time of day, seasons)
   - Weather categories (Clear, Rain, Snow, Reduced Visibility, etc.)
   - Crash severity classification (No Injury, Non-Fatal Injury, Fatal)
   - Crash type grouping
4. **Temporal Filtering** – Focusing on crashes from 2020 onwards
5. **Data Export** – Generating processed datasets for analysis
6. **Large Dataset Handling** – Implementing chunk-based processing for efficient memory usage

### Analysis Methods

We employed several advanced analytical techniques:

#### 1. Random Forest for Crash Type Prediction
- Predicting the most common crash types using environmental and roadway features
- Comparing model performance against baseline predictions
- Analyzing feature importance to identify key predictors

#### 2. DBSCAN Clustering for Geographic Hotspots
- Identifying spatial clusters of crashes across Chicago
- Analyzing crash characteristics within each hotspot
- Visualizing the geographic distribution of high-risk areas

#### 3. Time Series Analysis for Temporal Patterns
- Examining daily, weekly, monthly, and seasonal crash patterns
- Performing seasonal decomposition to identify underlying trends
- Comparing weekday vs. weekend crash distributions
- Analyzing hourly patterns throughout the day

## 📈 Key Insights & Visualizations

### Crash Severity Distribution
- Majority of crashes result in no injuries
- Significant portion lead to non-fatal injuries
- Small but critical percentage result in fatalities

### Environmental Factors Analysis
- Weather conditions significantly impact crash severity
- Lighting conditions show strong correlation with injury rates
- Road alignment/condition affects crash outcomes
- Traffic control infrastructure influences severity

### Temporal Patterns
- Distinctive patterns by time of day (morning, afternoon, evening, night)
- Day of week variations in crash frequency and severity
- Clear seasonal patterns throughout the year

### Crash Type Analysis
- Pedestrian and bicycle crashes show highest injury rates
- Injury rates vary significantly by crash type

### Infrastructure Analysis
- Speed limits strongly correlate with injury rates
- Road types show varying patterns of injury severity
- Traffic control condition impacts crash outcomes
- Road geometry (curves, hills) affects severity

## 🔍 Model Results

### Random Forest for Crash Type Prediction
The model successfully predicts common crash types based on environmental and roadway features, outperforming baseline predictions. Posted speed limit, environmental conditions, and temporal aspects emerged as key predictive factors.

### DBSCAN Clustering for Geographic Hotspots
Spatial analysis identified distinct crash hotspots across Chicago, revealing locations with elevated risk. Each hotspot shows characteristic crash types and severity patterns, providing targets for focused intervention.

### Time Series Analysis
Temporal analysis revealed clear patterns in crash occurrence by hour, day, month, and season. These patterns differ significantly between weekdays and weekends, and certain times of day show elevated risk for severe crashes.

## 💻 Technical Implementation

The project is implemented in Python, utilizing several key libraries:
- **Data Processing**: Pandas, NumPy
- **Visualization**: Matplotlib, Seaborn
- **Machine Learning**: Scikit-learn (RandomForestClassifier, DBSCAN)
- **Time Series Analysis**: Statsmodels

## 👥 Team Members

| Team Member                  | Email          | GitHub Profile |
|------------------------------|----------------|----------------|
| Karthik Kumar Muppala        | kmupp@uic.edu  | [m-karthik-kumar](https://github.com/m-karthik-kumar) |
| Kodati Shruthi               | skoda13@uic.edu | [Shruthikodati](https://github.com/Shruthikodati) |
| Siddhi Dabholkar             | sdabh@uic.edu  | [siddhidabholkar10](https://github.com/siddhidabholkar10) |
| Meena Anand                  | ameen4@uic.edu | [Anandm0101](https://github.com/Anandm0101) |
| Naga Malleshwar Reddy Lingala | nling4@uic.edu | [malleshwar](https://github.com/malleshwar) |

## 🤝 Contributions

| Contribution | Team Members |
|--------------|--------------|
| ETL and Data Preprocessing, Cleaning, and Visualizations | Anand and Siddhi |
| Random Forest for Crash Type Prediction and Visualizations | Malleshwar and Karthik |
| DBSCAN for Geographic Crash Hotspots and Visualizations | Shruthi and Anand |
| Time Series Analysis for Temporal Patterns and Visualizations | Malleshwar, Karthik, Shruthi, and Siddhi |

## 🔮 Future Work

- Enhanced data cleaning and imputation strategies
- Integration with additional datasets (vehicles and people involved in crashes)
- Implementation of advanced spatial features
- Development of XGBoost models for improved prediction
- Creation of ARIMA models for crash frequency forecasting
- Integration of language models for crash narrative analysis
- Development of interactive dashboard combining model outputs with geographic visualization

## 🙏 Acknowledgments

We would like to thank the City of Chicago for making this data publicly available through their Data Portal, enabling this research to help make Chicago roads safer.
