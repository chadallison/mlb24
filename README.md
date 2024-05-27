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

1.  Atlanta Braves def. Pittsburgh Pirates 8-1
2.  Seattle Mariners def. Washington Nationals 9-5
3.  Texas Rangers def. Minnesota Twins 6-2

------------------------------------------------------------------------

### Team Volatility

![](README_files/figure-gfm/unnamed-chunk-12-1.png)<!-- -->

##### Most Volatile Teams

1.  Arizona Diamondbacks (6.9)
2.  Oakland Athletics (6.89)
3.  Texas Rangers (6.66)

##### Most Volatile Offenses

1.  Arizona Diamondbacks (3.8)
2.  Texas Rangers (3.6)
3.  San Diego Padres (3.44)

##### Most Volatile Defenses

1.  Miami Marlins (3.73)
2.  Los Angeles Angels (3.59)
3.  Chicago Cubs (3.54)

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

1.  Cleveland Guardians (9-1)
2.  Kansas City Royals (8-2)
3.  San Francisco Giants (8-2)
4.  St. Louis Cardinals (8-2)
5.  Miami Marlins (7-3)
6.  New York Yankees (7-3)
7.  Philadelphia Phillies (7-3)
8.  Houston Astros (6-4)
9.  Pittsburgh Pirates (6-4)
10. San Diego Padres (6-4)

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

- Colorado Rockies (45.8% home / 25% away)
- Kansas City Royals (71.4% home / 52% away)
- San Francisco Giants (60% home / 41.4% away)

##### Better-on-the-Road Teams

- Los Angeles Angels (24% home / 50% away)
- San Diego Padres (37.9% home / 63% away)
- Boston Red Sox (42.3% home / 59.3% away)

------------------------------------------------------------------------

### Winning and Losing Streaks

- **Winning Streaks**: Cleveland Guardians (W9), St. Louis Cardinals
  (W6), Baltimore Orioles (W4), Cincinnati Reds (W3), Detroit Tigers
  (W3)
- **Losing Streaks**: Chicago White Sox (L5), Los Angeles Dodgers (L5),
  Chicago Cubs (L4), Los Angeles Angels (L3), Toronto Blue Jays (L3)

------------------------------------------------------------------------

*Interested in the underlying code that builds this report?* Check it
out on GitHub:
<a href="https://github.com/chadallison/mlb24" target="_blank">mlb24</a>

    ## [1] "Most Frequent Winners on Each Day of Week"

    ## Sunday: Boston Red Sox
    ## Monday: Los Angeles Dodgers
    ## Tuesday: Arizona Diamondbacks
    ## Wednesday: New York Yankees
    ## Thursday: Baltimore Orioles
    ## Friday: Milwaukee Brewers
    ## Saturday: New York Yankees

    ## [1] "--------------------------"

    ## [1] "Most Frequent Losers on Each Day of Week"

    ## Sunday: Chicago White Sox
    ## Monday: Miami Marlins
    ## Tuesday: Colorado Rockies
    ## Wednesday: Pittsburgh Pirates
    ## Thursday: Boston Red Sox
    ## Friday: Arizona Diamondbacks
    ## Saturday: New York Mets

### “Groups of Five” Records

    ## [1] 50

![](README_files/figure-gfm/unnamed-chunk-26-1.png)<!-- -->
