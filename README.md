# STA-S380 Exercises
## Probability Practice
### Part A
Using the rule of total probability, we know that:
```math
P(\text{RC}) \times P(\text{Yes} | \text{RC}) + P(\text{TC}) \times P(\text{Yes} | \text{TC}) = P(\text{Yes})
```
With the information given, we can fill in the equation so that: 
```math
0.3 \times 0.5 + 0.7 \times P(\text{Yes} | \text{TC}) = 0.65 Yes
```
After solving the equation, we find that **71.4% of people that are truthful clickers answered yes**.

### Part B
Based on Baye's Theorem, we know that:
``` math
 P(\text{Disease} \mid \text{Positive}) = \frac{P(\text{Disease}) \times P(\text{Positive} \mid \text{Disease})}{P(\text{Positive})}
```
We already have information on P(Positive | Disease), and P(Disease). However, now we need to use the rule of total probability to find P(Positive). We know that the probability that someone who tests positive is the sum of the probabilities that someone who does not have the disease takes the test and tests positive plus the probability that someone who has the disease takes the test and tests positive. In equation form:
```math
P(\text{No Disease}) \times P(\text{Positive} | \text{No Disease}) + P(\text{Disease}) \times P(\text{Positive} | \text{Disease}) = P(\text{Positive})
```
Filling in the Equation with the given information, we know: 
```math
0.999975 \times 0.0001 + 0.000025 \times 0.993 = P(\text{Positive})
```
As a result, we know that the probability of someone testing positive is .000125. To find the probability that someone who tested positive actually has the disease, we can plug this into our original equation:
``` math
P(\text{Disease} \mid \text{Positive}) = \frac{0.000025 \times 0.993}{0.000125}
```
After solving this equation, we find that **there is a 19.89% chance that they have the disease**.
## Wrangling the Billboard Top 100
### Part A

Here is a table showing the top 10 most popular songs since 1958, based on the total number of weeks spent on the Billboard Top 100:
![Top 10 Most Popular Songs](Top%2010%20Most%20Popular%20Songs.png)
<br>The code for creating this table can be found [here](Billboard%20Top%20100.ipynb#part-a).
### Part B
Here is a graph depicting the number of unique songs on the Billboard Top 100 from 1959-2020:
![Musical Diversity Over Time](Musical_Diversity.png)
<br>Here, we see a peak of over 800 songs from 1965-1970 before there is a steep drop. In the early 2000s, the music diversity hits a low with just under 400 songs. Then, it quickly jumps back up, almost reaching 800 again in 2020.  
<br>The code for this graph can be found [here](Billboard%20Top%20100.ipynb#part-b).
<br> (Note: You may have to scroll to Part B, as my anchored links have not been working)
### Part C
Here is a bar plot of the number of 10-week hits that artists with over 30 10-week hits have:  
<br>
![Most 10 Week Hits](10_Week_Hits.png)
<br>We can see that Elton John is the artist with the most 10-week hits, with over 50 songs that have stayed on the Billboard Top 100 for at least 10 weeks. He is followed by Madonna, who has just under 44, then Kenny Chesney, who has 42.  
<br>The code for this graph can be found [here](Billboard%20Top%20100.ipynb#part-c).
<br> (Note: You may have to scroll to Part C, as my anchored links have not been working)
