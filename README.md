# nba-player-info

This project web scrapes all historical NBA player information from the Basketball Reference website, and uses machine learning to predict player positions. 

We use data extracted from the website to make the following dataframe:

- name: full name of player, first name and last name
- active_from: year started playing for the NBA
- active_to: last year playing for the NBA (2018 is still active)
- birth_date: datetime variable, date of birth
- position: five positions classification - most common approach in modern ear
- trad_position: three positions classification - traditional approach of describing positions
- ppg: float variable, total points per game
- trb: float variable, total rebounds per game
- ast: float variable, total assists per game
- height_inches: float variable, height measured in inches
- weight: float variable, weight measured in pounds
- shooting hand: prefered shooting hand
- college: college basketball programs of participation
- hs_name: name of high school attended
- hs_city: city of high school location
- hs_state: state or country (if foreign player) of high school
- url: player page in www.basketball-reference.com

Then a player's position is predicted with different position classification schemes:
1. Modern five positions
- Point Guard 
- Shooting Guard 
- Small Forward 
- Power Forward 
- Center 
2. Traditional three positions
- Guard
- Forward
- Center

The data is then grouped into year-by-year statistics to predict player description (weight, height) and statistics (ppg, trb, ast, etc)
