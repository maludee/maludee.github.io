---
layout: post
title: Predicting success in the NBA
---

What is success?

In this case, I chose win/loss ratio - in other words, the total amount of wins a team achieves in a season divided by the total amount of losses. 

The background on this project:
The general goal was to scrape some data from the web, and make a prediction with it. I chose to focus on basketball because I wasn't too familiar with the sport and thought it would be a fun way to learn some new things!

I chose to scrape the data from basketball-reference.com, which has a huge amount of data about basketball, going all the way back to the 1940s.

Model # 1:

As someone who didn't know too much about basketball, I was interested in which features would be the most predictive of NBA success. So for my first model, I scraped a fairly diverse group of statistics, including offensive stats, defensive stats, and descriptive features about players. For example, my data included the average points scored by player, their pace, number of steals, age, average salary, and several other features.

I scraped the information by player by team, but then narrowed my information down to focus only on the starting five for each team. I thought that this would be a fairly simple way to then use this information to make decisions about who should spend the majority of their time on the court.

Another metric that I added in was "strong link" or "weak link." The thinking behind this was that if a team had a player on their starting five that was really strong (think, LeBron James or Steph Curry), this might have an added benefit to the team. Conversley, if a team had a player on the starting five who was significantly worse than the other five, this might have a particular negative impact. These metrics were measured by the distance that a player was away from the average of the starting five. For example, Steph Curry was almost 50% better than the average of his Golden State Warrior teammates in the starting five in 2016.

After fitting the model to my training data, I found a few features that were particularly important:
- PER (player efficiency rating - see detailed explanation [here:](http://www.basketball-reference.com/about/per.html)
- Player age
- Opponent field goal success rate
- Weak link
- % of time that the starting five started

After the exploration, I was interested in seeing whether these features would still predict win/loss ratio if I took data from just the first few games of the season rather than data from the entire season.

Model # 2:

I went back to basketball-reference.com and scraped the data again, this time just for the first month of the season. Since NBA seasons are typically 6 months, I thought this would be a good early indication of how teams were performing. 

I fitted the second model, and although the model was less predictive (and r-squared of about .4) it did still show that similar features were the most predictive:
- PER
- Player age
- Opponent field goal success rate
- Strong link

At the end of this project, I was able to use web scraping (Scrapy and Selenium), data manipulation (Pandas) and linear regression (StatsModels, SciKit - Learn) to hone in one some features that are predictive of team success in the NBA. 

See the complete presentation [here:](https://github.com/maludee/proj2-nba/blob/master/dee_malu_basketball_slides.pdf)
