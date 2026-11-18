# Patient No-Show Analysis (Power BI)

## Business problem
A healthcare provider loses money and clinic time when patients miss appointments. Which patients are most likely to miss, and what can the clinic do about it?

## Dataset
Medical Appointment No Shows (Kaggle), about 110,500 appointments from Brazil in 2016, with age, gender, neighbourhood, appointment dates, SMS reminder and a no-show flag.

## Approach
Cleaned the data in Power Query (fixed date and number types, removed rows with negative age). Created three columns in DAX: Wait_Days, Wait_Band and Age_Group. Wrote a DAX measure for the no-show rate. Built a dashboard with a KPI card, charts by age group and by waiting time (split by SMS reminder), and slicers for gender and neighbourhood. About 200 appointments dated before their booking date were excluded from the waiting-time chart as invalid.

## Findings
1. 20.2% of appointments are missed, about 1 in 5.
2. The no-show rate rises with waiting time: 5% for same-day appointments, 24% for 1-7 days, 32% for 8-30 days and 33% for more than 30 days.
3. Patients aged 19-40 miss the most (23%) and patients over 60 the least (15%).
4. For waits over a week, patients who received an SMS missed fewer appointments (29-30%) than those who did not (36-38%). For waits of 1-7 days there was no real difference (about 24% for both).

## Recommendations
1. Offer earlier slots or rebooking to patients who face waits of more than a week.
2. Send SMS reminders to every patient with a wait of more than a week.
3. Pay extra attention to the 19-40 age group when planning reminders.

## Limitations
This is observational data, so it shows links, not proof of cause. No same-day patients received an SMS, so the SMS effect could only be compared for longer waits. The data is from one region in one year, and percentages are rounded.

## Files
- noshow_dashboard.pbix: the Power BI file
- noshow_dashboard.pdf: the dashboard as a PDF
