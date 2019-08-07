## Summary
Based on NBA career statistics from all Basketball Hall of Fame inductees, a predictive model is used to calculate the probability of hall of fame induction for all current and recently-retired players 

## Introduction
Since 1959, the Naismith Memorial Basketball Hall of Fame has inducted almost 400 coaches, players, referees, contributors, and teams. It honors individuals who have shown exceptional skill at basketball, all-time great coaches, referees, and other major contributors to the sport (broadcasters, journalists, etc.). 

Several people have been inducted multiple times, either as players/coaches or as coaches/contributors. A players does have to play in the NBA to be inducted, as career achievements in college, WNBA, international teams, and other platforms are considered. For a player to be eligible on the ballot, he or she must be fully retired for at least three years. They can also become inducted as a part of a historically-significant team, such as the 1992 US men's Olympic basketball team - widely regarded as the greatest team ever assembled in any sports.

To analyze which current and recently-retired players will become inducted into the hall of fame in the future, I created various models based on almost 60 years of previous data.

## Data & Methods
Based on the data I web scraped from [Basketball Reference](https://www.basketball-reference.com/), I created a database of all historical ABA/NBA players since 1947 who played at least one game. For these players, I retrieved the following stats:

Column | Description
-------|-------------
'name' | full name of player, first name and last name
'active_from' | year started playing for the NBA
'active_to' | last year playing for the NBA (2018 is still active)
'career_length' | seasons played in league (disregards if retired during)
'birth_date' | datetime variable, date of birth
'position' | five positions classification - most common approach in modern ear
'trad_position' | three positions classification - traditional approach of describing positions
'ppg' | float variable, total points per game
'trb' | float variable, total rebounds per game
'ast' | float variable, total assists per game
'per' | float variable, [player efficiency rating](https://www.basketball-reference.com/about/per.html)
'ws' | float variable, [win shares](https://www.basketball-reference.com/about/ws.html)
'height_inches' | float variable, height measured in inches
'weight' | float variable, weight measured in pounds
'shooting hand' | prefered shooting hand
'hof' | 0 or 1, inducted into Naismith Memorial Basketball Hall of Fame as player. 0 if inducted as coach, contributor, etc.
'college' | college basketball programs of participation
'hs_name' | name of high school attended
'hs_city' | city of high school location
'hs_state' | state or country (if foreign player) of high school
'url' | player page in www.basketball-reference.com

Using all the counting statistics, such as career per-game statstics and advanced stats, I created four models to predict a player's hall of fame induction probability. 

With these inputs and outputs, I created four models:
- Logistic regression
- Decision tree and random forest classifier
- Naive Bayes classifier
- Support vector regression (SVM)

The models were trained and tested on hall of fame data from 1947-2015, and then made predictions for current players and players retired since 2015.

## Conclusion
The model predicts tha LeBron James - based on current achievements - has the highest likelyhood of becoming inducted into the hall of fame. Recently-retired players like Tim Duncan, Kevin Garnett, and Kobe Bryant - all likely to be in the hall of fame class of 2021 - will be inducted within a few years. We also saw the model's limitations, since it does not take account for international career, team success, awards, cultural impact, etc. However, the model is mostly accurate in predicting which active and recently-retired players will be inducted.


