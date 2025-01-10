## Technical Analysis

### Overview
This document provides a detailed breakdown of the technical steps taken to conduct the AeroClub Operational Analysis, including data preparation, visualizations, and key calculations.

### Analysis Steps

#### Data Preparation
- **Objective:** Prepare data for analysis by consolidating multiple sources, including flight logs and financial reports.
- **Tools:** Power Query for data cleaning.
- **Steps:**
  - Standardized column names and formats.
  - Removed duplicates and handled missing values.

#### Fleet Utilization Analysis
- **Objective:** Evaluate usage rates of different aircraft.
- **Visualization:** Bar charts and pie charts highlighting flight hours per aircraft.
- **KPI:** Utilization rate = Hours flown / Total available hours.

#### Seasonality Trends
- **Objective:** Identify patterns in flight activity.
- **KPI Calculation:**
  ```markdown
  Saison = IF DATEPART('month', [Date]) IN (3, 4, 5) THEN 'Printemps'
           ELSEIF DATEPART('month', [Date]) IN (6, 7, 8) THEN 'Été'
           ELSEIF DATEPART('month', [Date]) IN (9, 10, 11) THEN 'Automne'
           ELSE 'Hiver'
  ```
- **Visualization:** Line charts showing monthly trends.

#### Financial Performance
- **Objective:** Assess revenue distribution by aircraft and activity type.
- **KPI Calculation:** Revenue per hour = Total revenue / Flight hours.
- **Visualization:** Scatter plots and heatmaps.

### Technical Implementation
#### Calculations in Tableau
1. **Hourly Bins:**
   ```markdown
   Horaire_bin = CASE
                 WHEN DATEPART('hour', [Heure]) < 9 THEN 'Matin'
                 WHEN DATEPART('hour', [Heure]) < 14 THEN 'Midi'
                 ELSE 'Après-midi'
                 END
   ```
2. **Projection Scenarios:**
   - Optimistic:
     ```markdown
     Projected_hours = Current_hours + Growth_rate * Remaining_period
     ```
   - Pessimistic:
     ```markdown
     Projected_hours = Current_hours - Decline_rate * Remaining_period
     ```
### Parameters
- Monthly projected flight hours: `INT 3000/12`
- Annual projected flight hours: `3000`

## Issues and Solutions

### Update Management
1. **Issue**: Monthly data updates
2. **Solution**:
   - Creation of intermediate data model
   - Strict field standardization
   - Automated validation process

### Anomaly Processing
1. **Non-standard Airfields**
   - Solution: "Others" categorization in source CSV
   - Impact: Improved analysis representativeness

### Weather Impact Analysis
1. **Operating Hours**: 8:00-19:00 (winter period)
2. **Average Used**: 10 hours/day
3. **Unavailability Factors**:
   - 95 rain days/year
   - ~8 precipitation days/month
4. **Utilization Scenarios**:
   - Optimistic: 81% (700 unavailable hours)
   - Pessimistic: 75% (900 unavailable hours)
   - Nominal: 78% (800 unavailable hours)

## Technical Recommendations

### Process Optimization
1. **Data Pipeline**
   - Live connection implementation
   - Python CSV preprocessing
   - Import automation

2. **Maintenance**
   - Systematic backup before updates
   - Post-import data validation
   - Modification documentation

### Suggested Improvements
1. Optimization of underutilized aircraft usage
2. Time slot adjustment based on temporal analysis
3. Development of data-driven promotions

## Additional Notes
- Complete dashboards available upon request
- Certain sections redacted for confidentiality
- Regular update of weather impact calculations recommended
#### Dashboard Implementation
- **Tools Used:** Tableau for visualizations.
- **Steps:**
  1. Imported cleaned datasets.
  2. Created calculated fields for KPIs.
  3. Designed dashboards with filters for interactivity.



### Findings
#### Key Visualizations
1. **Fleet Utilization:**
   ![Fleet Utilization](dashboard_screenshots/fleet_utilization.png)
2. **Seasonality Trends:**
   ![Seasonality Trends](dashboard_screenshots/seasonality_trends.png)
3. **Financial Performance:**
   ![Financial Performance](dashboard_screenshots/financial_performance.png)

#### Recommendations
- Encourage use of underutilized aircraft (e.g., XL8, BOMI).
- Optimize schedules to increase off-peak activity.
- Develop tailored promotions to improve member engagement.

### Dashboard Evidence
- Full dashboards are available upon request, with certain sections redacted to maintain confidentiality.
