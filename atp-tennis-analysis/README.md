# ATP Tennis Match Analysis (2000–2023)

This project explores professional ATP tennis matches from 2000–2023 to understand match distribution, player performance, and match intensity across different surfaces.

- Original dataset: ATP Tennis 2000–2023 (Daily Pull)

## Project Overview

The goal of this analysis is to answer key questions about professional tennis play:

* Which surfaces are most commonly played?

* Which players dominate on each surface?

* How physically demanding are matches across surfaces?

This analysis is intended for beginners in SQL and data exploration, demonstrating the ability to query, aggregate, and interpret sports data.

## Analysis Steps & Key Insights
Step 1 — Matches by Surface

SELECT Surface, COUNT(*) AS total_matches
FROM tennis-analysis-481321.tennis_data.tennis_cleaned
GROUP BY Surface
ORDER BY total_matches DESC;


Purpose: Understand the distribution of professional matches across surfaces.
Insight: Hard courts dominate professional play, followed by clay and grass.

Step 2 — Wins per Player per Surface

SELECT Surface, Winner AS player, COUNT(*) AS wins
FROM tennis-analysis-481321.tennis_data.tennis_cleaned
GROUP BY Surface, player
ORDER BY Surface, wins DESC;


Purpose: Identify top-performing players on each surface.
Insight: Shows which players specialize or dominate on certain surfaces.

Step 3 — Three-Set Matches by Surface

SELECT Surface, COUNT(*) AS three_set_matches
FROM tennis-analysis-481321.tennis_data.tennis_cleaned
WHERE set3_score IS NOT NULL
GROUP BY Surface
ORDER BY three_set_matches DESC;


Purpose: Measure match intensity and endurance across surfaces.
Insight: Certain surfaces produce longer, more demanding matches.

## Key Takeaways

Surface distribution: Most matches are played on Hard courts.

Player specialization: Some players excel on specific surfaces (e.g., clay specialists).

Match intensity: Three-set matches are more common on surfaces that favor endurance and longer rallies.

## Skills Demonstrated

* SQL: COUNT, GROUP BY, ORDER BY, filtering conditions

* Data exploration and aggregation

* Sports analytics and pattern recognition

* Communicating insights in a clear, concise manner

## Optional Next Steps

Calculate win rates per player per surface

Explore tournament-level patterns

Analyze match duration and score trends over time

## Files
Powerpoint Presentation: https://github.com/imindia12/Data-Analytics-Portfolio/blob/main/atp-tennis-analysis/ATP%20Tennis%20Presentstion.pptx
