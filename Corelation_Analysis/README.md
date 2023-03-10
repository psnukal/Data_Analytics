Correlation:
Correlation is a measure of the strength and direction of relationship that exists between two random variables
and is measured using correlation coefficient. Correlation can assist data scientists to choose the variables for
model building that is used for solving an analytics problem.
There are different types of correlation coefficients, based on the nature of the data being compared:
Between two continuous (interval, ratio) random variables - Pearson's Product Moment Correlation Coefficient
Between two ordinal random variables - Spearrnan-Rank Correlation Coefficient
Between a «:mtinuous RV and a dichotomous RV - Point Bi-Serial Correlation Coefficient
Between two binary random variables - Phi Coefficient


Road Accidents
India is the world's second-mcFt populous country with a population of around 1.2 billion people (as of July
2022). Roads are a very important mode of transport in India, spanning over 6.2 million kilometers of length,
making it the country with the second-largest road network, after the United States of America. (Source:
Wikipedia). With India trying to modernize its road infrastructure, there is still the problem of frequent road
accidents.
Road accidents in India is a major cause of death and injury. The NCRB (National Crime Records Bureau)
of India collects detailed data on traffic accidents and collisions annually. Please downl€kid the dataset from
the GitHub repository that contains road accident data in India from 2016. The data was obtained from this
kaggle dataset.


Data Dictionary
S. No. : Serial number
State/ UT: name of state/union terrirory in India
Fine/C1ear — Total Accidents: total accidents per state/UT in Fine/C1ear weather conditions
Fine/C1ear — Persons Killed: total fatalities per state/UT in Fine/C1ear weather conditions
Fine/C1ear — Persons Injured: total injured people per state/UT in Fine/C1ear weather conditions
Mist/ Foggy — Total Accidents: total accidents per state/UT in Mist/Foggy weather conditions
Mist/ Foggy — Persons Killed: total fatalities per state/UT in Mist/Foggy weather conditions
Mist/ Foggy — Persons Injured: total injured people per state/UT in Mist/Foggy weather conditions
Cloudy — Total Accidents: total accidents per state/UT in Cloudy weather conditions
Cloudy — Persons Killed: total fatalities per state/UT in Cloudy weather conditions
Cloudy — Persons Injured: total injured people per state/UT in Cloudy weather conditions
Snowfall — Persons Killed: total fatalities per state/UT in Snowfall weather conditions
Snowfall — Persons Injured: total injured people per state/UT in Snowfall weather conditions
Hail/S1eet — Total Accidents: total accidents per state/UT in Hail/S1eet weather conditions
Hail/S1eet — Persons Killed: total fatalities per state/UT in Hail/S1eet weather conditions
Hail/S1eet — Persons Injured: total injured people per state/UT in Hail/S1eet weather conditions
Dust Storm — Total Accidents: total accidents per state/UT in Dust Storm weather conditions
Dust Storm — Persons Killed: total fatalities per state/UT in Dust Storm weather conditions
Dust Storm — Persons Injured: total injured people per state/UT in Dust Storm weather conditions
Others — Total Accidents: total accidents per state/UT in Other weather conditions
Others — Persons Killed: total fatalities per state/UT in Other weather conditions
Others — Persons Injured: total injured people per state/UT in Other weather conditions


Problem 1 (2 points)
Find the total number of accidents in each state for the year 2016 and display your results. Make sure
to display all rows while printing the dataframe. Print only the necessary columns. (Hint: use the grep
command to help filter out column names).


Problem 2 (2 points)
find the fatality rate in each state. Find out if there is a significant linear
Find the (fatality rate
total number of accidents
correlation at a significance of 0.05 between the fatality rate of a state and the mist/fogyy mte (fraction
of total accidents that happen in mist/foggv conditions).
Correlation between two continuous RVs: Pearson's correlation coefficient. correlation coefficient
between two RVs and y is given by:
Covariance(r, y)
where is the standard deviation of a variable.
Plot the fatality rate against the mist/fogkv rate. (Hint: use the ggscatter library to plot a scatterplot with
the confidence interval of the correlation coefficient).
Plot the fatality rate and mist/foggv rate (see this and this for R plot customization).

Problem 3 (3 points)
Rank the states based on total accidents and total fatalities (give a rank of 1 to the state that has the highest
value of a property). You are free to use any tie-breaking method for assigning ranks.
Find the Spearman-Rank correlation coefficient between the two rank columns and determine if there is
any statistical significance at a significance level of 0.05. Also test the hypothesis that the correlation
coefficient is at least 0.2.
The t statistic is given by
Where rs is the calculated Spearman-Rank correlation coefficient and ps is the value of the population
correlation coefficient being tested against.

Problem 4 (1.5 points)
Convert the column Hail. Sleet.. notal. Accidents to a binary column as follows. If a hail/sleet accident
has occurred in a state, give that state a value of 1. Otherwise, give it a value of O. Once converted, find
out if there is a significant correlation between the hail_accident_occcur binary column created and the
number of rainy total accidents for every state.
Calculate the point bi-serial correlation coefficient between the two columns. (Hint: it is equivalent to
calculating the Pearson correlation between a continuous and a dichotomous mriable. You could also use the
Itm package's biserial. cor function).

Problem 5 (1.5 points)
Similar to in Problem 4, create a binary column to represent whether a dust storm accident has occurred in a
state (1 occurred, 0 not occurred). Convert the two columns into a contingency table.
Calculate the phi coefficient of the two tables. (Hint: use the psych package),
