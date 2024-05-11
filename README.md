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

1.  Milwaukee Brewers def. St. Louis Cardinals 11-2
2.  Seattle Mariners def. Oakland Athletics 8-1
3.  Philadelphia Phillies def. Miami Marlins 8-2

------------------------------------------------------------------------

### Team Volatility

![](README_files/figure-gfm/unnamed-chunk-12-1.png)<!-- -->

##### Most Volatile Teams

1.  Oakland Athletics (7.42)
2.  Arizona Diamondbacks (7.17)
3.  Texas Rangers (7.01)

##### Most Volatile Offenses

1.  Arizona Diamondbacks (4.11)
2.  Texas Rangers (3.93)
3.  Boston Red Sox (3.71)

##### Most Volatile Defenses

1.  Los Angeles Angels (3.83)
2.  San Francisco Giants (3.8)
3.  Oakland Athletics (3.79)

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

1.  Baltimore Orioles (8-2)
2.  Los Angeles Dodgers (8-2)
3.  Minnesota Twins (8-2)
4.  Philadelphia Phillies (8-2)
5.  Kansas City Royals (7-3)
6.  San Diego Padres (7-3)
7.  Milwaukee Brewers (6-4)
8.  New York Yankees (6-4)
9.  Tampa Bay Rays (6-4)
10. Texas Rangers (6-4)

------------------------------------------------------------------------

*Interested in the underlying code that builds this report?* Check it
out on GitHub:
<a href="https://github.com/chadallison/mlb24" target="_blank">mlb24</a>

![](README_files/figure-gfm/unnamed-chunk-18-1.png)<!-- -->

``` r
get_game_first_score_team = function(pk) {
  x = mlb_pbp(pk) |>
    mutate(about.startTime = as_datetime(about.startTime)) |>
    filter(result.awayScore > 0 | result.homeScore > 0) |>
    slice_min(about.startTime, n = 1, with_ties = F) |>
    pull(batting_team) |>
    unlist()
  return(x[1])
}

# end_first_scores = end_games |>
#   mutate(first_scorer = sapply(game_pk, get_game_first_score_team))

end_first_scores = read_csv("data/first_scorers.csv", show_col_types = F)

new_scores = end_games |>
  filter(!game_pk %in% end_first_scores$game_pk)

if (nrow(new_scores) > 0) {
  new_first_scores = new_scores |>
    mutate(first_scorer = sapply(game_pk, get_game_first_score_team))
  
  end_first_scores = rbind(end_first_scores, new_first_scores)
}

write_csv(end_first_scores, "data/first_scorers.csv")
```

``` r
first_score_rates = end_first_scores |>
  count(first_scorer) |>
  arrange(desc(n)) |>
  rename(team = first_scorer, first_scores = n) |>
  inner_join(team_records |>
  transmute(team, gp = wins + losses, win_pct = pct), by = "team") |>
  mutate(first_score_rate = round(first_scores / gp * 100, 1))

get_team_win_pct_when_first_score = function(team) {
  data = end_first_scores |> filter(first_scorer == team)
  wins = data |> filter(win_team == team) |> nrow()
  losses = data |> filter(lose_team == team) |> nrow()
  return(round(wins / (wins + losses) * 100, 1))
}

first_score_rates |>
  mutate(win_pct_on_first_score = sapply(team, get_team_win_pct_when_first_score)) |>
  inner_join(teams_info, by = "team") |>
  ggplot(aes(first_score_rate, win_pct_on_first_score)) +
  geom_point(aes(col = team), shape = "square", size = 4, show.legend = F) +
  scale_color_manual(values = team_hex) +
  ggrepel::geom_text_repel(aes(label = abb), size = 3) +
  geom_line(stat = "smooth", method = "lm", formula = y ~ x, linetype = "dashed", alpha = 0.5) +
  geom_vline(xintercept = 50, linetype = "dotted", alpha = 0.25) +
  geom_hline(yintercept = 50, linetype = "dotted", alpha = 0.25) +
  labs(x = "First Score Rate", y = "Win Percentage When Scoring First",
       title = "Which teams capitalize on an early lead?") +
  scale_x_continuous(breaks = seq(0, 100, by = 5)) +
  scale_y_continuous(breaks = seq(0, 100, by = 5))
```

![](README_files/figure-gfm/unnamed-chunk-20-1.png)<!-- -->
