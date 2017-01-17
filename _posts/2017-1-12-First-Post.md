---
layout: post
title: Analyzing NYC Subway Data
---

What's the best place in NYC to gather signatures?

For our first project at Metis, we analyzed MTA turnstile data to determine the best places for a (fictional) organization to place canvassers. 

The MTA posts weekly data files with information about how many people enter or exit all 472 subway stations in the city, broken out by turnstile, date, and time. 

The organization in question had a few concrete goals:

- Raise awareness/gather signatures
- Boost attendance for an early-summer gala
- Get donations

With these goals in mind, we decided to focus on a few different factors. The most important consideration was traffic - in other words, we wanted to use the MTA data to figure out how many people were going in and out of the different subway stops during the period of time we were examining (April - June 2016). We also wanted to further narrow our focus by considering the income of the neighborhood as well - it seemed like a simple way to reach people who might have more to donate.

Our group was also lucky to have someone who had real-life canvassing experience. They told us about a few other factors that we may not have otherwise considered. For example, it's useful to send a team of canvassers to a location a few times - that way, someone walking by can get several opportunities to stop for a canvasser. Then, after spending about a week at a location (for a full day), the team rotates to a new station. 

Having this expertise was not only very interesting, but also helped up think about how many subway stations we should recommend to the organization. At first it seemed like it would be simple to recommend a handful of stations - maybe five or ten - but after speaking to our real-life canvasser, we realized that a larger list of about fifty stations would be more practical. 

After cleaning the data and removing outliers and duplicate entries, we organized the information we had by station and combined entry and exit figures for total traffic. Then we plotted a histogram based on each station's daily traffic average. From that, we learned that:

- Most stations have a daily average of less than 25K visitors
- The median number of visitors was about 11.5K
- There were some stations with extremely high traffic figures, like Grand Central with 210K daily visitors

We didn't want to send canvassers to stations with extremely high traffic, our thought being that after a certain point, higher traffic would just make it too overwhelming and crowded. We decided to use stations in the 70th to 90th percentiles of traffic volume. That left us with a list of about 100 stations.

The final step was to further narrow down that list by merging it with income data. We used data from the New Yorker's "Inequality and the New York Subway" [found here.](http://projects.newyorker.com/story/subway/)

We sorted our list of 100 stations by income, and dropped the second half of the list to leave us with our final 50 subway stations that we would recommend to the organisation.

See our final presentation [here:](https://github.com/maludee/proj1-mta/blob/master/Benson%20Slides.pdf)


