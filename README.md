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
- [Pythagorean Wins](#pythagorean-wins)

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

1.  Detroit Tigers def. Milwaukee Brewers 10-2
2.  Baltimore Orioles def. Tampa Bay Rays 9-2
3.  Minnesota Twins def. Pittsburgh Pirates 11-5

------------------------------------------------------------------------

### Team Volatility

![](README_files/figure-gfm/unnamed-chunk-12-1.png)<!-- -->

##### Most Volatile Teams

1.  Arizona Diamondbacks (6.86)
2.  Oakland Athletics (6.67)
3.  Colorado Rockies (6.57)

##### Most Volatile Offenses

1.  Arizona Diamondbacks (3.67)
2.  San Diego Padres (3.54)
3.  Boston Red Sox (3.48)

##### Most Volatile Defenses

1.  Colorado Rockies (3.57)
2.  Miami Marlins (3.56)
3.  Los Angeles Angels (3.43)

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

1.  Cincinnati Reds (8-2)
2.  New York Yankees (8-2)
3.  Baltimore Orioles (7-3)
4.  Philadelphia Phillies (7-3)
5.  Arizona Diamondbacks (6-4)
6.  Cleveland Guardians (6-4)
7.  Houston Astros (6-4)
8.  Los Angeles Dodgers (6-4)
9.  Milwaukee Brewers (6-4)
10. New York Mets (6-4)

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

- Seattle Mariners (65.6% home / 45.7% away)
- Chicago White Sox (35.3% home / 16.1% away)
- Kansas City Royals (67.6% home / 48.4% away)

##### Better-on-the-Road Teams

- San Diego Padres (41.7% home / 57.6% away)
- New York Mets (37.1% home / 51.7% away)
- Los Angeles Angels (32.4% home / 45.2% away)

------------------------------------------------------------------------

### Winning and Losing Streaks

- **Winning Streaks**: Baltimore Orioles (W3), Washington Nationals
  (W3), Cleveland Guardians (W2), Toronto Blue Jays (W2)
- **Losing Streaks**: Atlanta Braves (L3), Tampa Bay Rays (L3), Miami
  Marlins (L2), Oakland Athletics (L2)

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

*Interested in the underlying code that builds this report?* Check it
out on GitHub:
<a href="https://github.com/chadallison/mlb24" target="_blank">mlb24</a>

``` r
get_npr_on = function(team, dt) {
  return(end_npr |>
    filter((home_team == team | away_team == team) & date <= dt) |>
    mutate(team_npr = ifelse(home_team == team, home_off_npr + home_def_npr, away_off_npr + away_def_npr)) |>
    summarise(npr = sum(team_npr)) |>
    pull(npr))
}

all_szn_dates = seq.Date(from = min(end_games$date), to = Sys.Date(), by = 1)

npr_on_dates = crossing(team = all_teams, date = all_szn_dates) |>
  rowwise() |>
  mutate(npr_on_date = get_npr_on(team = team, dt = date)) |>
  ungroup()

npr_on_dates = npr_on_dates |>
  inner_join(teams_info, by = "team") |>
  inner_join(team_divisons, by = "team")

last_dates = npr_on_dates |>
  group_by(team) |>
  filter(date == max(date)) |>
  ungroup()

npr_on_dates |>
  ggplot(aes(date, npr_on_date)) +
  geom_line(aes(col = team), linewidth = 1.25, show.legend = F) +
  scale_color_manual(values = team_hex) +
  theme(axis.text = element_blank()) +
  facet_wrap(vars(division)) +
  labs(x = NULL, y = NULL, title = "Season-Long Team NPR Trends") +
  ggrepel::geom_text_repel(aes(label = abb, col = team),
                           data = last_dates, segment.alpha = 0, nudge_x = 10, direction = "y", hjust = 0, size = 3, show.legend = F)
```

![](README_files/figure-gfm/unnamed-chunk-30-1.png)<!-- -->
