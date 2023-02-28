# Yulu---Hypothesis_Testing
Yulu has recently suffered considerable dips in its revenues. They have contracted a consulting company to understand the factors on which the demand for these shared electric cycles depends. Specifically, they want to understand the factors affecting the demand for these shared electric cycles in the Indian market.

Data has 10886 rows and 12 columns. Rest of the observations are in the notebook


Comments on range of attributes, outliers of various attributes : 

Date :
Min value : 2011-01-01
Max value : 2012-12-19

Season : All 4 are almost evenly distributed accounting for roughly 25% each

Working day : Around 70% are working day and 30% non working day

Weather : 1 and 2 account for most of the values (more than 90%)

Temp : 13-26 in this we have 50% of the values.  37+ and less than 6 are outliers

Atemp : 6-31 in this we have 50% of the values. 40+ and less than 8 are outliers

Humidity : 47-100 in this range we have 75% of the values. Values below  16 can be considered outliers (except 0)

Windspeed : 0 to 40 covers most of the values in decreasing order of counts. 40+ can be considered outliers

Casual : 0 to 17 is very densely populated and contains 50% of the values. Values of 300 plus can be considered outliers

Registered : 0 to 118 contains 50% of the values.  0 to 36 is range wise the smallest quartile. 800+ can be considered outliers

Count :  to 145 contains 50% of the values. 800+ can be considered outliers



Comments on plots and distribution / relation of variables :

For Categorical variables :
Holiday 0 and for Working Day 1 accounts for most values

Seasons : All 4 are evenly distributed

Weather : 1 and 2 are most common . 4 almost 0%

Temp :  6-35 we get most of the values
Atemp: 10-39 we get most values
Humidity: 20 - 100 we have most values. Most frequent are in the range 70 to 100 like 88, 94, 83, 87 etc. Right skewed
Windspeed : 0  is most frequent and from there as windspeed increases the frequency decreases. Heavily left skewed distribution

For Casual, Registered and Count  heavily left skewed distributions. As we move from 0 to higher values the frequency decreases


Relationship between Variables :

workday - count : more count on 1 than 0

season - count :  2 and 3 are most seasons with highest count

weather - count : from 1 has  highest and then decreases till 3 . For 4 slightly than 3 but less than 2

temp-count : from 3 onwards till 40 count linearly increases as temperature increases

humidity-count : below 20 count is negligible. At 20 count peaks and then decreases in a linear fashion till 100 humidity

windspeed-count: between 0 to 40 windspeed avg count is almost uniform. 40 to 50 avg count decreases and then 50 plus it peaks  Not much inference can be drawn from this

working day-casual : on a non working day a lot more casual users are there than on a working day.

working day-registered : on a working day more registered users are there but difference not very significant to non working day.
 

Hypothesis Testing :

1) 2 sample T test

 t val is 1.26, DOF is 1
for significance level (0.05) for two tailed T test the critical value s 12.706
Critical value < t val

Hence we accept the Null Hypothesis that working day has no major effect on no of electric cycles rented

2) ANNOVA

Weather

p value much smaller than 0.05. We reject null hypothesis and no of cycles rented are different in different weather

Season

p value much smaller than 0.05 hence again we reject the null hypothesis. No of cycles rented changes with season


These findings are consistent with what we have found graphically as well
