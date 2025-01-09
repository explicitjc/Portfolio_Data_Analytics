# AeroClub Operational Analysis (2024)

## Disclaimer

The data used in this analysis belongs exclusively to the Annecy AeroClub and has been anonymized to ensure privacy and confidentiality. The purpose of this report is to showcase the operational performance of the AeroClub, demonstrate advanced data analysis skills, and provide actionable recommendations for improving operations, member engagement, and financial outcomes.

---

## Overview

This analysis provides a comprehensive evaluation of the Annecy AeroClub’s performance in 2024. It explores fleet utilization, financial outcomes, and member activity while leveraging data visualization tools like Tableau to uncover trends and propose data-driven solutions. The report balances technical depth with actionable insights, tailored for stakeholders such as data analysts, pilots, and AeroClub leadership.

---

## Key Questions Addressed
1. **How efficiently is the fleet being utilized, and which aircraft require attention?**
2. **What temporal patterns can be leveraged to boost activity during low-demand periods?**
3. **How can financial performance be improved while maintaining high service quality?**
4. **What are the key drivers of member engagement, and how can they be enhanced?**

---

## Dashboard Interactive

![Dashboard Overview](images/overview.png)

**Explore the interactive [Tableau dashboard](#) for a deeper dive into the AeroClub's operational analysis.**  
This dashboard includes filters to explore key metrics like fleet utilization, revenue breakdowns, and temporal trends.

---

## Fleet Utilization Analysis

### Insights
- **Fleet Composition and Utilization**:
  - **8 aircraft divided into 4 categories**:
    - **2 PS-28 (HSHH/HSHI)**: Primarily dedicated to training (66%).
    - **2 DA-40 (GUVU/HDAF)**: Versatile aircraft with high utilization.
    - **1 DA-40 NG (GNCY)**: Designed for travel purposes.
    - **1 A22 (74AJL)**: Ultralight aircraft (ULM) used for training.
    - **1 XL8 (JITQ), 1 PA-19 (BOMI)**: For specific purposes.
  - **Flight Hours**:
    - 75% of total flight hours are handled by DA-40 (HDAF, GUVU) and PS-28 aircraft.
    - Underutilized aircraft: XL8 (212 HDV) and BOMI (69 HDV).

![Fleet Utilization](images/repart_ressources.png)

- **Aircraft Roles**:
  - DA-40 NG (GNCY): Primarily used for advanced training, including CPL preparation, contributing 40% of its flight hours to professional qualifications.
  - PS-28: Critical for instruction, with 67% of hours dedicated to this activity.

### Recommendations
1. **Increase Utilization**:
   - Launch targeted campaigns promoting BOMI and XL8, emphasizing their unique capabilities.
2. **Dynamic Pricing**:
   - Introduce tiered pricing based on aircraft demand and time slots.
3. **Strategic Positioning**:
   - DA-40 NG should cater to pilots aiming for advanced certifications like IFR.

---

## Member Engagement and Activity

### Insights
- **Active Membership**:
  - 245 members flew in 2024, averaging 13 HDV per member.
  - 15 members contributed 22% of total flight hours, most of whom are students.
- **Instructional Impact**:
  - One instructor accounted for 16% of all instructional activity (220 HDV).

### Recommendations
1. **Loyalty Programs**:
   - Reward highly engaged members with discounted training hours.
2. **Event-Driven Engagement**:
   - Host off-season events or competitions to boost activity during low-demand months.
3. **Instructor Retention**:
   - Develop incentives for top-performing instructors to maintain high instructional standards.

---

## Temporal Trends and Seasonality

### Insights
- **Seasonal Peaks**:
  - Highest activity: July (363 HDV), August (339 HDV).
  - Lowest activity: December (73 HDV), primarily due to adverse weather conditions.
- **Daily Patterns**:

![Activity by Day](images/repart_days.png)

  - Saturdays dominate, with minimal activity on Tuesdays.
  - Underused time slots: 12 PM–2 PM.

![Activity by Time](images/repart_horaires.png)

### Recommendations
1. **Optimize Low-Demand Hours**:
   - Offer discounted flights or free discovery sessions during underutilized slots.
2. **Targeted Instruction**:
   - Schedule more training sessions during low-demand hours to optimize fleet usage.
3. **Limit Reservation Length**:
   - Restrict reservation duration on high-demand days like Saturdays to increase overall activity.

---

## Financial Performance

### Insights
- **Revenue Breakdown**:
  - DA-40 NG generates the highest revenue per flight (€221), while A22 AJL is the least profitable (€93).
  - Personal flights account for 53% of total revenue, and instruction makes up 47%.

![Revenue by Aircraft](images/repart_ressources_part.png)

### Recommendations
1. **Focus on Profitability**:
   - Reassess the viability of low-performing aircraft like BOMI and XL8.
2. **Boost Instruction Revenue**:
   - Introduce accelerated training programs during off-peak seasons.
3. **Cost Analysis**:
   - Evaluate detailed cost metrics, including maintenance and fuel costs.

---

## Data-Driven Projections and Scenarios

### Weather Analysis Summary
- **Data Source**: Historical weather data, focusing on rainfall and visibility.
- **Key Metrics**:
  - Average 8 rainy days/month in Haute-Savoie.
  - Operational efficiency estimated between **75% (pessimistic)** and **81% (optimistic)**.

### Scenarios
1. **Optimistic**:
   - Projected 2,950 HDV, assuming favorable weather conditions.
2. **Pessimistic**:
   - Projected 2,750 HDV, accounting for adverse conditions.

![Scenario Analysis](images/scenario.png)

---

## Challenges and Solutions

### Challenges Encountered
1. **Data Source Consistency**:
   - Issues integrating new months due to mismatched column names in CSV files.
   - Manual adjustments required for schema alignment.
2. **Limited Automation**:
   - Updates were manual, increasing the risk of errors.

### Proposed Solutions
1. **Centralized Data Repository**:
   - Maintain a structured folder hierarchy for raw and processed data.
2. **Intermediate Data Model**:
   - Use tools like Python or Alteryx for preprocessing and schema enforcement.
3. **Automation**:
   - Automate data updates with scripts or Tableau live connections.

---

## To Go Further

1. **Expand Financial Analysis**:
   - Incorporate detailed cost metrics to evaluate profit margins.
2. **Maintenance Impact**:
   - Assess how scheduled and unscheduled maintenance affects fleet availability and revenue.
3. **Geospatial Analysis**:
   - Add geospatial data to visualize flight patterns and destinations.
4. **Predictive Analytics**:
   - Build models to forecast member activity and operational demand.
5. **Member Insights**:
   - Conduct in-depth member segmentation to tailor services and promotions.

---

## Conclusion

This report highlights the key operational trends and offers a roadmap for strategic improvements at the Annecy AeroClub. By addressing current challenges and leveraging advanced data analytics, the AeroClub can achieve sustained growth while enhancing member satisfaction.

---

This revised version improves clarity, resolves formatting inconsistencies, and better emphasizes your analytical skills while maintaining a professional tone.
