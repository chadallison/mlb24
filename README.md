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

1.  Toronto Blue Jays def. Minnesota Twins 15-0
2.  Tampa Bay Rays def. San Diego Padres 11-4
3.  Pittsburgh Pirates def. Cleveland Guardians 3-0

------------------------------------------------------------------------

### Team Volatility

![](README_files/figure-gfm/unnamed-chunk-12-1.png)<!-- -->

##### Most Volatile Teams

1.  Oakland Athletics (6.76)
2.  Arizona Diamondbacks (6.71)
3.  Colorado Rockies (6.71)

##### Most Volatile Offenses

1.  Arizona Diamondbacks (3.6)
2.  Oakland Athletics (3.56)
3.  Minnesota Twins (3.4)

##### Most Volatile Defenses

1.  Colorado Rockies (3.42)
2.  Pittsburgh Pirates (3.38)
3.  Boston Red Sox (3.3)

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

1.  Chicago Cubs (8-2)
2.  Los Angeles Dodgers (8-2)
3.  Atlanta Braves (7-3)
4.  Detroit Tigers (7-3)
5.  Milwaukee Brewers (7-3)
6.  New York Mets (7-3)
7.  Texas Rangers (7-3)
8.  Toronto Blue Jays (7-3)
9.  Arizona Diamondbacks (6-4)
10. Houston Astros (6-4)

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

- Colorado Rockies (47.1% home / 27.5% away)
- Seattle Mariners (59.4% home / 41.8% away)
- San Francisco Giants (57.4% home / 42% away)

##### Better-on-the-Road Teams

- Boston Red Sox (44.3% home / 58.2% away)
- New York Yankees (54.5% home / 60.9% away)
- San Diego Padres (53.6% home / 58% away)

------------------------------------------------------------------------

### Winning and Losing Streaks

- **Winning Streaks**: Chicago Cubs (W5), Milwaukee Brewers (W5),
  Houston Astros (W4), Los Angeles Dodgers (W4), New York Mets (W3)
- **Losing Streaks**: Chicago White Sox (L10), Kansas City Royals (L4),
  Arizona Diamondbacks (L3), Cincinnati Reds (L3), Washington Nationals
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

- Milwaukee Brewers (9)
- Baltimore Orioles (8)
- Colorado Rockies (8)
- St. Louis Cardinals (7)
- Pittsburgh Pirates (6)

##### Longest Streaks of Allowing Fewer Than Five Runs

- Milwaukee Brewers (5)
- Houston Astros (4)
- Toronto Blue Jays (4)
- New York Mets (3)
- Atlanta Braves (2)

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
    ## 1      Milwaukee Brewers  1.776
    ## 2           Chicago Cubs  1.467
    ## 3      Toronto Blue Jays  1.430
    ## 4         Houston Astros  1.383
    ## 5   Arizona Diamondbacks  1.308
    ## 6         Detroit Tigers  1.269
    ## 7    Los Angeles Dodgers  0.783
    ## 8       San Diego Padres  0.259
    ## 9  Philadelphia Phillies  0.139
    ## 10         New York Mets  0.128
    ## 11        Atlanta Braves  0.078
    ## 12  Washington Nationals  0.068
    ## 13  San Francisco Giants -0.096
    ## 14    Kansas City Royals -0.118
    ## 15     Oakland Athletics -0.185
    ## 16      Seattle Mariners -0.223
    ## 17      New York Yankees -0.252
    ## 18     Baltimore Orioles -0.401
    ## 19   St. Louis Cardinals -0.408
    ## 20        Tampa Bay Rays -0.422
    ## 21       Minnesota Twins -0.428
    ## 22      Colorado Rockies -0.550
    ## 23    Los Angeles Angels -0.700
    ## 24   Cleveland Guardians -0.748
    ## 25         Texas Rangers -0.888
    ## 26         Miami Marlins -0.890
    ## 27     Chicago White Sox -0.898
    ## 28        Boston Red Sox -0.928
    ## 29       Cincinnati Reds -1.064
    ## 30    Pittsburgh Pirates -1.316

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
  data = end_games |> filter((home_team == tm | away_team == tm) & date == dt)
  if (nrow(data) == 0) return(NA)
  runs = data |> mutate(runs = ifelse(home_team == tm, home_score, away_score)) |> pull(runs)
  return(sum(runs))
}

get_team_runs_allowed_on = function(tm, dt) {
  data = end_games |> filter((home_team == tm | away_team == tm) & date == dt)
  if (nrow(data) == 0) return(NA)
  runs = data |> mutate(runs = ifelse(home_team == tm, away_score, home_score)) |> pull(runs)
  return(sum(runs))
}

# this took 17s to run on 2024/08/24
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
  # geom_line(stat = "smooth", formula = y ~ x, method = "loess", se = F) +
  geom_hline(yintercept = 0.5, linetype = "dashed", alpha = 0.5) +
  scale_color_manual(values = hex_pct_ordered) +
  facet_wrap(vars(abb)) +
  theme(axis.text = element_blank()) +
  labs(x = NULL, y = "Pythagorean Win Percentage in Ten-Game Window",
       title = "Season-long pythagorean win percentages in rolling ten-game windows")
```

![](README_files/figure-gfm/unnamed-chunk-41-1.png)<!-- -->

``` r
data.frame(team = all_teams) |>
  mutate(rs = sapply(team, get_team_runs_scored),
         ra = sapply(team, get_team_runs_allowed),
         py = round((rs ^ 2) / (rs ^ 2 + ra ^ 2) * 100, 2),
         rank = as.integer(rank(-py))) |>
  arrange(rank)
```

    ##                     team  rs  ra    py rank
    ## 1      Milwaukee Brewers 665 531 61.07    1
    ## 2       New York Yankees 684 559 59.96    2
    ## 3    Los Angeles Dodgers 680 557 59.85    3
    ## 4  Philadelphia Phillies 656 547 58.99    4
    ## 5     Kansas City Royals 659 562 57.89    5
    ## 6         Houston Astros 621 537 57.22    6
    ## 7   Arizona Diamondbacks 729 643 56.24    7
    ## 8      Baltimore Orioles 679 599 56.24    7
    ## 9    Cleveland Guardians 618 551 55.71    9
    ## 10      San Diego Padres 660 594 55.25   10
    ## 11        Atlanta Braves 578 525 54.79   11
    ## 12       Minnesota Twins 636 595 53.33   12
    ## 13          Chicago Cubs 612 573 53.29   13
    ## 14         New York Mets 649 610 53.09   14
    ## 15      Seattle Mariners 542 517 52.36   15
    ## 16        Detroit Tigers 573 547 52.32   16
    ## 17       Cincinnati Reds 612 602 50.82   17
    ## 18        Boston Red Sox 658 650 50.61   18
    ## 19  San Francisco Giants 582 600 48.48   19
    ## 20    Pittsburgh Pirates 571 616 46.21   20
    ## 21         Texas Rangers 565 610 46.18   21
    ## 22     Toronto Blue Jays 587 634 46.16   22
    ## 23   St. Louis Cardinals 561 618 45.18   23
    ## 24  Washington Nationals 574 636 44.89   24
    ## 25        Tampa Bay Rays 524 588 44.26   25
    ## 26     Oakland Athletics 556 627 44.02   26
    ## 27    Los Angeles Angels 532 660 39.38   27
    ## 28      Colorado Rockies 590 796 35.46   28
    ## 29         Miami Marlins 513 700 34.94   29
    ## 30     Chicago White Sox 421 703 26.40   30
