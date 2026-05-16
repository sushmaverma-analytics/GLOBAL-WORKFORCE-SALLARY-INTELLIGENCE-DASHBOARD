# GLOBAL-WORKFORCE-SALLARY-INTELLIGENCE-DASHBOARD
GLOBAL WORKFORCE SALLARY INTELLIGENCE DASHBOARD
## Project-overview
-This Powern BI Project analyzes workforce Salary trends across industries, company sizes, Job roles, experience levels, skills, certifications, Education and remote work models.
## Feaatures
-Interactive KPI Dashboard for workforce salary analysis
-Salary comparison by industry, company size, and work mode
-Top 5 highest salary job role analysis
-Employee distribution analysis across job roles
-Average salary analysis using DAX measures
-Bookmark Navigation for enhanced user experience
-Selection Pane for dynamic visual interaction
-Matrix Visual for detailed workforce comparison
-Q&A Visual for natural language querying
-Row-Level Security (RLS) using Manage Roles
-Dynamic slicers and filtering functionality
-Remote, Hybrid, and Onsite work analysis
-Skills and certification impact analysis
-Industry-wise and company-wise salary insights
-Clear All Slicer button for interactive dashboard reset
-Business storytelling using interactive visualizations
##Tools Used
- Power BI Dessktop
- CSV
- Power Query
- DAX
- Data Modeling
- ## Data Modeling
- A star schema data model was implemented to improve report performance, maintain data consistency, and enable efficient analytical reporting.

-Fact Table
-Fact_Salary

-The fact table contains workforce salary-related information such as:

-Salary
-Experience Years
-Skills Count
-Certifications
-Job Titles
-Industry
-Company Size
-Remote Work Mode
-Education Level
-Dimension Tables

-The following dimension tables were created for optimized filtering and analysis:

-Dim_Job_Title
-Dim_Industry
-Dim_Company_Size
-Dim_Remote_Work
-Dim_Education_Level
-Relationships

-One-to-many relationships were established between dimension tables and the fact table to support interactive filtering and dynamic analysis.

-Data Modeling Benefits
-Improved dashboard performance
-Reduced data redundancy
-Efficient DAX calculations
-Better scalability and report organization
-Enhanced interactive analysis across multiple dimensions
## DAX Measures
-Average Salary
Average Salary = AVERAGE(Fact_Salary[salary])
-Total Employees
Total Employees = COUNTROWS(Fact_Salary)
-Highest Salary
Highest Salary = MAX(Fact_Salary[salary])
-Certified Employees
Certified Employees =
CALCULATE(
    COUNTROWS(Fact_Salary),
    Fact_Salary[certifications] > 0
)
-Large Company Avg Salary
Large Company Avg Salary =
CALCULATE(
    [Average Salary],
    Fact_Salary[company_size] = "Large"
)
## Business Insights
-Salaries vary significantly across industries, with Technology and Finance offering the highest compensation.
-Experience level strongly impacts salary, with senior professionals earning substantially more than entry-level roles.
-Company size influences pay, where large organizations generally provide higher salary packages.
-Job roles and skill sets create noticeable salary differences, highlighting demand for specialized skills.
-Remote and hybrid work patterns show slight variations in compensation trends across roles.
## Dashboard Preview
![Uploading Screenshot 2026-05-16 043719.png…]()


