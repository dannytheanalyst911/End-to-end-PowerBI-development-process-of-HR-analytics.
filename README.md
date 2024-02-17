# End-to-end PowerBI development process of HR analytics.
My client Atlas Labs would like to create a new report to help track their HR analytics.

STEPS:
![step1](https://github.com/dannytheanalyst911/End-to-end-PowerBI-development-process-of-HR-analytics./assets/107795987/024047eb-6192-43ac-b9a7-a9f9e6290c36)

Loading datasets from CSV files, matching expected data formatting for columns, changing table names based on role (Fact or Dimension table).

Create a DimDate table for better accuracy date and time in reporting, using DAX code in DimDate.txt

This is the relationship diagram after modeling:

![image](https://github.com/dannytheanalyst911/End-to-end-PowerBI-development-process-of-HR-analytics./assets/107795987/c562151b-5f4e-4973-bb55-daeb97c5b1cc)

Calculate key measures of Employee using DAX:

![image](https://github.com/dannytheanalyst911/End-to-end-PowerBI-development-process-of-HR-analytics./assets/107795987/39b0d2cf-16f3-4eae-9cf4-8c7985df3c42)


Visualize Employee Hiring Trends, use USERELATIONSHIP() to activate the relationship between DimEmployee and DimDate:

![image](https://github.com/dannytheanalyst911/End-to-end-PowerBI-development-process-of-HR-analytics./assets/107795987/b25b789e-d7e8-4089-a46c-1bfe92498393)

Visualise Active Employees by Department and Job Role with a bar chart and treemap, unveiling insight that the biggest department at Atlas is Technology (828 people) and Software Engineer is the most popular Job Role (247):

![image](https://github.com/dannytheanalyst911/End-to-end-PowerBI-development-process-of-HR-analytics./assets/107795987/1b679365-276f-43c7-aae5-0699cd942331)

![image](https://github.com/dannytheanalyst911/End-to-end-PowerBI-development-process-of-HR-analytics./assets/107795987/b6e5eebc-ca0c-4e09-ad4c-de8a61fd48e4)

Next, I dive deeper into the demographics of Employees, such as Age and Gender. First, I display 2 cards showing the age of the youngest and the oldest employee.

![image](https://github.com/dannytheanalyst911/End-to-end-PowerBI-development-process-of-HR-analytics./assets/107795987/a9aedb1a-d737-46b2-bfe1-e1127f93a8ee)

I want to know the number of employees broken down by age bins, so I created a conditional column called AgeBins in Power Query:

![image](https://github.com/dannytheanalyst911/End-to-end-PowerBI-development-process-of-HR-analytics./assets/107795987/b4b6f77c-8ae4-4782-b7e1-7cd18243bdce)

Then 2 columns charts to show Employees by Age and Employees by Age and Gender.

![image](https://github.com/dannytheanalyst911/End-to-end-PowerBI-development-process-of-HR-analytics./assets/107795987/ebfef1cc-7947-4c15-aed8-51d5a7801bc4)

![image](https://github.com/dannytheanalyst911/End-to-end-PowerBI-development-process-of-HR-analytics./assets/107795987/1b64f937-5024-4cf1-8d67-2d56c2f5665b)

Add a pie chart to show Employees by Marital Status:

![image](https://github.com/dannytheanalyst911/End-to-end-PowerBI-development-process-of-HR-analytics./assets/107795987/904119cf-bfd0-4f26-b3c1-772e133eb3b4)

Then a combination of line and bar chart to demonstrate Employees by Employees and Average Salary by Ethnicity:

![image](https://github.com/dannytheanalyst911/End-to-end-PowerBI-development-process-of-HR-analytics./assets/107795987/64991b82-dcb6-4e43-ad9c-8349f46c515f)

Create Performance Tracker by each individual Employee, first show their Start date, Last Review and Next Review ( if there was no review yet, next review will be 1 year from Start Date).

![image](https://github.com/dannytheanalyst911/End-to-end-PowerBI-development-process-of-HR-analytics./assets/107795987/d4dc73b1-9d77-4269-ba25-7f8fac898b72)

