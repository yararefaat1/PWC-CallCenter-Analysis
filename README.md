# PWC-CallCenter-Analysis
CallCenter Power BI Analysis
Overview
This repository contains the Power BI report analyzing call center performance data. The report is designed to provide insights into key metrics such as call volume, average handling time, customer satisfaction, and more. The analysis includes various visualizations and custom measures to help stakeholders understand and improve call center operations.

Features
Interactive Dashboards: Multiple dashboards providing an overview and detailed analysis of the call center's performance.
Custom Measures: Tailored calculations to accurately measure key performance indicators (KPIs).
Dynamic Filtering: Ability to filter data based on various criteria like date, agent, call type, etc.
Visualizations: A variety of visualizations, including bar charts, line charts, and tables, to represent the data effectively.
Measures Used
Below is a list of the key custom measures used in the report:

Total Calls:

Total Calls = COUNT(CallCenter[CallID])
Description: This measure counts the total number of calls handled by the call center.
Average Handling Time (AHT):

Average Handling Time = AVERAGE(CallCenter[HandlingTime])
Description: Calculates the average time spent handling each call.
Customer Satisfaction Score (CSAT):

CSAT Score = AVERAGE(CallCenter[SatisfactionScore])
Description: Calculates the average satisfaction score provided by customers after their interaction.
Calls Answered within SLA:

Calls within SLA = CALCULATE(COUNT(CallCenter[CallID]), CallCenter[HandlingTime] <= SLA[TimeLimit])
Description: Counts the number of calls answered within the Service Level Agreement (SLA) time.
Agent Performance Index:

Agent Performance = [Total Calls] / [Average Handling Time]
Description: A composite index to evaluate agent performance based on the number of calls handled and the average handling time.
Customizations
The following customizations have been applied to enhance the report:

Custom Date Slicer:

A custom slicer is used to filter data based on specific time periods (days, weeks, months).
Conditional Formatting:

Applied to the CSAT Score to highlight scores below a certain threshold in red and above the threshold in green.
Drill-Through Feature:

Implemented drill-through options to enable users to go from a summary view to detailed data for individual agents or specific time periods.
Calculated Columns:

Call Duration Category = IF(CallCenter[HandlingTime] <= 5, "Short", IF(CallCenter[HandlingTime] <= 10, "Medium", "Long"))
Description: Categorizes calls into short, medium, or long duration based on handling time.
Custom Tooltip Pages:

Custom tooltip pages are created to provide additional context when hovering over data points, such as showing a breakdown of call types for each agent.

You Can Freely Interact with the DAshboard on :
https://tinyurl.com/2yym25mh
