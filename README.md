# Inside Netflix's Catalog: Reach, Language and Ratings

An interactive Tableau analysis of 32,000 Netflix movies and TV shows: where the content comes from, which languages dominate, how audience ratings have changed, and how movies and TV shows compare.

**Live dashboards (Tableau Public)**
- [Inside Netflix's Catalog](https://public.tableau.com/views/InsideNetflixsCatalog-ReachLanguageandRatings/InsideNetflixsCatalog): reach, language and rating trend
- [Movies vs TV Shows](https://public.tableau.com/views/InsideNetflixsCatalog-ReachLanguageandRatings/MoviesvsTVShows): ratings, popularity and movie economics

<img width="1500" height="1200" alt="image" src="https://github.com/user-attachments/assets/2c34924c-c4e1-406c-8df9-d071a27ba26b" />

<img width="1500" height="1200" alt="image" src="https://github.com/user-attachments/assets/7af97f9c-42d7-43d0-8a02-109008b00b90" />



## Questions explored

1. **Where does the content come from?** Proportional-symbol map of titles by country (103 countries).
2. **Which languages dominate?** Sorted bar chart of titles by language.
3. **Are titles rated higher over time?** Average audience score by release year, 2010-2025.
4. **Do movies or TV shows score higher?** Average audience score by type.
5. **Which is more popular?** Average popularity score by type.
6. **How do movie budgets compare with revenue?** Total budget vs revenue by release year (movies only).

## Key findings

- **The catalog is US-heavy.** The United States accounts for 7,760 of the 32,000 titles, with further clusters in Europe, India, China and Japan.
- **English dominates; East Asia leads the rest.** English accounts for about 14,000 titles. Chinese, Japanese and Korean add roughly 2,000-3,000 each, ahead of Spanish and French (about 1,650 each).
- **Audience ratings trend upward.** The average score rises from about 5.4 for 2010 releases to about 6.4 for 2024 releases.
- **Movies score higher, TV shows score as more popular.** Movies average about 5.96 on audience score versus about 5.42 for TV shows. On the dataset's popularity score, TV shows average about 65 versus about 20 for movies.
- **Movie revenue outpaces budget, with a 2020 dip.** From 2010 to 2019, total revenue runs at roughly 2.5-3x total budget, peaking near $33B in 2017. Both fall sharply in 2020 and recover unevenly afterwards.

## Data notes and caveats

- **The data looks sampled.** It has exactly 16,000 movies, 16,000 TV shows and 2,000 titles per release year (2010-2025), so counts describe this sample, not Netflix's full library.
- **2025 is an outlier.** Its average rating drops to about 2.3, which likely reflects recent titles with few or no votes rather than a real decline.
- **Budget and revenue exist only for movies.** TV rows are empty, so the economics chart does not cover TV shows.
- **The popularity score is a field in the dataset.** I did not verify how it is calculated, so the movie vs TV gap may partly reflect different scales.
- **Genres were not analyzed.** They are stored as comma-separated combinations (3,896 distinct values) and would need to be split first.
- Fields used: `country`, `language`, `release_year`, `type`, `vote_average`, `popularity`, `budget`, `revenue`.
- Source: Netflix Movies and TV Shows dataset (add your source link here).

## Tools

Tableau Public (map, bar charts, two dashboards), hosted on GitHub Pages.

## Possible next steps

- Split the `genres` field and compare ratings and revenue by genre.
- Exclude or annotate 2025 and titles with very few votes.
- Compute return on investment (revenue / budget) per movie and per year.
- Add country and language filters to the dashboards.
