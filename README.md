# Tornado Analysis Project

## Objective
The goal of this project is to analyze tornado data to understand the energy dynamics and impacts of tornadoes across different Enhanced Fujita (EF) scale categories. Using the datasets, we calculate kinetic energy, classify tornadoes, and visualize trends in their impacts (deaths, injuries, and property damages).

---

## Datasets
### 1. `573dataform.csv`
- **Description**: Contains historical tornado data.
- **Key Columns**:
  - `TOR_F_SCALE`: Tornado scale classification (e.g., EF2, EF3).
  - `BEGIN_DATE`: Tornado start date.
  - `TOR_LENGTH`: Tornado length in miles.
  - `TOR_WIDTH`: Tornado width in yards.
  - `DEATHS_DIRECT`: Number of direct deaths caused by the tornado.
  - `INJURIES_DIRECT`: Number of direct injuries caused by the tornado.
  - `DAMAGE_PROPERTY_NUM`: Property damage in USD.

### 2. `violenttorke.csv`
- **Description**: Additional tornado dataset used for kinetic energy calculations.
- **Key Columns**:
-   Same as `573dataform.csv` but includes specific kinetic energy information
-  `HIGHEST_SPEED`: Tornado maximum wind speed (mph).
-  `DOW_SPEED`: Tornado maximum wind speed measured by Dopplar on Wheels (mph).

### Data Transformations
- Columns for kinetic energy and combined EF scales are added.
- Length, width, and wind speed are converted to metric units for calculations.

---

## Analysis Workflow
### Steps:
1. **Calculate Kinetic Energy Density**:
   - Using wind speeds from EF scale definitions, calculate the energy density for each category.

2. **Filter and Preprocess Data**:
   - Include only F/EF2 and higher tornadoes for impact analysis.
   - Combine F and EF scales into a unified scale (e.g., EF2 and F2 into `F/EF2`).

3. **Kinetic Energy Calculations**:
   - Use tornado dimensions (length, width, and height assumption of 1000m) to calculate kinetic energy.

4. **Visualization**:
   - Generate scatter plots, bar charts, and radar charts to showcase trends in kinetic energy and tornado impacts.

5. **Aggregate Results**:
   - Summarize the total deaths, injuries, and property damages for F/EF4 and F/EF5 tornadoes.

---

## Requirements
### Python Packages
- **Core Libraries**: `pandas`, `numpy`, `matplotlib`
- Additional: `seaborn` (for advanced visualizations, optional)

---

## Results Summary
- **Key Findings**:
  - High kinetic energy is correlated with increased tornado width and wind speed.
  - F/EF5 tornadoes account for the majority of fatalities and property damage.
  - Aggregated impacts for F/EF4 and F/EF5 tornadoes demonstrate significant regional variability.

- **Visualizations**:
  - Energy density by EF scale.
  - Stacked bar charts for impacts (deaths, injuries, damages).
  - Radar charts for average impacts by tornado category.

---


