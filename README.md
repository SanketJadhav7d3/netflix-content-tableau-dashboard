# Inside Netflix's Catalog

A Tableau Public project built on 32,000 Netflix movies and TV shows. I wanted to see where the catalog comes from, which languages dominate, how ratings have changed since 2010, and how movies compare with TV shows.

Live dashboards:
- [Inside Netflix's Catalog](https://public.tableau.com/views/InsideNetflixsCatalog-ReachLanguageandRatings/InsideNetflixsCatalog) (country, language and rating trend)
- [Movies vs TV Shows](https://public.tableau.com/views/InsideNetflixsCatalog-ReachLanguageandRatings/MoviesvsTVShows) (ratings, popularity and budget vs revenue)
- [Deep Dive - Ratings and ROI](https://public.tableau.com/views/InsideNetflixsCatalog-ReachLanguageandRatings/DeepDive-RatingsandROI) (rating by country and movie return on investment)

<img width="1500" height="1200" alt="image" src="https://github.com/user-attachments/assets/2c34924c-c4e1-406c-8df9-d071a27ba26b" />

<img width="1500" height="1200" alt="image" src="https://github.com/user-attachments/assets/7af97f9c-42d7-43d0-8a02-109008b00b90" />

## What I found

- The US accounts for 7,760 of the 32,000 titles. Europe, India, China and Japan make up most of the rest.
- English dominates with about 14,000 titles. Chinese, Japanese and Korean come next at roughly 2,000 to 3,000 each, ahead of Spanish and French (about 1,650 each).
- Average audience score rises from about 5.4 for 2010 releases to about 6.4 for 2024 releases.
- Movies score higher than TV shows (about 5.96 vs 5.42), but TV shows have a much higher popularity score (about 65 vs 20).
- Average rating differs noticeably by country. The rating map shades each country from 4.5 to 6.5.
- Movie revenue beat budget every year. Revenue divided by budget was about 2.5x in 2010, peaked near 3.5x in 2018 and 2019, dropped to about 1.45x in 2020, and was back around 2.5x by 2024.

## Things to keep in mind

- The data looks sampled. Every release year has exactly 2,000 titles, and there are exactly 16,000 movies and 16,000 TV shows, so the counts describe this sample and not Netflix's whole library.
- The 2025 numbers are odd. The average rating falls to about 2.3 and ROI to about 1.0x, probably because newer titles have few votes. I'd treat 2025 as incomplete.
- Budget and revenue only exist for movies, so the money charts leave out TV shows.
- I don't know how the popularity score is calculated, so the movie vs TV gap may partly come from different scales.
- I skipped genres. They're stored as comma-separated combinations (almost 3,900 distinct values) and I didn't split them.

## Data and tools

Fields used: country, language, release year, type, average vote, popularity, budget and revenue. Source: Netflix Movies and TV Shows dataset (add link here). Built in Tableau Public and hosted on GitHub Pages.

## If I keep going

- Split genres and compare ratings and ROI by genre.
- Filter out titles with very few votes, which would clean up 2025.
- Add country and language filters to the dashboards.
