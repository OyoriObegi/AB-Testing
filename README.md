# AB-Testing
This is a simple A/B testing simulation in Python to test whether a new website design increases the conversion rate compared to the old design. 
We randomly divided 1000 website visitors into two groups: 500 visitors see the old design (group A) and 500 visitors see the new design (group B).

# Hypothesis
We chose a one-tailed test:

H0: p = p0
Ha: p > p0

Null Hypothesis: There is no significant difference in the conversion rates between group A and group B.
Alternative Hypothesis: The conversion rate of group B is significantly higher than the conversion rate of group A.
where p and p0 stand for the conversion rate of the new and old design, respectively.

# Confidence Level
We set a confidence level of 95%:

alpha = 0.05

The alpha value is the probability of rejecting the null hypothesis when it is actually true. A common significance level is 0.05, which means that there is a 5% chance of incorrectly rejecting the null hypothesis. Since our alpha=0.05 (indicating 5% probability), our confidence (1 - alpha) is 95%.

# Variables
Group A, control group - They were shown the old design.
Group B, treatment (or experimental) group - They were shown the new design.
This was our Independent Variable.

For our Dependent Variable, we were interested in capturing the conversion rate. We used a binary variable to represent each user session:

0 - The user did not buy the product during this user session
1 - The user bought the product during this user session
This way, we were able to easily calculate the conversion rate of each design.

# Results
We simulated the results of the A/B test by randomly generating binary outcomes for each visitor: 0 for no conversion and 1 for conversion. If the conversion rate is 10%, we used 0.1 to generate a random binary outcome. We repeated this process for each visitor in both groups to obtain two arrays of binary outcomes, representing the conversion results for group A and group B.

We then calculated the conversion rates and performed hypothesis testing to determine whether the difference between the two rates is statistically significant.

We used the following libraries:

numpy
scipy

# Usage
Clone the repository:

git clone https://github.com/OyoriObegi/AB-Testing.git

Open the A_B_testing_simulation.ipynb notebook in Jupyter Notebook or Jupyter Lab.

# Contributions
Contributions are welcome! If you find any bugs, please file an issue. If you want to contribute code, please fork the repository and make a pull request.
