# gagandeep-ucw-2318246
This repository contains several projects created on AWS platform as part of my MBA - Cloud Computing course.

# 1. Descriptive Analysis
**Project Description**: Descriptive Analysis of “Issued operating permits – water systems”

**Project Title**: Understanding the Summary Statistics of Water Systems Operating Permits at the City of Vancouver

**Objective**: The core objective of this descriptive analysis is to answer some significant descriptive business questions for comprehensive insights and enable data-driven decision-making through the summarization of the key characteristics and trends. These insights will help the city increase operational efficiency and enhance public service delivery.

  *Q.1. How many systems in each category are currently Active vs. Inactive?*
  *Q.2. How many mechanical system owners are voluntarily participating in the Operating Permit program?*
  *Q.3. What is the current proportion of the four different types of mechanical systems?*
  *Q.4. What is the count of the permits renewed by month?*

**Dataset**: This dataset details permits issued for water systems, including permit types, renewal and reporting dates, and the systems they govern.

  •	Operating permit number: Unique permit number generated when the application is submitted.
  •	Mechanical system type: Lists four types: Cooling towers, Decorative water features, Building water treatment systems and Rainwater harvesting/non-potable.
  •	Current system status: Either Active or Inactive.
  •	Permit renewal date: The permit renewal date is the date by which an Operating Permit must be renewed.
  •	Voluntary participant: Y or N, where Y means that the owner of the mechanical system is not subject to the Operating Permit program but is voluntarily participating, and N means that the owner is legally required to participate in the Operating Permit program.
  •	Turbidity: The turbidity of the water sample as measured by an accredited laboratory in units of NTU (nephelometric turbidity units) and applicable only to rainwater harvesting water systems.
  •	Temperature: The temperature of the water sample, as measured by the operator, is in units of degrees Celsius and is applicable only to rainwater harvesting.

**Tools and Technologies**:

  •	Primarily, the AWS Glue and Glue DataBrew services were used to carry out descriptive analysis.
  •	The Open Data Portal of the City of Vancouver provides a built-in feature named Chart Builder. This has been used to create different visualizations.

**Methodology**:

1.	Data Collection and Preparation: As part of the data ingestion process, the dataset was exported in Excel format from the City of Vancouver – Open Data Portal and then uploaded to the raw S3 bucket on AWS. Further, the dataset was prepared for the descriptive analysis by profiling and cleaning it using the AWS Glue DataBrew.
2.	Descriptive Statistics: To find the answers to the descriptive questions given, ETL pipelines were designed using the AWS Glue service.
3.	Data Visualization: Different kinds of visual representations were also created to illustrate the findings produced by the ETL pipelines, such as:
    a.	Bar chart for Current System Status by Mechanical System Type
    b.	Normally stacked Bar chart for the Voluntary Participant count by Mechanical System Type
    c.	Pie chart for the proportion of Mechanical System Types
    d.	Treemap for the count of permits renewed by month

**Insights and Findings**:
The insights derived from the descriptive analysis of the given dataset were as follows:

1.	The Cooling Tower system has the highest number of active permits, followed by the Decorative Water Feature system. The rainwater harvesting system has the least active permits.
2.	The proportion of voluntary participation by the system owners is significantly less, merely a little over three percent.
3.	Most operating permits are applied by the owners of Cooling Tower water systems, which stands at 57% of the total.
4.	Nearly 30% of the permit holders are due to renew their operating permits in the first two months (January and February) of 2025.
