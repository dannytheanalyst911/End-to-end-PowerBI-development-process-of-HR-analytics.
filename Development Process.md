# End-to-end PowerBI development process of HR analytics.
My client Atlas Labs would like to create a new report to help track their HR analytics.

STEPS:
![step1](https://github.com/dannytheanalyst911/End-to-end-PowerBI-development-process-of-HR-analytics./assets/107795987/024047eb-6192-43ac-b9a7-a9f9e6290c36)

## Loading data

Loading datasets from CSV files, matching expected data formatting for columns, changing table names based on role (Fact or Dimension table).

Create a DimDate table for better accuracy date and time in reporting, using DAX code in DimDate.txt

This is the relationship diagram after modeling:

![image](https://github.com/dannytheanalyst911/End-to-end-PowerBI-development-process-of-HR-analytics./assets/107795987/c562151b-5f4e-4973-bb55-daeb97c5b1cc)

## Construct cards and visuals

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

Create a Performance Tracker for each Employee, show their Start date, Last Review and Next Review ( if there was no review yet, next review will be 1 year from Start Date).

![image](https://github.com/dannytheanalyst911/End-to-end-PowerBI-development-process-of-HR-analytics./assets/107795987/d4dc73b1-9d77-4269-ba25-7f8fac898b72)

Breakdown their satisfied level by year, also include the difference between Seft Rating and Manager Rating:

![image](https://github.com/dannytheanalyst911/End-to-end-PowerBI-development-process-of-HR-analytics./assets/107795987/dbeb59d7-02ce-459c-862a-e3826030cb56)

Next, let's dive deeper into the attrition rate of the company, starting with the overall Attrition Rate and break down by Department and Job Role:

![image](https://github.com/dannytheanalyst911/End-to-end-PowerBI-development-process-of-HR-analytics./assets/107795987/a9cd994d-2e80-4e2f-bcbc-f284226426b4)

The attrition rate by Hire Date is also a good measure that needs to be included in our report. First, we need to activate the relationship between the Hire Date from DimEmployee and the Date column from DimDate using USERELATIONSHIP() in the DAX editor.

![image](https://github.com/dannytheanalyst911/End-to-end-PowerBI-development-process-of-HR-analytics./assets/107795987/d8c2d0e9-6423-427f-973f-8566a6112993)

![image](https://github.com/dannytheanalyst911/End-to-end-PowerBI-development-process-of-HR-analytics./assets/107795987/6f20fd45-f5f1-4b2f-8b03-b51167613dff)

Let's take into account other factors that can impact the Attrition Rate, which are Travel frequency, Overtime and Tenure (Years of working in Atlas):

![image](https://github.com/dannytheanalyst911/End-to-end-PowerBI-development-process-of-HR-analytics./assets/107795987/1b0686d5-c132-44d8-843e-5445d71183ef)

![image](https://github.com/dannytheanalyst911/End-to-end-PowerBI-development-process-of-HR-analytics./assets/107795987/b8de0f2a-f260-45fd-bc20-a8a6569d1b10)

![image](https://github.com/dannytheanalyst911/End-to-end-PowerBI-development-process-of-HR-analytics./assets/107795987/82b016a0-8fbb-4b2b-8244-cfd90ecf6cad)

## Layout design

Now it's time to arrange the card and customize the theme, I found this interesting [color palette](https://www.color-hex.com/color-palette/1040017), so let's apply it to the report.

### Overview
![image](https://github.com/dannytheanalyst911/End-to-end-PowerBI-development-process-of-HR-analytics./assets/107795987/9a77d48c-ed2f-4a28-88bf-8323269252c6)

- There is a total of 1470 employees at Atlas Labs, which 1233 (83,8%) is active.
- The biggest department is Technology with 838 employees, and HR is the least with only 51 people.
- Software Engineer and Data Scientist is the most popular job at Atlas.

### Demographics
![image](https://github.com/dannytheanalyst911/End-to-end-PowerBI-development-process-of-HR-analytics./assets/107795987/2aae8a94-4a10-4a8c-846c-a688bfd9e8e0)

- Employees' age varies from 18 to 51, with the biggest portions in 20-29 age bins, followed by U40 and U50. Atlas has a pretty young workforce since it is a tech map firm.
- The gender breakdown is quite equal between men and women, and there is about 10% identified as others, so there is no evidence of gender inequality when hiring for the position.
- Married is the most popular among employees status with 42,45%, while the divorced rate is quite high, standing at 20,2%.
- White people make up most of Atlas's workforce (about 60%), and they are the highest-paid group.
- There are only 16 minority employees and they are reported to have the lowest salary, with an average of just a little bit more than $100k a year, still a good salary in the market. Atlas Labs has a pretty fair compensation package.
### Performance Tracker
![image](https://github.com/dannytheanalyst911/End-to-end-PowerBI-development-process-of-HR-analytics./assets/107795987/581eb4bb-182a-4624-ab38-049cece9c30c)

- We can see individual employee stats by selecting the name, as well as when they get hired, last and next date of review.
- For example, employee Estelle Chung has job satisfaction decreased by year, and in the last review, he stated himself as meeting expectations, but the manager thinks he needs improvement. The HR department needs to discuss with him what was happening and resolve the issue.
### Attrition
![image](https://github.com/dannytheanalyst911/End-to-end-PowerBI-development-process-of-HR-analytics./assets/107795987/06ef204c-fd35-4be7-8f54-93fcdbbf93e7)

- The overall Attrition rate is 16.1%.
- Sales Representatives is the fastest-changing position with almost 40%, while Engineer Manager tends to stay within the company with only 2.7% attrition.
- Employees tend to hold on to their jobs at the beginning of the year and quit when Christmas comes, due to the attrition rate growing substantially from Q1 to Q4. Further investigations need to be done to find out why.
- Most of the employees(1043) are doing some business travel, and the one who goes on business trips frequently tends to quit more than others.
- People required to work overtime are likely to quit 3 times more than the ones who don't (30% vs 10%). Atlas may need to work on the company's overtime policy if it wants to fix this problem.
- Last but not least, seniors are less likely to quit than freshers.
