Chad’s 2024 MLB Report
================

*Interested in the underlying code that builds this report?* Check it
out on GitHub:
<a href="https://github.com/chadallison/mlb24" target="_blank">mlb24</a>

------------------------------------------------------------------------

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
- [Pythagorean Wins](#pythagorean-wins)
- [Season Long NPR Trends](#season-long-npr-trends)
- [Season Long Pythagorean Trends](#season-long-pythagorean-trends)
- [Runs Scored and Allowed Streaks](#runs-scored-and-allowed-streaks)
- [Team NPR Trends in Past Ten
  Games](#team-npr-trends-in-past-ten-games)
- [First Inning Score Rates](#first-inning-score-rates)
- [One Run vs. Multi Run Games](#one-run-vs.-multi-run-games)

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
interpretability.

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

1.  Philadelphia Phillies def. Washington Nationals 13-3
2.  San Francisco Giants def. Atlanta Braves 6-0
3.  Baltimore Orioles def. Boston Red Sox 5-1

------------------------------------------------------------------------

### Team Volatility

![](README_files/figure-gfm/unnamed-chunk-12-1.png)<!-- -->

##### Most Volatile Teams

1.  Oakland Athletics (6.8)
2.  Colorado Rockies (6.78)
3.  Arizona Diamondbacks (6.77)

##### Most Volatile Offenses

1.  Oakland Athletics (3.64)
2.  Arizona Diamondbacks (3.63)
3.  Minnesota Twins (3.46)

##### Most Volatile Defenses

1.  Colorado Rockies (3.43)
2.  Boston Red Sox (3.33)
3.  Atlanta Braves (3.3)

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

1.  Arizona Diamondbacks (9-1)
2.  San Diego Padres (9-1)
3.  Houston Astros (8-2)
4.  Cincinnati Reds (7-3)
5.  Milwaukee Brewers (7-3)
6.  Baltimore Orioles (6-4)
7.  Detroit Tigers (6-4)
8.  Los Angeles Dodgers (6-4)
9.  New York Yankees (6-4)
10. Oakland Athletics (6-4)

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

- Colorado Rockies (45.8% home / 27% away)
- Seattle Mariners (58.7% home / 44.1% away)
- San Francisco Giants (57.1% home / 42.6% away)

##### Better-on-the-Road Teams

- Boston Red Sox (47.5% home / 57.6% away)
- New York Yankees (53.4% home / 63.5% away)
- San Diego Padres (53.2% home / 60% away)

------------------------------------------------------------------------

### Winning and Losing Streaks

- **Winning Streaks**: Houston Astros (W8), Arizona Diamondbacks (W6),
  Cleveland Guardians (W5), Cincinnati Reds (W4), Detroit Tigers (W4),
  San Diego Padres (W3), Toronto Blue Jays (W3), Baltimore Orioles (W2),
  Milwaukee Brewers (W2), New York Yankees (W2), Philadelphia Phillies
  (W2)
- **Losing Streaks**: Pittsburgh Pirates (L10), St. Louis Cardinals
  (L4), Chicago Cubs (L3), Colorado Rockies (L3), Los Angeles Angels
  (L3), Seattle Mariners (L3), Tampa Bay Rays (L3), Boston Red Sox (L2),
  Chicago White Sox (L2), Los Angeles Dodgers (L2), Washington Nationals
  (L2)

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

## Records vs. Above/Below .500 Teams

![](README_files/figure-gfm/unnamed-chunk-28-1.png)<!-- -->

------------------------------------------------------------------------

### Pythagorean Wins

![](README_files/figure-gfm/unnamed-chunk-29-1.png)<!-- -->

------------------------------------------------------------------------

### Season Long NPR Trends

![](README_files/figure-gfm/unnamed-chunk-30-1.png)<!-- -->

------------------------------------------------------------------------

### Season Long Pythagorean Trends

![](README_files/figure-gfm/unnamed-chunk-31-1.png)<!-- -->

------------------------------------------------------------------------

### Runs Scored and Allowed Streaks

##### Longest Streaks of Scoring Three or More Runs

- Kansas City Royals (19)
- Arizona Diamondbacks (11)
- Los Angeles Dodgers (8)
- Colorado Rockies (6)
- Cincinnati Reds (4)

##### Longest Streaks of Allowing Fewer Than Five Runs

- Detroit Tigers (10)
- Houston Astros (10)
- Cincinnati Reds (5)
- Minnesota Twins (4)
- Arizona Diamondbacks (3)

------------------------------------------------------------------------

### Team NPR Trends in Past Ten Games

![](README_files/figure-gfm/unnamed-chunk-34-1.png)<!-- -->

------------------------------------------------------------------------

### First Inning Score Rates

![](README_files/figure-gfm/unnamed-chunk-35-1.png)<!-- -->

------------------------------------------------------------------------

### One Run vs. Multi Run Games

![](README_files/figure-gfm/unnamed-chunk-36-1.png)<!-- -->

------------------------------------------------------------------------

``` r
get_npr_last_25 = function(team) {
  return(end_npr |>
    filter(home_team == team | away_team == team) |>
    slice_max(date, n = 25, with_ties = F) |>
    mutate(my_off_npr = ifelse(home_team == team, home_off_npr, away_off_npr),
           my_def_npr = ifelse(home_team == team, home_def_npr, away_def_npr)) |>
    summarise(total_npr = round(sum(my_off_npr + my_def_npr) / 25, 3)) |>
    pull(total_npr))
}

data.frame(team = all_teams) |>
  mutate(last25 = sapply(team, get_npr_last_25)) |>
  arrange(desc(last25))
```

    ##                     team last25
    ## 1   Arizona Diamondbacks  2.072
    ## 2       San Diego Padres  1.962
    ## 3      Oakland Athletics  1.200
    ## 4   San Francisco Giants  0.738
    ## 5      Milwaukee Brewers  0.730
    ## 6         Tampa Bay Rays  0.695
    ## 7        Minnesota Twins  0.624
    ## 8           Chicago Cubs  0.606
    ## 9          Miami Marlins  0.557
    ## 10    Kansas City Royals  0.404
    ## 11   Los Angeles Dodgers  0.267
    ## 12       Cincinnati Reds  0.245
    ## 13        Houston Astros  0.201
    ## 14        Detroit Tigers  0.196
    ## 15         New York Mets  0.181
    ## 16      Seattle Mariners -0.016
    ## 17     Toronto Blue Jays -0.086
    ## 18      New York Yankees -0.220
    ## 19      Colorado Rockies -0.265
    ## 20     Baltimore Orioles -0.274
    ## 21    Pittsburgh Pirates -0.344
    ## 22    Los Angeles Angels -0.350
    ## 23   Cleveland Guardians -0.486
    ## 24 Philadelphia Phillies -0.685
    ## 25   St. Louis Cardinals -0.767
    ## 26  Washington Nationals -0.774
    ## 27        Boston Red Sox -0.930
    ## 28        Atlanta Braves -1.033
    ## 29         Texas Rangers -1.269
    ## 30     Chicago White Sox -2.073
