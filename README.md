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

1.  St. Louis Cardinals def. Cincinnati Reds 7-1
2.  Cleveland Guardians def. Colorado Rockies 13-7
3.  Boston Red Sox def. Baltimore Orioles 8-3

------------------------------------------------------------------------

### Team Volatility

![](README_files/figure-gfm/unnamed-chunk-12-1.png)<!-- -->

##### Most Volatile Teams

1.  Oakland Athletics (6.89)
2.  Arizona Diamondbacks (6.85)
3.  Colorado Rockies (6.66)

##### Most Volatile Offenses

1.  Arizona Diamondbacks (3.78)
2.  Texas Rangers (3.57)
3.  San Diego Padres (3.4)

##### Most Volatile Defenses

1.  Miami Marlins (3.68)
2.  Los Angeles Angels (3.57)
3.  Colorado Rockies (3.56)

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
2.  San Francisco Giants (8-2)
3.  St. Louis Cardinals (8-2)
4.  Kansas City Royals (7-3)
5.  Boston Red Sox (6-4)
6.  Minnesota Twins (6-4)
7.  New York Yankees (6-4)
8.  Philadelphia Phillies (6-4)
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

- Kansas City Royals (71.4% home / 48.1% away)
- San Francisco Giants (63% home / 41.4% away)
- Colorado Rockies (46.2% home / 25% away)

##### Better-on-the-Road Teams

- Los Angeles Angels (26.9% home / 50% away)
- San Diego Padres (41.9% home / 63% away)
- Boston Red Sox (42.3% home / 58.6% away)

------------------------------------------------------------------------

### Winning and Losing Streaks

- **Winning Streaks**: Detroit Tigers (W3), San Diego Padres (W3),
  Seattle Mariners (W3), Los Angeles Dodgers (W2), Minnesota Twins (W2),
  San Francisco Giants (W2), Texas Rangers (W2), Toronto Blue Jays (W2)
- **Losing Streaks**: Chicago White Sox (L7), Kansas City Royals (L3),
  Philadelphia Phillies (L3), Arizona Diamondbacks (L2), Houston Astros
  (L2), Miami Marlins (L2), New York Mets (L2), New York Yankees (L2)

------------------------------------------------------------------------

*Interested in the underlying code that builds this report?* Check it
out on GitHub:
<a href="https://github.com/chadallison/mlb24" target="_blank">mlb24</a>

    ## [1] "Most Frequent Winners on Each Day of Week"

    ## Sunday: Boston Red Sox
    ## Monday: Toronto Blue Jays
    ## Tuesday: Los Angeles Dodgers
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

### “Groups of Seven” Records

![](README_files/figure-gfm/unnamed-chunk-26-1.png)<!-- -->

``` r
get_seven_window_margin = function(team, group) {
  data = end_games |> filter(home_team == team | away_team == team) |> arrange(date)
  data$seven_group = seven_seq[1:nrow(data)]
  data = data |> filter(seven_group == group)
  if (nrow(data) == 0) return(NA)
  
  margin = data |>
    mutate(team_score = ifelse(home_team == team, home_score, away_score),
           opp_score = ifelse(home_team == team, away_score, home_score),
           margin = team_score - opp_score) |>
    summarise(x = sum(margin)) |>
    pull(x)
  
  return(margin)
}

crossing(team = all_teams, seven_group = 1:upper_lim) |>
  rowwise() |>
  mutate(margin = get_seven_window_margin(team, seven_group)) |>
  ungroup() |>
  filter(!is.na(margin)) |>
  inner_join(teams_info, by = "team") |>
  ggplot(aes(seven_group, 1)) +
  geom_col(aes(fill = margin), show.legend = F) +
  facet_wrap(vars(abb), scale = "free") +
  theme(axis.text = element_blank()) +
  scale_fill_gradient(low = "indianred3", high = "springgreen4") +
  labs(x = NULL, y = NULL,
       title = "Team Margins in Seven-Game Windows")
```

![](README_files/figure-gfm/unnamed-chunk-27-1.png)<!-- -->

``` r
get_series_data = function(team, series) {
  x = end_games |>
    filter(home_team == team | away_team == team) |>
    arrange(date) |>
    mutate(my_team = ifelse(home_team == team, home_team, away_team),
           opp_team = ifelse(home_team == team, away_team, home_team))
  
  x$series_num = NA
  x$series_num[1] = 1
  
  for (i in 2:nrow(x)) {
    if (x$opp_team[i] == x$opp_team[i - 1]) {
      x$series_num[i] = x$series_num[i - 1]
    } else {
      x$series_num[i] = x$series_num[i - 1] + 1
    }
  }
  
  data = x |> filter(series_num == series)
  if (nrow(data) == 0) return(NA)
  wins = data |> filter(win_team == team) |> nrow()
  losses = data |> filter(lose_team == team) |> nrow()
  
  if (wins > losses) {
    return("Series Win")
  } else if (wins < losses) {
    return("Series Loss")
  } else {
    return("Series Tied or In Progress")
  }
  
  return(x)
}

upper_lim = ceiling(team_records |>
  transmute(gp = wins + losses) |>
  slice_max(gp, n = 1, with_ties = F) |>
  pull(gp) / 2)

team_series_results = crossing(team = all_teams, series = 1:upper_lim) |>
  rowwise() |>
  mutate(wl = get_series_data(team, series)) |>
  ungroup() |>
  filter(!is.na(wl))

team_series_results |>
  ggplot(aes(series, 1)) +
  geom_col(aes(fill = wl), width = 0.75, position = "dodge") +
  facet_wrap(vars(team), scales = "free") +
  scale_fill_manual(values = c("indianred3", "black", "springgreen4")) +
  theme(axis.text = element_blank())
```

![](README_files/figure-gfm/unnamed-chunk-28-1.png)<!-- -->
