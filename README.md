# Sports Tournament and Performance Analysis System

A beginner-friendly, menu-driven Python project (B.Tech CSE, 1st year) that loads
players' data from a CSV file, analyses it with **pandas** and draws graphs with **matplotlib**.


## Features

1. Add a new player / team (with input validation)
2. View all players
3. Search a player or team
4. Tournament standings (points table, 1 win = 3 points)
5. Top 5 performers (by Rating / Points / Win %)
6. Team-wise performance comparison
7. Player-wise win percentage
8. Statistics (average, max, min, sport-wise average)
9. Graphs: bar chart, pie chart, line chart
10. Fixture generator (random round-robin schedule)
11. Winner prediction between two teams
12. Save data to CSV

## Requirements

- Python 3.9+
- pandas, matplotlib

```bash
pip install pandas matplotlib
```

## How to run

```bash
python sports_analysis.py
```

Keep `players.csv` in the same folder as `sports_analysis.py`.

## Files

| File | Purpose |
|------|---------|
| `sports_analysis.py` | Main program |
| `players.csv` | Sample data (20 players, 4 teams, 4 sports) |

## CSV columns

`Player_Name, Team, Sport, Matches_Played, Wins, Losses, Points, Rating, Recent_Scores`

- `Points` = runs / goals / points depending on the sport
- `Recent_Scores` = last 5 match scores (space separated), used for the line chart

## Notes

- Team wins = total of its players' wins (simplified model).
- Points of different sports are not directly comparable, so ranking by Rating is the default.
- Winner prediction is a simple formula (60% average rating + 40% win %), not a guarantee.
