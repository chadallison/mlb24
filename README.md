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

1.  New York Yankees def. San Diego Padres 8-0
2.  Kansas City Royals def. Tampa Bay Rays 8-1
3.  Pittsburgh Pirates def. Atlanta Braves 11-5

------------------------------------------------------------------------

### Team Volatility

![](README_files/figure-gfm/unnamed-chunk-12-1.png)<!-- -->

##### Most Volatile Teams

1.  Oakland Athletics (6.98)
2.  Arizona Diamondbacks (6.96)
3.  Texas Rangers (6.76)

##### Most Volatile Offenses

1.  Arizona Diamondbacks (3.83)
2.  Texas Rangers (3.66)
3.  San Diego Padres (3.47)

##### Most Volatile Defenses

1.  Miami Marlins (3.74)
2.  Los Angeles Angels (3.66)
3.  Chicago Cubs (3.59)

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
3.  New York Yankees (8-2)
4.  Philadelphia Phillies (8-2)
5.  St. Louis Cardinals (8-2)
6.  Houston Astros (7-3)
7.  Miami Marlins (7-3)
8.  San Francisco Giants (7-3)
9.  Arizona Diamondbacks (5-5)
10. Baltimore Orioles (5-5)

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

- Chicago White Sox (40% home / 19.2% away)
- Colorado Rockies (45.5% home / 25% away)
- San Francisco Giants (60% home / 40.7% away)

##### Better-on-the-Road Teams

- San Diego Padres (37% home / 63% away)
- Los Angeles Angels (26.1% home / 50% away)
- Boston Red Sox (41.7% home / 59.3% away)

------------------------------------------------------------------------

### Winning and Losing Streaks

- **Winning Streaks**: Cleveland Guardians (W7), Kansas City Royals
  (W7), St. Louis Cardinals (W4), Minnesota Twins (W3), New York Yankees
  (W3), San Francisco Giants (W3), Baltimore Orioles (W2), Miami Marlins
  (W2)
- **Losing Streaks**: Tampa Bay Rays (L5), Texas Rangers (L5), New York
  Mets (L4), Chicago White Sox (L3), Los Angeles Dodgers (L3), Seattle
  Mariners (L3), Chicago Cubs (L2)

------------------------------------------------------------------------

*Interested in the underlying code that builds this report?* Check it
out on GitHub:
<a href="https://github.com/chadallison/mlb24" target="_blank">mlb24</a>

``` r
days_of_week = c("Sunday", "Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday")

print("WINNERS")
```

    ## [1] "WINNERS"

``` r
for (dw in days_of_week) {
  team = end_games |> filter(weekdays(date) == dw) |> count(win_team) |> slice_max(n, n = 1, with_ties = F) |> pull(win_team)
  print(glue("{dw}: {team}"))
}
```

    ## Sunday: Boston Red Sox
    ## Monday: Los Angeles Dodgers
    ## Tuesday: Arizona Diamondbacks
    ## Wednesday: New York Yankees
    ## Thursday: Baltimore Orioles
    ## Friday: Milwaukee Brewers
    ## Saturday: New York Yankees

``` r
print("--------------------------")
```

    ## [1] "--------------------------"

``` r
print("LOSERS")
```

    ## [1] "LOSERS"

``` r
for (dw in days_of_week) {
  team = end_games |> filter(weekdays(date) == dw) |> count(lose_team) |> slice_max(n, n = 1, with_ties = F) |> pull(lose_team)
  print(glue("{dw}: {team}"))
}
```

    ## Sunday: Colorado Rockies
    ## Monday: Miami Marlins
    ## Tuesday: Colorado Rockies
    ## Wednesday: Pittsburgh Pirates
    ## Thursday: Boston Red Sox
    ## Friday: Arizona Diamondbacks
    ## Saturday: Arizona Diamondbacks
