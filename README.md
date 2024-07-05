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

1.  Chicago Cubs def. Philadelphia Phillies 10-2
2.  Arizona Diamondbacks def. Los Angeles Dodgers 9-3
3.  Oakland Athletics def. Los Angeles Angels 5-0

------------------------------------------------------------------------

### Team Volatility

![](README_files/figure-gfm/unnamed-chunk-12-1.png)<!-- -->

##### Most Volatile Teams

1.  Arizona Diamondbacks (6.92)
2.  Colorado Rockies (6.76)
3.  Texas Rangers (6.61)

##### Most Volatile Offenses

1.  Arizona Diamondbacks (3.61)
2.  San Diego Padres (3.44)
3.  New York Mets (3.42)

##### Most Volatile Defenses

1.  Colorado Rockies (3.56)
2.  Los Angeles Angels (3.38)
3.  Texas Rangers (3.35)

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

1.  Houston Astros (8-2)
2.  Boston Red Sox (7-3)
3.  Milwaukee Brewers (7-3)
4.  Minnesota Twins (7-3)
5.  San Diego Padres (7-3)
6.  San Francisco Giants (7-3)
7.  Tampa Bay Rays (7-3)
8.  Baltimore Orioles (6-4)
9.  Cincinnati Reds (6-4)
10. Kansas City Royals (6-4)

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

- Seattle Mariners (64.4% home / 43.2% away)
- Oakland Athletics (47.7% home / 26.7% away)
- Kansas City Royals (62.5% home / 42.5% away)

##### Better-on-the-Road Teams

- Boston Red Sox (46.5% home / 62.8% away)
- New York Mets (45.7% home / 53.8% away)
- Tampa Bay Rays (47.9% home / 53.8% away)

------------------------------------------------------------------------

### Winning and Losing Streaks

- **Winning Streaks**: Boston Red Sox (W4), Cincinnati Reds (W3),
  Oakland Athletics (W3), Arizona Diamondbacks (W2), Houston Astros
  (W2), San Diego Padres (W2), Washington Nationals (W2)
- **Losing Streaks**: Los Angeles Angels (L4), Miami Marlins (L4), New
  York Yankees (L3), Los Angeles Dodgers (L2), New York Mets (L2), Texas
  Rangers (L2), Toronto Blue Jays (L2)

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

##### Longest Streaks of Scoring Two or More Runs

- Minnesota Twins (22)
- Milwaukee Brewers (21)
- Los Angeles Dodgers (18)
- Houston Astros (14)
- Baltimore Orioles (10)

##### Longest Streaks of Allowing Fewer Than Five Runs

- Cincinnati Reds (7)
- San Francisco Giants (4)
- Colorado Rockies (3)
- Milwaukee Brewers (3)
- Seattle Mariners (3)

------------------------------------------------------------------------

### WORK IN PROGRESS

Coming soon …

``` r
get_date_tenth_last_game = function(team) {
  date = end_games |>
    filter(home_team == team | away_team == team) |>
    slice_max(date, n = 10, with_ties = F) |>
    slice_min(date, n = 1, with_ties = F) |>
    pull(date)
  
  return(as.character(date))
}

teams_tenth_last = data.frame(team = all_teams) |>
  mutate(tenth_date = as_date(sapply(team, get_date_tenth_last_game)))

teams_tenth_last |>
  rowwise() |>
  mutate(npr_past = get_npr_on(team = team, dt = tenth_date)) |>
  ungroup() |>
  inner_join(team_npr |>
  distinct(team, total_npr), by = "team")
```

    ## # A tibble: 30 × 4
    ##    team                 tenth_date npr_past total_npr
    ##    <chr>                <date>        <dbl>     <dbl>
    ##  1 Arizona Diamondbacks 2024-06-23   -7.27      -0.03
    ##  2 Atlanta Braves       2024-06-24   22.0        0.23
    ##  3 Baltimore Orioles    2024-06-24   58.0        0.64
    ##  4 Boston Red Sox       2024-06-22   27.9        0.23
    ##  5 Chicago Cubs         2024-06-24  -10.8       -0.13
    ##  6 Chicago White Sox    2024-06-24  -77.5       -0.71
    ##  7 Cincinnati Reds      2024-06-24   12.4        0.2 
    ##  8 Cleveland Guardians  2024-06-24   49.0        0.42
    ##  9 Colorado Rockies     2024-06-23  -56.9       -0.8 
    ## 10 Detroit Tigers       2024-06-23    0.230     -0.11
    ## # ℹ 20 more rows
