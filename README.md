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

Visualise Active Employees by Department and Job Role with bar chart and treemap, unveiling insight that the biggest department at Atlas is Technology (828 people) and Software Engineer is the most popular Job Role (247):

![image](https://github.com/dannytheanalyst911/End-to-end-PowerBI-development-process-of-HR-analytics./assets/107795987/1b679365-276f-43c7-aae5-0699cd942331)

![image](https://github.com/dannytheanalyst911/End-to-end-PowerBI-development-process-of-HR-analytics./assets/107795987/b6e5eebc-ca0c-4e09-ad4c-de8a61fd48e4)
