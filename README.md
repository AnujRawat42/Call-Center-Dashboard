# Call Centre Dataset -Dashboard

### Dashboard Link : https://app.powerbi.com/view?r=eyJrIjoiMWYwNDE3OWQtNDEzMC00NzUzLTgxNGItOTY4NDNjMDJlZWJlIiwidCI6IjE1NTE1N2M3LTc5MzUtNDkxYi04OWQxLWY5NTJhYWQ1YzYwOSJ9

## Problem Statement

The management team requires a comprehensive Power BI dashboard that visualizes key performance indicators (KPIs) and metrics critical to the center’s operational efficiency and customer satisfaction. The dashboard should offer clear insights into overall customer satisfaction, call handling efficiency, and agent performance. The goal is to provide actionable data that helps improve service quality, optimize resource allocation, and enhance decision-making.
Here is the [DATA FILE](https://drive.google.com/drive/folders/16E-EZy_nZsLDDi8aMrjlHC5IK7icSgMa?usp=drive_link)

## Key KPIs

- **Customer Satisfaction**: Measuring overall customer experience.
- **Call Handling Metrics**: Total calls answered vs. abandoned, categorized by time.
- **Operational Efficiency**: Average speed of answer, call duration, and peak call times.
- **Agent Performance**: Analyzing agent effectiveness using a quadrant view of average handle time (talk duration) vs. calls answered.



### Steps followed 

### 1. Data Preparation
- Loaded the call center dataset into Power Query.
- Checked the column distribution to understand data structure and quality.

### 2. Measure Creation
- Created a measure for answered calls:
  ```DAX
  Answered = CALCULATE(COUNT(Sheet1[Call Id]), FILTER(Sheet1, Sheet1[Answered (Y/N)] = "Y"))
- Created a measure for resolved calls:
    ```DAX
  Resolved(Y) = CALCULATE(COUNT(Sheet1[Call Id]), FILTER(Sheet1, Sheet1[Resolved] = "Y"))
### 3. Dashboard Visuals
- **Gauge**: Displayed the average satisfaction rating of agents.
- **Column Chart**: Visualized the number of calls per month.

### 4. Agent Statistics
- **Table**: Showed detailed statistics for each agent, including:
  - Number of resolved calls
  - Number of answered calls
  - Performance ratings


# Key Insights from the Dashboard



1. **Jim** was the top performer in terms of call volume, answering a total of **536 calls** with **485 resolved**.

2. **Stewart** achieved the highest customer satisfaction rating, with a score of **3.40**.

3. The overall **Speed of Answer (SOA)** was recorded at **67.52**, indicating the average time taken to respond to calls.

4. **January** experienced the highest volume of answered calls, highlighting it as the peak month for call activity.

5. A **dropdown filter** is available to analyze employee performance across different call topics, including:
   - **Admin support**
   - **Contact related**
   - **Payment related**
   - **Streaming**
   - **Technical support**

## Snapshot of the dashboard
![Screenshot 2024-08-23 154000](https://github.com/user-attachments/assets/15b0f777-6f1a-4337-8286-654a6e65a2fa)
