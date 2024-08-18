# STA-S380 Exercises
## Probability Practice
### Part A
Using the rule of total probability, we know that:
```math
P(\text{RC}) \times P(\text{Yes} | \text{RC}) + P(\text{TC}) \times P(\text{Yes} | \text{TC}) = P(\text{Yes})
```
With the information given, we can fill in the equation so that: 
```math
0.3 \times 0.5 + 0.7 \times P(\text{Yes} | \text{TC}) = 0.65
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
## Visual Story Telling Part 1
## Visual Story Telling Part 2: Capital Metro Data
When first looking at the Cap Metro data, I wanted to make sure I understood the overall trends before I dug into the details. As a result, I started very broad. Below, you'll see a graph plotting the average number of people who got on and off the bus on a given day throughout the semester. 
![Total Boardings and Alightings](Total_Boardings_Alightings.png)
There is an obvious pattern here: large spike followed by large drops. I assumed that this was because the weekdays have a lot more riders than the weekends, as students and university employees will likely not be coming in on the weekends. It's also interesting to note the more prolonged drop in November. This seems to be Thanksgiving break.   
<br> To zoom in on the days of the week and confirm my suspicions, I created two side-by-side bar graphs that you'll see below. It measures the average number of people that got on (left) or off (right) the bus on a given day of the week. 
![Average by Day](Average_by_day.png)
As I thought, ridership is much higher on the weekdays than on the weekends. It peaks on Tuesdays, stays pretty steady throughout the rest of the weekdays, and then has a slight drop on Fridays. Finally, the weekends have less than about 25% of the weekdays' ridership.   
<br> Now that I examined the patterns of ridership by the day of the week, I wanted to zoom in even further. Below, you'll see two side-by-side line graphs. These are similar to the graphs above in that they measure average ridership, but this time it is by hour of the day, rather than by day of the week. Additionally, since we have now seen a large difference in weekdays versus weekends, I split the graphs on this variable and plotted boarding and alightings together. 
![Average by Hour](Average_by_hour.png)
Here, the data shows what we would expect. The number of alightings is high in the mornings, as people are coming to campus for classes or work. Then, boardings hit their peak in the late afternoon/evening, as people get off work or school and head home. The weekends actually show a similar pattern, just at a much less exaggerated level.  
<br> Again, I wanted to zoom in even more. Now, we've seen boardings and alightings by day and by hour. Let's look at the 15-minute increments as well. To do this more effectively, I decided to focus on weekdays only so that the visuals wouldn't get too complicated. Furthermore, this is just where most of the data is, so it would be easier to find more solidified patterns there. Below, you'll again see two graphs. The first is for average alightings for each 15 minute period from 6 am to 12 pm. I zoomed in on this 6 hour period, as it captures the peak of alightings. The second graph is the same for boarding, except it zooms in from 1 pm to 7 pm, in order to capture the peak for alightings.
![Average by 15 Minutes](Average_by_15.png)
The peaks for boardings (the second graph) made a lot of sense. The highest is at 5:15 pm. We can assume that people are getting off work and then catching the bus 15 minutes later. However, there is also a really high peak at 2 pm. I would guess that this is for students who have finished their classes for the day and are heading home.  
<br> However, what caught my attention most was in the first graph. There is a clear pattern for four hours, where there is a peak at the 45-minute mark, with a stark drop when the clock hits the hour. Obviously, people are taking the bus in to get to work or classes, which usually start on the hour. Making a few assumptions, I believe we can extract information here on how many people are late on average. When the drop between the 45-minute mark and the hour is very steep, people are more on time. However, when this becomes flatter, more people are late. I decided to focus on average alightings in the morning to see if I could find any other patterns on alightings and lateness.  
<br> Next, I decided to try and see if people are later on specific days. Below, you'll see a graph plotting the average alightings by day of the week. This is a little convoluted, so I have also split the graph three ways. However, I wanted to include the overall graph for an easier comparison of all five days. In the three graphs below, I split them to show Mondays and Wednesdays together, Tuesdays and Thursdays together, and ten Fridays. This is because I found these days followed similar patterns, likely because of how students' schedules work. 
![Average by 25 Minutes Weekday](Average_by_25_weekday.png)
![Average by 15 Minutes Weekday Split](Average_by_15_weekday_split.png)
In terms of lateness, there aren't any extremely strong patterns, but there are still some things I'm noticing. First, the drop from 7:45 am to 8 am remains pretty consistent, while there is more variability throughout the rest of the morning. My main theory for this is that 8 am is when work starts, while the later hours are when more classes start. As a result, employees are more consistently on time than students.  
<br>Next, when looking at the three smaller graphs, we can see that the smallest drops are on Monday at 9 am and Tuesday at 9 am. The rest of the data shows pretty consistent steep drops from the 45-minute mark to the hour. From this, I am assuming that students are most likely to be late for morning classes at the beginning of the week. While we would need more data to confirm this suspicion, it is an interesting point to note.  
<br> I would like to note that I also created a couple more graphs to look at the data by month and explore the effects of temperature. These are included in my code, but I did not find them as interesting in terms of the narrative I am telling here, so I decided to leave them out in order to keep my story more focused and concise.  
<br> [Here is the code for this problem.](Capital%20Metro.ipynb)
