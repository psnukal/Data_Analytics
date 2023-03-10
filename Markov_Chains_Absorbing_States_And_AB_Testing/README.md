Its a freezing day in New york, Commisioner Wench has sent a report to Captain Holt that the 99th precinct has much lower reported crimes compared to other precincts. Upon Analysis Captain Holt decides to add feedback unit along with the 4 major units to analyse this descripency. All the units are mentioned below

1.   Major Crimes
2.   Traffic
3.   General crimes
4.   Feedback
5.   Theft

---
---
<br>

The initial probablity of a person going to a particular unit on a particular day is given as follows


<br>

Major Crimes | Traffic | General crimes | Feedback | Theft
:----------: | :-----: | :------------: | :--------: | :---:
0.3 | 0.4 | 0.1 | 0.15 | 0.05 
<br>


To measure how many people will go to the feedback unit, the personel files of all employees are give to the **_Move-o-Tron 99_** and it gives us the following matrix which shows us the probability of people moving from one unit to another on a particular day . It is known that the **_Move-o-Tron 99_** alwasy outputs matices which follow a first order Markov chain. 

| |Major Crimes|Traffic|General crimes|Feedback|Theft|
|---|---|---|---|---|---|
|Major Crimes|0\.002|0\.666|0\.31|0\.0|0\.022|
|Traffic|0\.466|0\.102|0\.222|0\.0|0\.21|
|General crimes|0\.022|0\.11|0\.502|0\.0|0\.366|
|Feedback|0\.0|0\.0|0\.0|1\.0|0\.0|
|Theft|0\.11|0\.122|0\.066|0\.0|0\.702|

As the people of New York are smart the will learn where all the units are present and hence the next days (day 1) distribution will be the distribution present at the end of the current day (day 0). Captain holt want to check if the matrix given by the **_Move-o-Tron_** can be used to model the footfall.


<br>
<br>
<br>

## Problem 1 (2 points)

1. What technique can be used to model the probability of people going to the correct unit to report thier crime after N days? (0 points)
2. Is the chain irreducible? Justify (0.5 point)
3. What will be the intital probability of a person going to a particular unit after 1 day, 2 days, 10 days, 1000 days and 1001 days. (1 point)
 Hint: Use the  Chapman−Kolmogorov relationship
4. What can you say about the markov chain from state of intital probability of a person going to a particular unit after 1000 and 1001 days? (0.5 points)


<br>
<br>
<br>

## Problem 2 (4 points)

1. Is the chain irreducible? Justify (0.5 point)
2. What will be the intital probability of a person going to a particular unit after 1 day, 2 days, 10 days, 1000 days and 1001 days. (1 point)
 Hint: Use the  Chapman−Kolmogorov relationship
3. What can you say about the markov chain from state of intital probability of a person going to a particular unit after 1000 and 1001 days? (0.5 points)
4. Summer Edgecombe is Confidential Informant (CI) to the Officer Kimbal Cho and comes in every day to the police station. If on the first day she goes to the Major crimes Unit what will be the probability that she gives a feedback? (2 points)



<br>
<br>
<br>
##Problem 3 (4 points)

It seems that there is a bug in **_Move-o-Tron 99_** which makes general crimes and feedback units as absorbing states. After updating the software of **_Move-o-Tron 99_**, Captain Holt wants to find out the effect that Amy Santiago has on the probability of a person giving feedback. So one matrix is generated including Santiago and the other one without. 

Matrix 1 (With Santiago)

| |Major Crimes|Traffic|General crimes|Feedback|Theft|
|---|---|---|---|---|---|
|Major Crimes|0\.002|0\.232|0\.31|0\.434|0\.022|
|Traffic|0\.426|0\.102|0\.222|0\.04|0\.21|
|General crimes|0\.03|0\.11|0\.2|0\.294|0\.366|
|Feedback|0\.003|0\.176|0\.321|0\.3|0\.2|
|Theft|0\.11|0\.422|0\.166|0\.1|0\.202|

Matrix 2 (Without Santiago)

| |Major Crimes|Traffic|General crimes|Feedback|Theft|
|---|---|---|---|---|---|
|Major Crimes|0\.11|0\.222|0\.092|0\.374|0\.202|
|Traffic|0\.03|0\.11|0\.2|0\.294|0\.366|
|General crimes|0\.002|0\.232|0\.31|0\.434|0\.022|
|Feedback|0\.466|0\.102|0\.02|0\.032|0\.38|
|Theft|0\.003|0\.176|0\.321|0\.3|0\.2|

<br>

1. How can you find out the effect that Santiago has on the probability of feedback? (1 point)

2. What effect does Santiago have one the probability of getting feedback? (1 point)

    Note: The initial probablity of a person going to a particular unit on a particular day remains the same

3. Name the test Captain Holt is performing. (0.5 points)

Lina Ginetti reports to Captain Holt that the there two kinds of days in the precicnt _"There are normal days and then there are days where workflow is dismal with a tiny dash of pathetic."_. Captain Holt decided to sample the initial probablity of a person going to a particular unit on a good day and a bad day.

4. Without the information about these inital probabilities, can you tell if there is any difference in the probability of getting a feedback? Explain. (1.5 points)

