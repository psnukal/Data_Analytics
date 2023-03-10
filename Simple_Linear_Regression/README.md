Simple Linear Regression:
Simple linear regression is a statistical technique for finding the existence of an association relationship
between a dependent variable and an independent variable. Simple linear regression implies that there is only
one independent variable in the model. Regression is one of the most important techniques in predictive
analytics since many prediction problems are modeled using regression.

Action Potentials in Dragons:
Brain cells, called neurons (diagram shown below), send information throughout the brain and body. The
information is sent via electro-chemical signals known as action potentials that travel down the length of the
neuron. These neurons are then triggered to release chemical messengers at synapses, called neurotransmitters,
which help trigger action potentials in nearby cells, and so help spread the signal all over. An action potential
travels down a neuron's axon in an ion cascade. (Source: Khan Academy).

In the imaginary land of the once extinct dragons were spotted again. The maesters of the capital,
King's Landing, were summoned to study the nervous systems of these dragons. They were curious about
how such large were able to move around so quickly. They studied 67 nerve bundles of two dragons
and measured the maximal conduction velocity fibers and the axon diameter of the largest fiber
(Similar to the study conducted by Hursh in 1939).

Data Dictionary
axon_diameter: diameter of the axon in micrometers
conduction _ velocity: conduction velocity of action potentials in meters per second.

Problem 1 (1 point)
Find if a linear model is appropriate for representing the relationship between the conduction velocity
(response variable) and axon diameter (explanatory variable) by finding the OLS solution. Print out the slope
and the coefficient. Plot the OLS best-fit line of the model (Hint: use the ggplot library),

Problem 2 (3 points)
Plot the residuals of the model, Do the residuals look like white noise? If they do not, try to find a suitable
functional form (hint: try transforming either x or y using natural-log or squares).

Problem 3 (3 points)
Using Mahalanobis distance as a metric, are there any potential outliers you notice? What are their
Mahalanobis distances? the model that you decided on in the previous problem (Problem 2) as your
regression model. Ensure that you plot the ellipse with a radius equal to the square root of the Chi-square
value with 2 degrees of freedom and 0.95 probability.

Problem 4 (1 point)
What are the R-squared values of the initial linear model and the functional form chosen in Problem 2? What
do you infer from this? (hint: use the summary function on the created linear models)

Problem 5 (2 points)
Using the same summary function as Problem 4, determine if there is a statistically significant linear relationship
at a significance value of 0.05 of the overall model chusen in Problem 2. What do you understand about
the relationship between dragons' axon diameters and conduction velocity? (Hint: understand the values
displayed in summary and search for the right data).
