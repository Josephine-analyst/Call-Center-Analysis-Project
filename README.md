
# CALL CENTER ANALYTICS PROJECT

## PROJECT DESCRIPTION
   This project aims to optimize call center operations by leveraging data analytics to enhance efficiency, improve customer satisfaction and reduce operational costs. By analyzing key performance metrics, customer interactions and agent performance, the project will provide actionable insights to drive data-informed decision-making.
   
 ![Main Dashboard Overview](Screenshot%20(63).png)](Screenshot%20(63).png)

### BUSINESS OBJECTIVES
    Transform raw call center data into actionable insights to:
    - Optimize agent workload distribution
    - Improve first-contact resolution rates
    - Increase overall customer satisfaction
    - Identify training needs and peak call patterns
    - Reduce operational costs through better resource planning

### TECHNOLOGY & TOOLS USED
    - **Data Source** — Excel (.xlsx)
    - **Data Transformation** — Power Query
    - **Modeling** — DAX (measures + calculated date table)
    - **Visualization** — Power BI Desktop
    - **Interactivity** — Slicers (Agent, Month)


### STEPS FOLLOWED:
    * Step 1: Load data into power bi desktop, dataset is an xlsx file.
    * Step 2: Open the power query editor to check for duplicates, empty cells and missing values.
    * Step 3: Remove duplicates, empty cells and fill up missing values using the fill up & down option (fill with averages).
    * Step 4: Click on the close & apply button on the menu bar to close the power query editor window and apply any pending changes.

### ADD CALCULATED TABLE
    * Step 5: Using the Date column from the dataset to create a date table
               - DATE TABLE = CALENDARAUTO()

    * Step 6: Extracting the month and day from the Date Table
               - MONTH = FORMAT('DATE TABLE'[Date],"MMMM")
               - DAY = FORMAT('DATE TABLE'[Date],"DDDD")
               - YEAR = YEAR('DATE TABLE'[Date])

### USE DAX(DATA ANALYSIS EXPRESSION) TO CREATE MEASURES FOR KEY METRICS, SUCH AS:
    * Step 7: TOTAL CALLS RECEIVED = COUNT(Sheet1[Call Id])

    * Step 8: AVERAGE CALLS DURATION = AVERAGE(Sheet1[Speed of answer in seconds])

    * Step 9: AVERAGE CSAT RATING = AVERAGE(Sheet1[Satisfaction rating])

    * Step 10: TOTAL CALLS DURATION = SUM(Sheet1[Speed of answer in seconds])

    * Step 11: RESOLVED CALLS = COUNTROWS(FILTER('Sheet1','Sheet1'[Resolved]="Y"))

    * Step 12: UNRESOLVED CALLS = COUNTROWS(FILTER('Sheet1','Sheet1'[Resolved]="N"))

## 🔍 Key Metrics & Visuals

| Metric                        | Visualization Type       | Business Question Answered                              |
|-------------------------------|--------------------------|------------------------------------------------------------------|
| Total Calls Received          | KPI Card                 | What is the overall call volume?                                 |
| Calls per Agent               | Stacked Bar              | Who handles the most calls? (Workload balance)                   |
| CSAT by Agent                 | Clustered Bar            | Which agents deliver the best customer experience?               |
| Most Common Call Issues       | Stacked Column           | What are customers calling about most often?                     |
| Common Issues per Day         | Stacked Bar              | Are certain issues spiking on specific days?                     |
| Resolution Rate by Issue      | Donut                    | Which issue types are resolved most/least effectively?           |
| Calls per Month / per Day     | Line                     | What are the seasonal / daily patterns?                          |

