# football-data

Football datasets covering 2016–2026, built to analyse match patterns,
compare statistical probabilities with pre-match odds, and explore
live exchange trading strategies.

## Leagues

- Serie A — Italy
- Serie B — Italy, from 2016/17
- Premier League — England
- Bundesliga — Germany
- La Liga — Spain
- Ligue 1 — France
- Eredivisie — Netherlands

Actual season coverage is available in each league’s CSV.

## Available datasets

- A combined CSV containing all seven leagues.
- Separate CSV files for each league.

## Data structure

Each CSV contains 12 fixed columns. Column names remain in Italian.

| Column | Description |
|---|---|
| campionato | League |
| stagione | Season |
| data | Match date |
| casa | Home team |
| trasferta | Away team |
| gol_casa | Home team goals |
| gol_trasferta | Away team goals |
| quota_1 | Bet365 pre-match home win odds |
| quota_X | Bet365 pre-match draw odds |
| quota_2 | Bet365 pre-match away win odds |
| minuti_gol_casa_json | Home goal times as a JSON array |
| minuti_gol_trasferta_json | Away goal times as a JSON array |

All odds are pre-match decimal odds. No live odds are included.
Serie B goal times are collected manually from FBref.

## Analysis approach

Analysis considers the timing of goals, home/away status, and the
current match minute. Pre-match odds provide an additional filter.

The aim is to estimate event probabilities and corresponding fair
odds for comparison with live exchange prices.
