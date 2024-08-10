# STA-S380 Exercises
## Probability Practice
**Part A**<br>
Using the rule of total probability, we know that:
```math
P(\text{RC}) \times P(\text{Yes} | \text{RC}) + P(\text{TC}) \times P(\text{Yes} | \text{TC}) = P(\text{Yes})
```
With the information given, we can fill in the equation so that: 
```math
0.3 \times 0.5 + 0.7 \times P(\text{Yes} | \text{TC}) = 0.65 Yes
```
After solving the equation, we find that **71.4% of people that are truthful clickers answered yes**.

**Part B**<br>
Based on Baye's Theorem, we know that:
``` math
 P(\text{Disease} \mid \text{Positive}) = \frac{P(\text{Disease}) \times P(\text{Positive} \mid \text{Disease})}{P(\text{Positive})}
```
We alread have information of P(Positive | Disease), and P(Disease). However, now we need to use the rule of total probability to find P(Positive). We know that the probability that someone who tests positive is the sum of the probabilities that someone who does not have the disease takes the test and tests positive plus the probability that someone who has the disease takes the test and tests positive. In equation form:
```math
P(\text{No Disease}) \times P(\text{Positive} | \text{No Disease}) + P(\text{Disease}) \times P(\text{Positive} | \text{Disease}) = P(\text{Positive})
```
Filling in the Equation with the given information, we know: 
```math
0.999975 \times 0.0001 + 0.000025 \times 0.993 = P(\text{Positive})
```
AS a result, we know that the probaility of someone testing positive is .000125. To find the probability that someone that tested positive actually has the disease, we can plug this into our original equation:
``` math
P(\text{Disease} \mid \text{Positive}) = \frac{.000025 \times .993} \mid \text{Disease})}{.000125}
```
After solving this equation, we find that **there is a 19.89% chance that they have the disease**.
