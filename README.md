
# CALL CENTER ANALYTICS PROJECT

## PROJECT DESCRIPTION
   This project aims to optimize call center operations by leveraging data analytics to enhance efficiency, improve customer satisfaction and reduce
   operational costs. By analyzing key performance metrics, customer interactions and agent performance, the project will provide actionable insights
   to drive data-informed decision-making.

### SOFTWARE USED
    * Excel
    * Power Bi

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

### VISUALIZATION
    * Step 13: Most Common Call Issues Per Day <Stacked Bar Chart>
                Refers to the reasons for calls that occur most frequently on a given day. It involves categorizing calls and determining which
                category has the highest volume each day. This helps to identify daily patterns, priortize resources and address recurring problems.
 <img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/309cd0db-5761-444b-80b9-6c67bef8e476" />

    * Step 14: Customer Satisfaction by Agent <Clustered Bar Chart>
                This is a metric that measures how satisfied customers are with the service provided by individual call center agents. This metric
                helps evaluate agent performance, identify training needs and improve customer experience.
 <img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/10c47c45-c165-47e6-b3ce-3650e350db0e" />

    * Step 15: Number of Calls handled per agent <Stacked Bar Chart>
                Is the total count of calls (incoming, outgoing or both) managed by an individual agent over a defined period.
                This metric measures agent workload and productivity, helping managers assess performance, balance schedules and optimize operations.
 <img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/20275828-1dc8-4865-a936-2af696fd39cc" />

    * Step 16: Common Call Issues <Stacked Column Chart>
                Are the most frequent reasons customers initiate calls to a support center. Identifying these helps businesses priortize resources,
                improve processes and enhance customer satisfaction.
 <img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/0c7c7bef-291b-455b-9e00-b7dd587a912b" />

    * Step 17: Total Calls Per Month <Line Chart>
                Refers to the aggregate number number of calls made, received or handled within a month. This metric is often used to measure activity 
                levels, assess performance in industries like telecommunications, customer support.
 <img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/bb97fb1f-8e77-4741-a7bf-ad26b6d681ba" />
     
    * Step 18: Resolution rate by issue <Donut Chart>
                Is a performance metric that calculates the percentage of issues that are successfully resolved within a given period.This metric helps
                identify how effectively different issues are being handled, revealing strenghts or weaknesses in processes,teams or systems.
 <img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/515d5e9e-9ccc-445f-a2b1-8a9b2a55665b" />

    * Step 19: Total Calls per Day <Line Chart>
                Is the sum of all calls handled within a single day. It helps track daily call volume to identify patterns,manage operations or assess
                performance.
 <img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/95f329ea-cc60-40e1-adb2-ef48ae3a6282" />

### ADD INTERACTIVITY WITH SLICER
    1. Select the slicer visual: In the visualizations pane (on the right), click the slicer icon. This adds a blank slicer to your report canvas.
    2. Add a field to the slicer: In the fields pane, locate the dataset and drag the field you want to filter(Month and Agent) into the values 
       area of the slicer.
    3. Resize and format the slicers to control user interactions.

### KEY INSIGHTS
    * Agent workload distribution affects productivity
        Agent Jim handled the most calls(536) followed by Agent Dan(523) and Agent Becky(517), balance workload to avoid over-burdening agents like
        Agent Jim and Agent Dan most especially on  high-volumn days.
  
    * Customer Satisfaction by Agents
        Agent Jim has the highest CSAT(1819), followed by Agent Dan(1803), Agent Joe lower CSAT may tie to handling more technical issues.
        Pair Agent Joe with simpler issues or provide technical training to improve satisfaction.
 
### CONCLUSION
    This analysis reveals a clear picture of operational dynamics, highlighting opportunities to enhance efficiency, customer satisfaction and agent
    performance.The visualizations and underlying data are accessible via the 
 <img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/a9b482bd-570d-4ff6-8287-e89d2918d143" />

     
    
        
    

