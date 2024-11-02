# Insurance_Domain_PowerBI_Dashboard
## Project Overview
This report focuses on understanding the company’s customer base and revenue generation, tracking daily growth rates, and monitoring month-over-month policy changes to identify trends and improvement areas. We aim to segment customers by age group and analyze data by city and age to uncover key insights.

I worked on this project during my Virtual Internship in AtliQ Technologies.

[Live Report Link](https://app.powerbi.com/view?r=eyJrIjoiZmM2MTI5MDEtZDBjNy00MDYwLTk5NWMtNWIzZjdiMGQyODZjIiwidCI6ImM2ZTU0OWIzLTVmNDUtNDAzMi1hYWU5LWQ0MjQ0ZGM1YjJjNCJ9&pageName=2c73049311389a5d9268)

Visit My Presentation Video on LinkedIn -> <a href="https://www.linkedin.com/posts/atharvasutar_codebasicsvirtualinternship-activity-7258470950180900864-co5p?utm_source=share&utm_medium=member_desktop" target="blank"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/linked-in-alt.svg" alt="https://www.linkedin.com/feed/update/urn:li:activity:7243549037071609858/" height="30" width="40" /></a>

## Tools stacks
* PowerBi Desktop
* Excel
## PowerBI techniques Learnt
* What are all the questions that should be asked before starting the project
* Creating calculated columns
* Creating measures using the DAX language
* Data modeling
* Using Bookmarks to switch between two visuals
* Page navigation with buttons
* Using the divide function to prevent zero division errors
* Using KPIs
* Data validation techniques
* PowerBi services
* Publishing reports to PowerBi services
* Collaboration, workspace, and access permissions in PowerBi services
* And more 😅
## Business related terms
* Revenue
* Daily Revenue Growth
* Daily Customer Growth
* Net Invoice sale
* Revenue Change compared to last month
* Customer Change compared to last month
## Company’s Background
Shield Insurance is an Indian Insurance Company which operates across several cities in India, including Delhi NCR, Mumbai, Hyderabad, Indore, and Chennai. Each region provided unique customer insights, and understanding these regional variations was essential for identifying growth opportunities.

### Questions to ask before starting with the dashboard
* What is the objective of building this PowerBi dashboard?
* In what terms the success of this project will be measured?
* What will be the deadline for the project?
* Do the stakeholders expect a preview before the actual release?
* What are all the hopes stakeholders have out of this project?
* What are all the fears the stakeholders have in terms of building this dashboard?
* Who will be using this dashboard and for what purpose?
* What are all expectations the stakeholders have, by the completion of this project?
* What can go wrong while building this project?
* What are all the resources/ data needed to build this dashboard?
* Is there any input from stakeholders in terms of design and views of the dashboard?
After the project kick-off meetings, the data engineering team has given the data as per the request of the data analytics team, let’s explore them.

### Dataset Understanding
Understanding what data is available will be more helpful while doing analysis. before jumping on to the analysis get a good understanding of what are data available.

Dimension table: It will have static data like details of customers and products

Fact table: It will have the data about the transactions

  - dim_customer
    - This table contains all the information about the customers.
    - city: It is the city where the customer is present
    - customer code: Unique code is given to each customer
    - date of birth (dob): Customer's date of birth
  - dim_date
    - This table contains the dates at daily, monthly levels and week numbers of the year.
    - date: date at the daily level
    - day_type: weekday (Sunday, Monday, etc.)
    - mmm_yy: date at the monthly level
    - week_no: week number of the year as per the date column
  - dim_policies
    - This table contains all policies data.
    - policy_id: unique ID for a particular policy
    - base_coverage_amt(INR): base cover amount for that particular policy
    - base_premium_amt(INR): The premium amount that the customer has to pay to get the policy
  - fact_premiums
    - This table contains all information about policy orders.
    - customer_code: Unique code is given to each customer
    - policy_id: Unique ID for each policy
    - sales_mode: mode of the sales (Offline-Agent, Offline-Direct, Online-App, Online-Website)
    - final_premium_amt(INR): The premium amount that is paid for that policy by the customer
  - fact_settlements
    - age: Age of the policyholder
    - settlement% : Percent of policy settlements happend for this age 
## Importing Data into PowerBi
* As the datasets are in CSV format, so I imported the datasets from Excel to PowerBi by using Power Query.
## Data Model
* Data modeling plays a vital role and is considered as the basement of the report. All the visuals will be built upon the data model.
* Poor data modeling affects the overall performance of the report.
* Following Good practices of data modeling is a must. Refer to this page to get to know the good practices of Blog
* In this project, we have followed the Snowflake data modeling schema.
![Data Model](https://github.com/user-attachments/assets/fbd3d450-bfb2-4f37-a28c-f20883666884)


Dashboard designing
Based on the mock-ups received as required, the team will start designing the visuals and create measures as and when required.

Home view
In Home view, all the views button are available. Users will land on a specific view page by clicking the button

* Home Page
* Overall Analysis View
* Sales Mode Analysis View
* Age Group Analysis View

## Home Page
![Home Page](https://github.com/user-attachments/assets/3a5ab9ac-7b98-4f1e-ab3f-57e9e5009b0e)

## Overall Analysis View
![Overall Analysis View](https://github.com/user-attachments/assets/ef2749a4-d080-4523-aa80-702c9e2fa9e5)

## Sales Mode Analysis View
![Sales Mode Analysis View](https://github.com/user-attachments/assets/66abedca-1f1a-44dd-98bf-b21b62748b30)

## Age Group Analysis View
![Age Group Analysis View](https://github.com/user-attachments/assets/b6ba5c05-f54a-4071-9c25-5bd1fb45a560)

## Key Project Insights
1. Almost 41% of the revenue generates from Delhi NCR region followed by Mumbai and Hyderabad.
2. Huge chunk of customers come from 31-40 age group segment.
3. A large surge in revenue and customer on-boarding is seen in the month of March.
4. Almost 148 customers are on-boarded and 5.47 Million revenue is generated daily. 
