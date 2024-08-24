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
- [Rolling Ten-Game Windows](#rolling-ten-game-windows)

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

1.  Arizona Diamondbacks def. Boston Red Sox 12-2
2.  Milwaukee Brewers def. Oakland Athletics 11-3
3.  San Diego Padres def. New York Mets 7-0

------------------------------------------------------------------------

### Team Volatility

![](README_files/figure-gfm/unnamed-chunk-12-1.png)<!-- -->

##### Most Volatile Teams

1.  Oakland Athletics (6.78)
2.  Arizona Diamondbacks (6.76)
3.  Colorado Rockies (6.72)

##### Most Volatile Offenses

1.  Arizona Diamondbacks (3.65)
2.  Oakland Athletics (3.57)
3.  Minnesota Twins (3.43)

##### Most Volatile Defenses

1.  Colorado Rockies (3.41)
2.  Boston Red Sox (3.37)
3.  Toronto Blue Jays (3.25)

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

1.  Arizona Diamondbacks (7-3)
2.  Atlanta Braves (7-3)
3.  Detroit Tigers (7-3)
4.  Kansas City Royals (7-3)
5.  Los Angeles Dodgers (7-3)
6.  Milwaukee Brewers (7-3)
7.  Houston Astros (6-4)
8.  New York Mets (6-4)
9.  New York Yankees (6-4)
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

- Colorado Rockies (46.8% home / 26.9% away)
- Seattle Mariners (59.4% home / 41.5% away)
- San Francisco Giants (57.6% home / 42.2% away)

##### Better-on-the-Road Teams

- Boston Red Sox (46.8% home / 58.5% away)
- New York Yankees (54.8% home / 62.1% away)
- San Diego Padres (53.7% home / 58.7% away)

------------------------------------------------------------------------

### Winning and Losing Streaks

- **Winning Streaks**: Los Angeles Dodgers (W5), Arizona Diamondbacks
  (W4), New York Yankees (W3), St. Louis Cardinals (W3), Atlanta Braves
  (W2), Chicago Cubs (W2), Kansas City Royals (W2), Pittsburgh Pirates
  (W2), Texas Rangers (W2), Toronto Blue Jays (W2)
- **Losing Streaks**: Miami Marlins (L4), Cleveland Guardians (L3),
  Colorado Rockies (L3), Los Angeles Angels (L3), Cincinnati Reds (L2),
  Philadelphia Phillies (L2), San Francisco Giants (L2), Tampa Bay Rays
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

- Kansas City Royals (26)
- Arizona Diamondbacks (5)
- San Diego Padres (5)
- Toronto Blue Jays (5)
- Los Angeles Dodgers (4)

##### Longest Streaks of Allowing Fewer Than Five Runs

- Atlanta Braves (7)
- Los Angeles Dodgers (5)
- Washington Nationals (5)
- Texas Rangers (4)
- New York Yankees (3)

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
    ## 1   Arizona Diamondbacks  2.065
    ## 2       San Diego Padres  1.148
    ## 3     Kansas City Royals  1.004
    ## 4           Chicago Cubs  0.752
    ## 5      Milwaukee Brewers  0.730
    ## 6        Minnesota Twins  0.645
    ## 7       New York Yankees  0.507
    ## 8    Los Angeles Dodgers  0.414
    ## 9      Toronto Blue Jays  0.399
    ## 10  San Francisco Giants  0.307
    ## 11        Houston Astros  0.286
    ## 12        Tampa Bay Rays  0.224
    ## 13      Seattle Mariners  0.176
    ## 14     Baltimore Orioles -0.086
    ## 15        Atlanta Braves -0.137
    ## 16         New York Mets -0.185
    ## 17        Detroit Tigers -0.203
    ## 18   St. Louis Cardinals -0.223
    ## 19    Pittsburgh Pirates -0.266
    ## 20     Oakland Athletics -0.291
    ## 21         Miami Marlins -0.358
    ## 22        Boston Red Sox -0.393
    ## 23    Los Angeles Angels -0.420
    ## 24  Washington Nationals -0.460
    ## 25   Cleveland Guardians -0.468
    ## 26 Philadelphia Phillies -0.641
    ## 27       Cincinnati Reds -0.726
    ## 28      Colorado Rockies -0.882
    ## 29     Chicago White Sox -1.314
    ## 30         Texas Rangers -1.480

------------------------------------------------------------------------

### Rolling Ten-Game Windows

![](README_files/figure-gfm/unnamed-chunk-38-1.png)<!-- -->

``` r
get_team_all_pythag = function(tm) {
  data = end_games |>
    filter(home_team == tm | away_team == tm) |>
    mutate(my_score = ifelse(home_team == tm, home_score, away_score),
           other_score = ifelse(home_team == tm, away_score, home_score),
           pythag = (my_score ^ 2) / (my_score ^ 2 + other_score ^ 2)) |>
    transmute(team = tm, date, pythag)
  
  return(data)
}

pythag = data.frame()

for (team in all_teams) {
  new = get_team_all_pythag(tm = team)
  pythag = rbind(pythag, new)
}

hex_pct_ordered = team_records |>
  inner_join(teams_info, by = "team") |>
  arrange(desc(pct)) |>
  pull(hex)

pythag |>
  group_by(team) |>
  mutate(roll = rollapply(pythag, width = 10, FUN = "mean", align = "right", fill = NA)) |>
  ungroup() |>
  na.omit() |>
  inner_join(teams_info, by = "team") |>
  inner_join(team_records, by = "team") |>
  mutate(abb = fct_reorder(abb, -pct)) |>
  ggplot(aes(date, roll)) +
  geom_line(aes(col = abb), linewidth = 1.25, show.legend = F) +
  # geom_line(stat = "smooth", formula = y ~ x, method = "loess", se = F) +
  geom_hline(yintercept = 0.5, linetype = "dashed", alpha = 0.5) +
  scale_color_manual(values = hex_pct_ordered) +
  facet_wrap(vars(abb)) +
  theme(axis.text = element_blank()) +
  labs(x = NULL, y = "Pythagorean Win Percentage",
       title = "Season-long pythagorean win percentage in ten-game rolling windows",
       subtitle = "Average of individual games method")
```

![](README_files/figure-gfm/unnamed-chunk-40-1.png)<!-- -->

``` r
get_team_runs_scored_on = function(tm, dt) {
  data = end_games |>
    filter((home_team == tm | away_team == tm) & date == dt)
  
  if (nrow(data) == 0) return(NA)
  
  runs = data |>
    mutate(runs = ifelse(home_team == tm, home_score, away_score)) |>
    pull(runs)
  
  return(sum(runs))
}

get_team_runs_allowed_on = function(tm, dt) {
  data = end_games |>
    filter((home_team == tm | away_team == tm) & date == dt)
  
  if (nrow(data) == 0) return(NA)
  
  runs = data |>
    mutate(runs = ifelse(home_team == tm, away_score, home_score)) |>
    pull(runs)
  
  return(sum(runs))
}

scored_allowed_on_dates = crossing(team = all_teams, date = all_szn_dates) |>
  rowwise() |>
  mutate(scored = get_team_runs_scored_on(tm = team, dt = date),
         allowed = get_team_runs_allowed_on(tm = team, dt = date)) |>
  ungroup() |>
  na.omit()

scored_allowed_on_dates |>
  mutate(roll_score = rollapply(scored, width = 10, FUN = "sum", align = "right", fill = NA),
         roll_allow = rollapply(allowed, width = 10, FUN = "sum", align = "right", fill = NA),
         pythag = (roll_score ^ 2) / (roll_score ^ 2 + roll_allow ^ 2)) |>
  na.omit() |>
  inner_join(teams_info, by = "team") |>
  inner_join(team_records, by = "team") |>
  mutate(abb = fct_reorder(abb, -pct)) |>
  ggplot(aes(date, pythag)) +
  geom_line(aes(col = abb), linewidth = 1.25, show.legend = F) +
  geom_hline(yintercept = 0.5, linetype = "dashed", alpha = 0.5) +
  scale_color_manual(values = hex_pct_ordered) +
  facet_wrap(vars(abb)) +
  theme(axis.text = element_blank()) +
  labs(x = NULL, y = "Pythagorean Win Percentage in Ten-Game Window",
       title = "Season-long pythagorean win percentages in rolling ten-game windows",
       subtitle = "Aggregated runs scored / runs allowed method")
```

![](README_files/figure-gfm/unnamed-chunk-41-1.png)<!-- -->
