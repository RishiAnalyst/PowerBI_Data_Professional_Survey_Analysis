# Data Professionals Survey Analysis with Power BI
### Power BI Report: https://app.powerbi.com/view?r=eyJrIjoiZTk3Yzk3MGQtMjFkMi00MmZhLWEzOTktZTg4Y2U1MjgwOWZiIiwidCI6IjlmMzA5MDY2LTU1Y2YtNDQ4NS04N2Q0LWViNTljZDdiYzY4NCJ9
## Project Overview
The data professional survey analysis project aimed to explore the key aspects of the data industry by examining survey responses. This analysis focused on understanding how factors like age, gender, education, and work experience shape the career paths and satisfaction levels of data professionals. By leveraging the visualization capabilities of Power BI, the project presented clear and impactful insights, helping to uncover trends in salary distribution, popular programming tools, and career transitions within the data field.

## Objectives
### The primary objectives of this project were to:

1. Explore the demographics and characteristics of data professionals.
2. Analyze career satisfaction, including salary and work-life balance.
3. Identify trends in programming language preferences and career switching within the data industry.
## Steps Involved
### Data Importation:
Imported survey data into Power Query for cleaning and transformation.
### Data Cleaning and Processing

For this project, **Power Query** was used for data cleaning and preprocessing to ensure accuracy and relevance. The original table had 28 columns before the cleaning process. Below are the steps performed:

#### 1. Removed Blank Rows  
- Removed 6 columns with empty rows such as **"Email," "Browser," "OS," "City," "Country," "Referrer"** and other unwanted columns like **"Time Taken (America/New_York)"** and **"Time Spent."**

![Blank colms](https://github.com/user-attachments/assets/a22ed50c-c9ca-4c7d-8246-65473a8d7dd7)

#### 2. Handled Null Values  
- In the **"Highest Level of Education"** column, replaced null values with **"Others"** instead of leaving them as empty cells.

#### 3. Split Columns and Cleaned Data  
- Split the following columns by delimiter:  
  - **"Current Role"**  
  - **"Industry"**  
  - **"Favorite Programming Language"**  
  - **"Preference About the New Job"**  
  - **"Country"**  
  - **"Ethnicity"**  
- Deleted the second unwanted column that  that Exceeded part from the cell values ( Other ),

 ![others 1](https://github.com/user-attachments/assets/e589ffee-0ad8-4c59-8ad7-c45a4bd492bb)
 
- Replaced **"Student/Looking/None"** values with **"Other"**, as they were not important for analysis.

#### 4. Processed Salary Column  
- The **"Current Yearly Salary"** column contained salary ranges (e.g., **"0 – 40k"**). To calculate the average salary:  
  1. Split the column by delimiter to isolate numbers.  
  2. Removed unnecessary characters (e.g., **"k"**).  
  3. Created a custom column to calculate the average salary:  
     ``` 
     (["Current Yearly Salary"] + ["Current Yearly Salary"]) / 2 
     ```
  4. Removed the original columns and retained the average salary column.

![Picture1](https://github.com/user-attachments/assets/23afc228-9a2e-40af-93f9-6691d27e8daf)

![Picture2](https://github.com/user-attachments/assets/a4acd150-1605-4617-8565-0fb5fc7fef73)

#### 5. Converted Salary to Thousands  
- Created a new custom column to convert the average salary into thousands:
     ```
   ["Average Salary($)"]*1000) 
     ```
![Picture3](https://github.com/user-attachments/assets/3170a0c1-3f3d-4145-bb26-488086a4fde3)

### Visualization:
Created interactive Dashboard with 10 visualizations 2 cards and Navigations in Power BI to present the findings in a clear and informative manner. Slicers was not necessary that all the visualisation was enough to filter down according to our need.

## Key Insights
### Salary Analysis
1. Data Scientists Lead in Salary: Among the survey respondents, data scientists are the highest earners, indicating a high demand and value for this role in the industry.


![datapro-1](https://github.com/user-attachments/assets/eb3451f0-0d76-4dad-8031-88b4377c72f1)

2. Higher Qualifications Correlate with Higher Salaries: Respondents with a PhD earn more on average than those with lower qualifications, highlighting the value of advanced education in the data field.

 ![datapro-2](https://github.com/user-attachments/assets/69fba351-bf6c-499d-9df0-80d03aa40e9d)
 
3. Gender Salary Disparity: Interestingly, the survey data shows that, on average, female data professionals are earning more than their male counterparts, which could indicate a shift towards more equitable pay.

 ![datapro-4](https://github.com/user-attachments/assets/881ed9b0-b0d2-4ab3-943e-cae7fd4fc99a)

### Programming Language Preference
Python as the Preferred Language: Python emerged as the favorite programming language among the majority of survey participants, reflecting its popularity and widespread use in data analysis and machine learning.

![datapro-3](https://github.com/user-attachments/assets/e2d3334c-71ef-48d1-85d9-64964c7b0e11)

### Career Switching Trends
Transition into Data Roles: A significant number of respondents have switched to data roles from different careers, suggesting the growing appeal of data-related professions across various backgrounds.

![datapro-5](https://github.com/user-attachments/assets/e9fe3f7a-d887-4514-9008-98481d22c3d5)

## Other Insights
### Happiness Index

![Screenshot (182)](https://github.com/user-attachments/assets/ca390016-e27c-409a-b158-f69292902c09)

1. Salary Satisfaction: The average happiness index for salary in the current role is below 5 out of 10, indicating room for improvement in compensation satisfaction among data professionals.
2. Work-Life Balance: The average happiness index for work-life balance is around 5 out of 10, suggesting that balancing work demands with personal life remains a challenge for many in the field.
3. Management Satisfaction: The average happiness index for the Management is also around 5 out of 10 indicate there is room for improvement for the management.
## Conclusion
The analysis provides a valuable overview of the current state of the data profession, highlighting key trends and areas for improvement. Key takeaways include the prominence of Python, the financial benefits of higher qualifications, and the encouraging trend of career switches into data roles. However, there is a need for better salary satisfaction, work-life balance among data professionals and Management employer relationship.





