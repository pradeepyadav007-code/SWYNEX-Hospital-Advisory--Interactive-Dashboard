# SWYNEX-Hospital-Advisory--Interactive-Dashboard
Interactive Power BI dashboard for hospital planning: when patients arrive, who they are, and what to do
# Hospital Advisory Interactive Dashboard (Power BI)

This project is an interactive 6-page Power BI dashboard built on a healthcare dataset of 54,966 patient records from 2019 to 2024. It helps a hospital understand when patients arrive, who they are, and what actions to take each month. It was built as part of the SWYNEX Technologies data analytics program.

## Dataset

The dataset has 54,966 admissions and 15 columns, including age, gender, medical condition, admission type, billing amount, insurance provider, test results, and admission and discharge dates. It covers six conditions: Arthritis, Asthma, Cancer, Diabetes, Hypertension and Obesity. The data looks synthetic (every condition has about 9,100 patients and test results are split almost equally), so the findings show analysis technique and not real clinical conclusions.

## What I did, step by step

First, I loaded the Excel file into Power BI and opened Power Query to check the data. There were no missing values, no exact duplicate rows, and no discharge dates before admission dates. I found about 9,955 rows with the same name and admission date but different ages. I flagged these and did not remove them.

Second, I added new columns in Power Query: Length of Stay (days between admission and discharge), Age Group (Under 18, 18 to 35, 35 to 50, 50 to 65, Over 65), Age Sort (to keep age groups in order), Admission Year, Admission Month, and Month Number (to sort months from January to December).

Third, I created DAX measures for Emergency Rate %, Abnormal Test Rate %, Total Revenue and Revenue in millions.

Fourth, I built six report pages: Overview, When, Who, Emergency, Revenue and Hospital Advisory. Each page has KPI cards and charts for its own question. For example, the Emergency page shows emergency counts and rates by month, condition and age group.

Fifth, I added five slicers (Medical Condition, Gender, Admission Type, Admission Year and Insurance Provider) and synced them, so one selection filters every page.

Finally, I built the Hospital Advisory page with recommendation cards and a month-by-month preparation calendar for hospital management.

## Key insights

August is the busiest month with 4,785 patients, and July has the most emergencies at 1,573. February has the fewest patients but the highest emergency rate at 34.5%, so the emergency ward should not be scaled down. Patients over 65 are the largest group at 16,923 (30.8%). Obesity has the highest emergency rate at 33.9%. Billing per patient is highest in October at $26,020 and lowest in September at $25,256. Total revenue is about $1.4 billion, with August highest at $121.6 million. Admissions jumped 53% from 2019 (7,300) to 2020 (11,172) and then stayed near 10,900 a year until 2023. The 2024 data covers only part of the year.

## Recommendations

Keep the emergency ward fully staffed in January and February. Prepare for maximum staffing and beds in July and August. Focus on elective procedures and health packages in June and October, when billing per patient is highest. Use September for claims processing and collections. Build a dedicated senior-care unit, since over 65 patients are the biggest group, and keep obesity emergency readiness in place.

## Tools used

Microsoft Excel, Power Query, DAX and Power BI Desktop.

## Limitations

The data is likely synthetic. 2024 is a partial year. Month-to-month differences are modest, roughly 5 to 10% between the best and worst months, so treat them as planning signals.
