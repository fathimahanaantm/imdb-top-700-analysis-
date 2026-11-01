# IMDb Top 700: Decoding What Makes a Movie Timeless

Exploratory data analysis of IMDb's Top 700 films to understand which factors (genre, decade, director, cast, votes, runtime, country) are linked to a high Bayesian-weighted IMDb rating.

**Live dashboard:** [Tableau Public](https://public.tableau.com/views/NL_IMDbTop700_17912856364920/DecodingWhatMakesaMovieTimeless)

## Key Metric
**Average IMDb Rating**, with three supporting KPIs: Average Votes per Film, Director Frequency, and Country Representation Rate.

## Dataset
700 films and 10 columns (Rank, Title, Year, Genre(s), Director, Main Actor(s), Country, IMDb Rating, Votes, Runtime), covering 1921 to 2026.

## Approach
1. Defined the key metric, KPIs and 7 testable hypotheses
2. Inspected and cleaned the data (missing actors, repeated names, duplicates)
3. Kept all outliers (IQR rule) because they are genuine classics and epics
4. Normalised Votes and Runtime (min-max)
5. EDA by genre, decade, director, actor, country, votes and runtime
6. Hypothesis testing (Welch's t-test, ANOVA, correlation)
7. Built an interactive Tableau dashboard with a 5-point storyboard

## Key Findings
- **Votes matter in a U shape:** films with 1M+ votes average 8.40, but low-vote films also rate high.
- **Serious genres rate highest:** War (8.18), Western (8.12), Biography (8.04), Drama (8.03). Horror, Action and Thriller rate lowest.
- **Old classics lead:** the 1930s to 1960s average about 8.15, the 2000s and 2010s about 7.93.
- **Longer films rate higher:** films over 160 minutes average 8.18.
- **Proven directors repeat success:** directors with 4+ films are over 3x more likely to have a Top 100 film.
- **Famous actors bring votes, not ratings:** 8.00 vs 8.00 average rating.
- **Data quality issue:** the Country column does not reflect where films were made, so regional conclusions are unreliable.
- 55 "hidden gems" found (rating 8.2+ with under 200K votes).

## Recommendations
1. Create a "Hidden Gems" section for high-rated, low-vote films
2. Build director collections (Nolan, Kurosawa, Leone, Wilder, Miyazaki)
3. Promote classics and War, Biography and Drama films as "timeless picks"
4. Label 2020s films as "rising" until their ratings settle
5. Use famous actors to attract viewers, not as a quality signal
6. Fix the Country column before any country-based reporting

## Files
- `NL_IMDbTop700.ipynb`: cleaning, EDA, hypothesis tests and visuals (Google Colab)
- `NL_IMDbTop700.pdf`: full report (15 pages)
- `NL_IMDbTop700.twbx`: packaged Tableau workbook

## Tools
Python (pandas, NumPy, Matplotlib, Seaborn, SciPy), Google Colab, Tableau
