# Premier League Champion Blueprint

## Overview
This project explores which specific metrics are most important for predicting a team's success in the Premier League, using live 2025/26 season standings data.

## Author
Harley Lainez-Murillo — DTSC 2301-001
Project 1: Defining a Data Science Problem & Understanding Data

## Goal
To identify which metrics are the strongest indicators of a team's performance and standing across a Premier League season.

## Data Source
Live Premier League table data scraped from the BBC Sport website (as of 02/23/2026) using `pandas.read_html()`. The dataset covers all 20 teams with the following fields:
- Matches Played
- Won / Drawn / Lost
- Goals Forward (renamed from "Goals For")
- Goals Against
- Goal Difference
- Points
- Form (last 6 games)

## Approach
1. **Data Collection** — Scraped the current Premier League standings table directly from BBC Sport.
2. **Data Cleaning** — Renamed columns for clarity (e.g., "Goals For" → "Goals Forward").
3. **Feature Engineering** — Calculated a Pythagorean expectation metric (`Pyth`) to estimate each team's expected win percentage based on goals scored vs. goals allowed, independent of actual results.
4. **Visualization** — Plotted Form vs. League Position to examine whether current league leaders were also the teams in the best recent form.

## Key Finding
Goals Forward and Goal Difference emerged as the strongest indicators of a team's performance across the season, more predictive of final standing than short-term form alone.
