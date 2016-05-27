# Making-Data-Management-Decisions
Assignment (wk3): Making Data Management Decisions in Data Management and Visualization

## Setting aside missing data
For the response of ' Were you born in the United States?', I coded out missing data.

<code>
print 'Were you born in the United States? '
print 'counts for original H1GI11'
I11 = data1['H1GI11'].value_counts(sort=True, dropna=False)
print(I11)

<output>
Were you born in the United States? 
counts for original H1GI11
1    4807
7    1293
0     399
8       3
6       2
Name: H1GI11, dtype: int64

0 no
1 yes [skip to Q.15]
6 refused [skip to Q.15]
7 legitimate skip [lived at current address since birth]
8 don’t know [skip to Q.15]

<code>
# recode missing values to python missing (NaN)
data1['H1GI11']=data1['H1GI11'].replace(6, np.nan)
data1['H1GI11']=data1['H1GI11'].replace(8, np.nan)

#if you want to include a count of missing add ,dropna=False  
print 'counts for H1GI11 with 6/8 set to NAN and number of missing requested'
I11a = data1['H1GI11'].value_counts(sort=True, dropna=False)
print(I11a)

<output> 
1.000000    4807
7.000000    1293
0.000000     399
nan            5
Name: H1GI11, dtype: int64

I collapsed the responses for urbanrate, femaleemployrate, and lifeexpectancy to create three new variables: urban, fer, and le. For urban, the most commonly endorsed response was 2 (62.44%), meaning that most countries have an urban rate of 25% - 75%. For fer, the most commonly endorsed response was 3 (45.07%), meaning that almost half of the countries have a female employment rate of 40% - 60%. For le, the most commonly endorsed response was 4 (35.68%), meaning that the life expectancy in about one-third of the countries is 65 – 75 years old.
