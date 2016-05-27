# Making-Data-Management-Decisions
Assignment (wk3): Making Data Management Decisions in Data Management and Visualization

###For Setting asdie missing data, 
I used 'Were you born in the United States? (variable 'H1GI11') and 'What language is usually spoken in your home? (variable 'H1GI10').

I recode missing values (code 6 and 8) to python missing (NaN).

###For Coding in valid data and recoding values,
recode 7 values as 1 in variable 'H1GI11'.

code 7 is  legitimate skip [lived at current address since birth]

###For Creating secondary variables,
I set new "Eng_US" variable, 

who is born in United State and speak English at home as 0

who is born in United State but speak other language at home as 1

who is not born in United State and speak English at home as 2

who is not born in United State but speak other language at home as 3

###For Grouping variables within individual variables,
I splite "AGE" variable into 3 groups (12-15, 16-18, 18-22) 