### VISUALIZATION
    * Step 13: Most Common Call Issues Per Day <Stacked Bar Chart>
               Refers to the reasons for calls that occur most frequently on a given day. It involves categorizing calls and determining which category has the highest volume each day. This helps to identify daily patterns, priortize resources and address recurring problems.
 <img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/309cd0db-5761-444b-80b9-6c67bef8e476" />

    * Step 14: Customer Satisfaction by Agent <Clustered Bar Chart>
               This is a metric that measures how satisfied customers are with the service provided by individual call center agents. This metric helps evaluate agent performance, identify training needs and improve customer experience.
 <img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/10c47c45-c165-47e6-b3ce-3650e350db0e" />

    * Step 15: Number of Calls handled per agent <Stacked Bar Chart>
               Is the total count of calls (incoming, outgoing or both) managed by an individual agent over a defined period.
               This metric measures agent workload and productivity, helping managers assess performance, balance schedules and optimize operations.
 <img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/20275828-1dc8-4865-a936-2af696fd39cc" />

    * Step 16: Common Call Issues <Stacked Column Chart>
               Are the most frequent reasons customers initiate calls to a support center. Identifying these helps businesses priortize resources,improve processes and enhance customer satisfaction.
 <img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/0c7c7bef-291b-455b-9e00-b7dd587a912b" />

    * Step 17: Total Calls Per Month <Line Chart>
               Refers to the aggregate number number of calls made, received or handled within a month. This metric is often used to measure activity levels, assess performance in industries like telecommunications, customer support.
 <img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/bb97fb1f-8e77-4741-a7bf-ad26b6d681ba" />
     
    * Step 18: Resolution rate by issue <Donut Chart>
               Is a performance metric that calculates the percentage of issues that are successfully resolved within a given period.This metric helps identify how effectively different issues are being handled, revealing strenghts or weaknesses in processes,teams or systems.
 <img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/515d5e9e-9ccc-445f-a2b1-8a9b2a55665b" />

    * Step 19: Total Calls per Day <Line Chart>
               Is the sum of all calls handled within a single day. It helps track daily call volume to identify patterns,manage operations or assess performance.
 <img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/95f329ea-cc60-40e1-adb2-ef48ae3a6282" />

### ADD INTERACTIVITY WITH SLICER
    1. Select the slicer visual: In the visualizations pane (on the right), click the slicer icon. This adds a blank slicer to your report canvas.
    2. Add a field to the slicer: In the fields pane, locate the dataset and drag the field you want to filter(Month and Agent) into the values 
       area of the slicer.
    3. Resize and format the slicers to control user interactions.

### KEY INSIGHTS
    1. **Workload Imbalance**  
         Agent **Jim** handled the highest volume (536 calls), followed closely by **Dan** (523) and **Becky** (517).  
         → Consider redistributing high-volume shifts or adding support staff.

    2. **CSAT Performance**  
         - **Jim** → highest total CSAT score (1819)  
         - **Joe** → noticeably lower satisfaction → likely due to higher share of technical issues  
         → Recommendation: Targeted technical training for Joe + route simpler issues to him temporarily.

    3. **Top Call Drivers**  
         Technical Support and Payment Issues dominate → highest volume and mixed resolution rates.  
         → Process/documentation improvements in these areas could yield quick wins.

    4. **Resolution Effectiveness**  
         Significant variation by issue type — some categories show < 60% first-contact resolution.  
         → Prioritize root-cause analysis on low-resolution issues.

   ## 🚀 How to Explore the Dashboard

         1. Clone the repository
         ```bash
         git clone https://github.com/Josephine-analyst/Call-Center-Analysis-Project.git

        2. Open CALL CENTER ANALYSIS PROJECT.pbix in Power BI Desktop
        3. If data doesn't load automatically:
        4. Go to Home → Transform data
        5. Update the source path to point to data/call-center-data.xlsx (recommended to add this file)
        6. Use the Agent and Month slicers to filter interactively

 
   ### CONCLUSION
       This analysis reveals a clear picture of operational dynamics, highlighting opportunities to enhance efficiency, customer satisfaction and agent performance.The visualizations and underlying data are accessible via the 
    
 <img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/a9b482bd-570d-4ff6-8287-e89d2918d143" />

     
    
        
    

