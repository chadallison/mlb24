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
- [Close Game Performance](#close-game-performance)
- [Runs Scored per Game](#runs-scored-per-game)
- [One-Run Games](#one-run-games)
- [NPR and Win Percentage](#npr-and-win-percentage)

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

1.  New York Yankees def. Milwaukee Brewers 15-5
2.  Houston Astros def. Colorado Rockies 8-2
3.  Minnesota Twins def. Los Angeles Angels 11-5

------------------------------------------------------------------------

### Team Volatility

![](README_files/figure-gfm/unnamed-chunk-12-1.png)<!-- -->

##### Most Volatile Teams

1.  Arizona Diamondbacks (7.3)
2.  Milwaukee Brewers (7.27)
3.  Chicago Cubs (7.21)

##### Most Volatile Offenses

1.  Arizona Diamondbacks (4.36)
2.  Boston Red Sox (3.86)
3.  New York Yankees (3.8)

##### Most Volatile Defenses

1.  Chicago Cubs (4.06)
2.  Los Angeles Angels (4.06)
3.  Milwaukee Brewers (3.86)

------------------------------------------------------------------------

### Close Game Performance

![](README_files/figure-gfm/unnamed-chunk-13-1.png)<!-- -->

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

*Interested in the underlying code that builds this report?* Check it
out on GitHub:
<a href="https://github.com/chadallison/mlb24" target="_blank">mlb24</a>

``` r
get_all_games_runs = function(team) {
  home = end_games |> filter(home_team == team) |> pull(home_score)
  away = end_games |> filter(away_team == team) |> pull(away_score)
  return(c(home, away))
}

xxx = data.frame()

for (team in all_teams) {
  yyy = data.frame(team = team, runs = get_all_games_runs(team))
  xxx = rbind(xxx, yyy)
}

xxx |>
  inner_join(xxx |>
  group_by(team) |>
  summarise(sd = sd(runs)), by = "team") |>
  ggplot(aes(reorder(team, -sd), runs)) +
  geom_boxplot(aes(fill = team), show.legend = F, outlier.alpha = 0.25) +
  coord_flip() +
  scale_fill_manual(values = team_hex) +
  labs(x = NULL, y = "Runs Scored SD") +
  scale_y_continuous(breaks = seq(0, 100, by = 2))
```

![](README_files/figure-gfm/unnamed-chunk-17-1.png)<!-- -->
