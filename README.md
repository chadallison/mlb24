Chad’s 2024 MLB Report
================

### Contents

- [Team Standings](#team-standings)
- [Team NPR](#team-npr)
- [Total NPR Rankings](#total-npr-rankings)
- [Offensive NPR Rankings](#offensive-npr-rankings)
- [Defensive NPR Rankings](#defensive-npr-rankings)
- [Scorigami](#scorigami)
- [Yesterday’s Largest Victories](#yesterdays-largest-victories)
- [Team Volatility](#team-volatility)
- [Runs Scored per Game](#runs-scored-per-game)
- [One-Run Games](#one-run-games)
- [NPR and Win Percentage](#npr-and-win-percentage)
- [Best Records in Last Ten Games](#best-records-in-last-ten-games)
- [Early Leads](#early-leads)
- [First Score Dependence](#first-score-dependence)
- [Home Field Advantage](#home-field-advantage)
- [Winning and Losing Streaks](#winning-and-losing-streaks)
- [Seven Game Windows](#seven-game-windows)
- [Team Margins in Seven Game
  Windows](#team-margins-in-seven-game-windows)
- [Team Series Results](#team-series-results)
- [Records vs. Above/Below .500
  Teams](#records-vs.-abovebelow-.500-teams)

------------------------------------------------------------------------

### Team Standings

![](README_files/figure-gfm/unnamed-chunk-4-1.png)<!-- -->

------------------------------------------------------------------------

### Team NPR

![](README_files/figure-gfm/unnamed-chunk-6-1.png)<!-- -->

**What is NPR?**

NPR, Naive Performance Rating, is a metric I devised as a measure of
team performance above/below expected. The logic behind it is this: I
calculate each team’s expected runs scored in each game by taking the
average of their runs scored per game and their opponent’s runs allowed
per game. I then compare this expected value to the actual value of runs
scored or allowed to calculate each team’s offensive and defensive NPR
for each game. Here is an example.

Suppose the Cubs are playing the Cardinals. Let’s say the Cubs, on
average, score 4.5 runs per game and allow 3.25 runs per game. And let’s
say the Cardinals score 3.75 runs per game and allow 2.75 runs per game.
We calculate the Cubs’ expected run value as the average of their runs
scored per game and the Cardinals’ runs allowed per game, so (4.5 +
2.75) / 2 = 3.63. We would calculate the Cardinals’ expected run value
the same way, so (3.75 + 3.25) / 2 = 3.5. We now have the Cubs’ expected
run value as 3.63 and the Cardinals’ expected run value as 3.5.

Suppose that the final score of the game is a Cubs victory, 5-3. We
would calculate the Cubs’ offensive NPR as their actual score minus
their expected score: 5 - 3.63 = 1.37. We would calculate their
defensive NPR as the Cardinals’ expected score minus their actual score:
3.5 - 3 = 0.5 (we do it in this order so positive values are good). For
the Cardinals, their offensive NPR is their actual score minus their
expected score, 3 - 3.5 = -0.5, and their defensive NPR is the Cubs’
expected score minus their actual score, 3.63 - 5 = -1.37. Notice how
these numbers are opposite each other. So each team will have an
offensive and defensive NPR for each game, which are aggregated in the
plot below.

Of course, there are so many other factors that would play into a team’s
true expected value, such as any injuries, starting pitchers, weather,
and more. That is why I have named it Naive Performance Rating, because
it assumes matchup metrics are independent of each other and does not
take external factors into account. Which, of course, will lead to flaws
in the metric, but is done for the sake of simplicity and
interpretability (which is ironic because I expect it is still difficult
to interpret for others than myself).

------------------------------------------------------------------------

### Total NPR Rankings

![](README_files/figure-gfm/unnamed-chunk-7-1.png)<!-- -->

------------------------------------------------------------------------

### Offensive NPR Rankings

![](README_files/figure-gfm/unnamed-chunk-8-1.png)<!-- -->

------------------------------------------------------------------------

### Defensive NPR Rankings

![](README_files/figure-gfm/unnamed-chunk-9-1.png)<!-- -->

------------------------------------------------------------------------

### Scorigami

![](README_files/figure-gfm/unnamed-chunk-10-1.png)<!-- -->

------------------------------------------------------------------------

### Yesterday’s Largest Victories

1.  Baltimore Orioles def. Toronto Blue Jays 10-1
2.  Atlanta Braves def. Boston Red Sox 8-3
3.  Tampa Bay Rays def. Miami Marlins 9-5

------------------------------------------------------------------------

### Team Volatility

![](README_files/figure-gfm/unnamed-chunk-12-1.png)<!-- -->

##### Most Volatile Teams

1.  Oakland Athletics (6.77)
2.  Arizona Diamondbacks (6.74)
3.  Colorado Rockies (6.64)

##### Most Volatile Offenses

1.  Arizona Diamondbacks (3.74)
2.  Texas Rangers (3.48)
3.  San Diego Padres (3.42)

##### Most Volatile Defenses

1.  Miami Marlins (3.63)
2.  Colorado Rockies (3.58)
3.  Los Angeles Angels (3.5)

------------------------------------------------------------------------

### Runs Scored per Game

![](README_files/figure-gfm/unnamed-chunk-14-1.png)<!-- -->

------------------------------------------------------------------------

### One-Run Games

![](README_files/figure-gfm/unnamed-chunk-15-1.png)<!-- -->

------------------------------------------------------------------------

### NPR and Win Percentage

![](README_files/figure-gfm/unnamed-chunk-16-1.png)<!-- -->

------------------------------------------------------------------------

### Best Records in Last Ten Games

1.  Baltimore Orioles (8-2)
2.  New York Yankees (8-2)
3.  Seattle Mariners (8-2)
4.  Cincinnati Reds (7-3)
5.  Cleveland Guardians (7-3)
6.  Detroit Tigers (7-3)
7.  Milwaukee Brewers (6-4)
8.  Minnesota Twins (6-4)
9.  Philadelphia Phillies (6-4)
10. Arizona Diamondbacks (5-5)

------------------------------------------------------------------------

### Early Leads

![](README_files/figure-gfm/unnamed-chunk-19-1.png)<!-- -->

------------------------------------------------------------------------

### First Score Dependence

![](README_files/figure-gfm/unnamed-chunk-20-1.png)<!-- -->

------------------------------------------------------------------------

### Home Field Advantage

![](README_files/figure-gfm/unnamed-chunk-22-1.png)<!-- -->

##### Most Home-Dependent Teams

- Kansas City Royals (67.7% home / 46.7% away)
- Colorado Rockies (44.8% home / 25.8% away)
- Seattle Mariners (65.6% home / 46.7% away)

##### Better-on-the-Road Teams

- San Diego Padres (40.6% home / 59.4% away)
- Los Angeles Angels (30% home / 45.2% away)
- Boston Red Sox (41.9% home / 56.7% away)

------------------------------------------------------------------------

### Winning and Losing Streaks

- **Winning Streaks**: New York Yankees (W6), Arizona Diamondbacks (W4),
  Seattle Mariners (W4), Cincinnati Reds (W3), Detroit Tigers (W3),
  Atlanta Braves (W2), Baltimore Orioles (W2), Houston Astros (W2), Los
  Angeles Angels (W2), New York Mets (W2), Philadelphia Phillies (W2),
  Tampa Bay Rays (W2)
- **Losing Streaks**: Chicago White Sox (L12), San Francisco Giants
  (L6), Colorado Rockies (L4), Miami Marlins (L3), San Diego Padres
  (L3), Boston Red Sox (L2), Milwaukee Brewers (L2), Oakland Athletics
  (L2), St. Louis Cardinals (L2), Texas Rangers (L2), Toronto Blue Jays
  (L2), Washington Nationals (L2)

<!-- ___ -->
<!-- ### Day of Week Results -->
<!-- ```{r echo = F} -->
<!-- days_of_week = c("Sunday", "Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday") -->
<!-- ``` -->
<!-- ##### Winners -->
<!-- - -->
<!-- ##### Losers -->
<!-- - -->

------------------------------------------------------------------------

### Seven Game Windows

![](README_files/figure-gfm/unnamed-chunk-25-1.png)<!-- -->

------------------------------------------------------------------------

### Team Margins in Seven Game Windows

![](README_files/figure-gfm/unnamed-chunk-26-1.png)<!-- -->

------------------------------------------------------------------------

### Team Series Results

![](README_files/figure-gfm/unnamed-chunk-27-1.png)<!-- -->

------------------------------------------------------------------------

### Records vs. Above/Below .500 Teams

![](README_files/figure-gfm/unnamed-chunk-28-1.png)<!-- -->

------------------------------------------------------------------------

*Interested in the underlying code that builds this report?* Check it
out on GitHub:
<a href="https://github.com/chadallison/mlb24" target="_blank">mlb24</a>
