# Reducing length of stay & managing treatment cost of healthcare services

## Business problem
Hospital management records a significant volume of patients and high amount of billings along the periods of 2019 to 2024. Leadership is concerned about:

-	Rising treatment costs
-	Increasing average length of stay
-	Uneven billing amounts across conditions
-	Insurance reimbursement pressures

**They want to know:**

-	Which medical conditions drive the highest costs?
-	Are certain admission types more expensive?
-	Have billings performed well across the years?
-	Is the variation between doctors and length of stay?

This report provides a comprehensive look at hospital performance by integrating clinical efficiency metrics with financial outcomes.

### Dataset 
-	Healthcare dataset gotten from Kaggle
-	Covers a timeline from 2019 – 2024 (approximately 6 years)
-	Contains 55,000 records

### Key columns

The data contains
-	Name
-	Age
-	Gender
-	Blood type
-	Medical condition
-	Date of admission
-	Doctor
-	Hospital
-	Insurance provider
-	Billing amount
-	Room number
-	Admission type
-	Discharge date
-	Medication
-	Test results
 
### Tools used

-	Excel/power query – ETL process
-	PowerPoint – for dashboard wireframing

### Data cleaning

-	Imported csv file into power query
-	Standardized column names
- Standardized date formats
-	Extracted year and month from admission date column for time intelligence
-	Created calculated columns for age bin and length of stay

### Data modeling

-	Created a couple DAX measures
-	Total and average billing
-	Average length of stay
-	Patient count
-	Max and min LOS and billing amount
-	Previous year billing, LOS and patient count
-	Standard deviation of billing and LOS
-	YOY % of billing, LOS, and patient count
-	Added timeline slicers to view the report year by year

### Key questions that need answers

I divide the questions into two; **Cost focused**

-	Which medical conditions generate the highest average billing?
-	Does admission type affects billing amount?
-	Which insurance providers are linked to highest/lowest billing?

and **Efficiency focused**

-	Which conditions have the highest patient volume?
-	Do older patients stay longer?
-	Which doctors handle longer stay patients?

## Key Insights

-	Volume vs. Revenue Growth: There has been a significant 22.85% increase in patient count year-over-year, which has directly driven a 22.98% increase in total billing (currently at $1417.43M).
-	Stability in Care Delivery: Despite the surge in volume, the Average length of Stay (LOS) has remained at 15.5 days (a negligible 0.09% increase). This indicates that our clinical throughput is scaling effectively with demand.
-	Billing Drivers: Diabetes remain our highest biliing condition, while Arthritis and Diabetes account for our highest patient volume.
-	Payer Mix: Billing is distributed almost evenly across major providers, with Cigna representing the highest billing total and Aetna the lowest.

## Recommendations

-	Optimize High-LOS Providers: Address the variance in LOS by Doctors. Some Providers have significantly higher stay than others. Standardizing care pathways for these outliers could free up bed capacity.
-	Resource Allocation for Chronic Care: Given that Arthritis and Diabetes dominate both patient volume and billing, consider expanding specialized outpatient programs to manage the conditions more efficiently and reduce the need for long inpatient stays.
-	Emergency vs. Elective Balance: The admission types are almost perfectly split (around 33% each for Elective, Emergency, And Urgent). We should investigate if Emergency admissions are driving higher costs vs. Elective to ensure our staffing models match these unpredictable influxes.

## Visualization

