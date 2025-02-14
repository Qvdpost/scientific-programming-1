## Assignment 2: how representative is the sample

In the real world we unfortunately can't always know everything. We cannot precisely determine the lengths of each women in the Netherlands, just like Maurice de Hond doesn't know of each Dutchman what political party they will vote for. By use of samples however, we can gain an insight on the entire population: we determine the lengths of a group of women, or the political preferences of a group of Dutch citizens and create an estimate of the characteristics of the entire population.

In this assignment we'll study how much more precise of an estimation we get of the 'real' average when we increase the number of people in a sample, by using the computer to generate fake samples. So we'll select random values from the original 'real' distribution. By calculating the average length for each of these samples we can determine how often such a sample approximates the actual value and how this percentage depends on the number of subject in a sample.

#### Assignment 2: effect of more measurements on accuracy

Create a program `statistics_2.py` that calculates what percentage of groups of women (samples) deviates more than 5 cm of the real average (170.6 cm). Do this for varying sample sizes (number of women in the sample): $$N=2,3,5,10,100$$.

Determine the fraction for a specific value of $$N$$ by following these steps:

  * Select N random values from the original distribution: a sample
  * For each sample: determine the average of the lengths of the women in that sample and store that value
  * Repeat this for a large number of samples (100000 for example)
  * Keep track in how many samples the average deviates more than 5 cm of the 'actual' average (170.6 cm)
    Note: we mean both greater than 175.6 cm and smaller than 165.6 cm
              
`Print` the percentages to the screen and use 2 decimals:
{: .language-python}
    Fraction of deviating samples for N =   2: x.xx percent
    Fraction of deviating samples for N =   3: x.xx percent
    Fraction of deviating samples for N =   5: x.xx percent
    Fraction of deviating samples for N =  10: x.xx percent
    Fraction of deviating samples for N = 100: x.xx percent

Extra: try to help the user by neatly formatting It numbers to be aligned underneath each other like in the example.

It is very insightful to view distributions of averages for varying choices in sample size. Use the histogram-method we've also implemented in assignment 1. Choose the appropriate bin-size yourself.

**Conclusion:** The larger the sample the better the average approximates the 'actual' value. That sounds logically, since it makes quite the difference whether Maurice de Hond asks 10 people their political preference or 100000. For each number, measurement, or graph that you see from now on, whether it's in the papers, on television or in a scientific publication, you always have to wonder what the uncertainty is of the estimation. The smaller the error/uncertainty, the more important the measurement is and the 'more gravity' you measurement has when you mean to compare results and draw conclusions from your measurements. So an estimation without specifying the margin of error has no real value.
