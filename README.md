# payroll
Payroll analysis for City of Columbia, Missouri

Columbia makes checkbook data available for download online: https://como.payroll.socrata.com/#!/year/All%20Years/full_time_employees,others/pay1,pay2,pay3,pay4/explore/1-0/segment2

Due to a glitch in the website, I had to download each year of data separately. For this analysis, I'm using fiscal years 2017-2023.

Each row of data represents a payroll transaction for a city employee -- including individual charges (base pay, overtime, social security, etc.) It allows us to see how much of each element makes up an individual's paycheck. 

The RMD file included in this repository includes integrity checks and questions for analysis -- most of which pertain to overtime allocation among city employees. This is also a work-in-progress. As I come up with more questions to ask the data in my spare time, I will update the RMD file. 

Key findings so far:

Unsurprisingly, the police and fire departments spend the most in payroll and have the highest paid employees. Police officers also ear the most in overtime -- sometimes more than $20,000 in a calendar year. This was tricky to track because of a consistent error I noticed occurring when overtime was logged. Sometimes it is logged correctly, in the field labeled "overtime_pay," but sometimes it is logged in the "other_pay" field, and labeled as overtime in the "subcategory" field. I have written code to grab all of the overtime payments, so we can analyze them without missing anything. 

I have been able to identify the highest earners in the department, and those who are putting in the most overtime. Additional reporting is needed to see what the rate of overtime pay is and how these dollar amounts translate to hours worked.

My next objectives including learning overtime trends for individuals just before they retire (as this dataset includes employees who have since retired), and analyzing travel and meal expenses.
