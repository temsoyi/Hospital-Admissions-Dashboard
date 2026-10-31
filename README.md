# Hospital-Admissions-Dashboard(Power BI)
An interactive Power BI dashboard analysing 929 patient admissions (sample dataset) across wards, diagnoses and age groups. The project covers data cleaning in Excel, DAX measures, and a dashboard built to answer questions about patient outcomes, readmissions and length of stay.

Business Questions
What share of patients are readmitted, and which age groups are most affected?
How do patient outcomes (discharged, transferred, deceased) differ by ward and diagnosis?
Which diagnoses have the longest average length of stay?
What is the gender split of admitted patients?

Rows: 929 admissions
Columns: admission_id, admission_date, discharge_date, ward, diagnosis_code, age_group, gender, los_days, readmission, outcome

Data Cleaning
Standardised mixed date formats (text dates such as 19-07-2021 converted to real dates; day/month/year parsed with Change Type Using Locale)
Created an Age Category column from age_group (Child, Young, Middle Aged Adult, Older Adult, Elderly, Very Elderly)
Handled blank values in the gender column (labelled "Unknown" / flagged)
Checked data types and consistency before building visuals

Dashboard Features
KPI cards: number of patients, % male, % female, readmission rate
Slicers: gender, outcome, age category
Visuals: outcome by diagnosis, outcome by ward, readmission rate by age category, readmitted vs not readmitted, average length of stay by diagnosis

Key Insights
Readmissions: 19.7% of patients (183 of 929) were readmitted.
Age and readmission: middle-aged adults had the highest readmission rate (23.7%), followed by young adults (22.2%). Older adults had the lowest (17.2%), so the oldest patients were not the most readmitted.
Length of stay: average stay ranged from about 21 days (F32) to 26.6 days (I50). I50, S72 and C34 were the longest at over 25 days, but the gap across diagnoses is only about 5 days.
Outcomes overall: about 60% of patients were discharged, 21% transferred and 20% deceased.
Outcomes by ward: Maternity had the highest share of deceased patients (about 28%), followed by Orthopaedics and General (about 24% each). Oncology (about 11%) and ICU (about 13%) were lowest. Orthopaedics handled the most patients (105).
Gender: 58% of patients were male and 42% female.

Recommendations
Add post-discharge follow-up for middle-aged and young adults, who are readmitted most.
Review cases in wards with the highest death share. This may reflect case severity as much as quality of care.
Look for avoidable delays behind the longest stays (I50, S72, C34) and set target stay lengths.
Investigate why about 21% of patients are transferred, as it may point to capacity or specialist gaps.
Standardise data entry at admission (dropdowns, mandatory fields) to reduce blanks and mixed date formats.

Tools
Excel (data cleaning), Power BI (data modelling, DAX, visualisation)
Author
Oche Oyifie

