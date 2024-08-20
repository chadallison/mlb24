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

1.  Arizona Diamondbacks def. Miami Marlins 9-6
2.  Cincinnati Reds def. Toronto Blue Jays 6-3
3.  Oakland Athletics def. Tampa Bay Rays 3-0

------------------------------------------------------------------------

### Team Volatility

![](README_files/figure-gfm/unnamed-chunk-12-1.png)<!-- -->

##### Most Volatile Teams

1.  Oakland Athletics (6.78)
2.  Colorado Rockies (6.74)
3.  Arizona Diamondbacks (6.72)

##### Most Volatile Offenses

1.  Arizona Diamondbacks (3.61)
2.  Oakland Athletics (3.6)
3.  Minnesota Twins (3.41)

##### Most Volatile Defenses

1.  Colorado Rockies (3.42)
2.  Boston Red Sox (3.33)
3.  Atlanta Braves (3.27)

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

1.  Houston Astros (9-1)
2.  Arizona Diamondbacks (7-3)
3.  Kansas City Royals (7-3)
4.  Los Angeles Dodgers (7-3)
5.  Milwaukee Brewers (7-3)
6.  Oakland Athletics (7-3)
7.  San Diego Padres (7-3)
8.  Atlanta Braves (6-4)
9.  Chicago Cubs (6-4)
10. Detroit Tigers (6-4)

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

- Colorado Rockies (46.8% home / 27% away)
- Seattle Mariners (58.7% home / 42.9% away)
- San Francisco Giants (57.8% home / 42.9% away)

##### Better-on-the-Road Teams

- Boston Red Sox (47.5% home / 57.1% away)
- New York Yankees (53.4% home / 62.1% away)
- San Diego Padres (54% home / 58.7% away)

------------------------------------------------------------------------

### Winning and Losing Streaks

- **Winning Streaks**: Kansas City Royals (W5), Milwaukee Brewers (W5),
  Houston Astros (W3), Atlanta Braves (W2), Detroit Tigers (W2), Los
  Angeles Dodgers (W2), San Francisco Giants (W2), Texas Rangers (W2)
- **Losing Streaks**: Chicago White Sox (L3), Cleveland Guardians (L3),
  Los Angeles Angels (L3), Boston Red Sox (L2), Minnesota Twins (L2),
  New York Yankees (L2), Pittsburgh Pirates (L2)

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

- Kansas City Royals (23)
- Colorado Rockies (9)
- Minnesota Twins (5)
- Philadelphia Phillies (5)
- Pittsburgh Pirates (4)

##### Longest Streaks of Allowing Fewer Than Five Runs

- Detroit Tigers (13)
- Kansas City Royals (5)
- Milwaukee Brewers (5)
- New York Yankees (5)
- New York Mets (4)

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
    ## 1   Arizona Diamondbacks  1.920
    ## 2       San Diego Padres  1.878
    ## 3     Kansas City Royals  0.980
    ## 4   San Francisco Giants  0.864
    ## 5        Minnesota Twins  0.734
    ## 6           Chicago Cubs  0.620
    ## 7      Milwaukee Brewers  0.504
    ## 8         Tampa Bay Rays  0.493
    ## 9          New York Mets  0.386
    ## 10        Houston Astros  0.300
    ## 11        Detroit Tigers  0.210
    ## 12         Miami Marlins  0.137
    ## 13     Oakland Athletics  0.066
    ## 14      Seattle Mariners  0.028
    ## 15   Los Angeles Dodgers  0.002
    ## 16     Toronto Blue Jays  0.000
    ## 17   Cleveland Guardians -0.077
    ## 18      New York Yankees -0.106
    ## 19       Cincinnati Reds -0.115
    ## 20     Baltimore Orioles -0.241
    ## 21    Los Angeles Angels -0.248
    ## 22      Colorado Rockies -0.403
    ## 23        Boston Red Sox -0.452
    ## 24        Atlanta Braves -0.505
    ## 25    Pittsburgh Pirates -0.519
    ## 26 Philadelphia Phillies -0.687
    ## 27   St. Louis Cardinals -0.977
    ## 28  Washington Nationals -1.158
    ## 29         Texas Rangers -1.229
    ## 30     Chicago White Sox -1.626

``` r
get_team_result_on_date = function(tm, dt) {
  data = end_games |> filter(date == dt & (home_team == tm | away_team == tm))
  if (nrow(data) == 0) return("DNP")
  if (data$win_team[1] == tm) return("Win")
  if (data$lose_team[1] == tm) return("Loss")
}

team_results_dates_raw = crossing(team = all_teams, date = unique(end_games$date)) |>
  arrange(team, date) |>
  rowwise() |>
  mutate(result = get_team_result_on_date(tm = team, dt = date)) |>
  ungroup()

team_results_dates = team_results_dates_raw |>
  filter(result != "DNP") |>
  group_by(team) |>
  mutate(game_num = row_number()) |>
  ungroup()

team_results_dates
```

    ## # A tibble: 3,694 × 4
    ##    team                 date       result game_num
    ##    <chr>                <date>     <chr>     <int>
    ##  1 Arizona Diamondbacks 2024-03-28 Win           1
    ##  2 Arizona Diamondbacks 2024-03-29 Win           2
    ##  3 Arizona Diamondbacks 2024-03-30 Loss          3
    ##  4 Arizona Diamondbacks 2024-03-31 Win           4
    ##  5 Arizona Diamondbacks 2024-04-01 Loss          5
    ##  6 Arizona Diamondbacks 2024-04-02 Win           6
    ##  7 Arizona Diamondbacks 2024-04-03 Loss          7
    ##  8 Arizona Diamondbacks 2024-04-05 Loss          8
    ##  9 Arizona Diamondbacks 2024-04-06 Loss          9
    ## 10 Arizona Diamondbacks 2024-04-07 Loss         10
    ## # ℹ 3,684 more rows
