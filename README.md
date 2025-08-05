# Talanta Hela: A Data-Driven Strategy for a New Movie Studio

## Overview

With the rise of original content from streaming giants, our company seeks to launch a new movie studio. However, entering the film industry without prior experience introduces financial risks. This project analyzes box office data to uncover what types of films perform best and provides actionable insights to guide content, budgeting, and release strategies.

## Business Understanding

The objective is to help studio leadership make informed decisions on film selection and production through data. The analysis identifies factors associated with high-grossing movies, such as genre, release timing, ratings, and budget efficiency.

## Data Sources

The analysis combines five public datasets and an IMDb SQLite database to provide a rich foundation for exploration.

- **The Numbers (`tn.movie_budgets.csv`)**: Production budgets and gross earnings.
- **Box Office Mojo (`bom.movie_gross.csv`)**: Studio-level revenue by year.
- **Rotten Tomatoes (`rt.movie_info.tsv` & `rt.reviews.tsv`)**: Film metadata and critic reviews.
- **TMDB (`tmdb.movies.csv`)**: Popularity scores, ratings, genres.
- **IMDb (`im.db`)**: Movie metadata, ratings, and relationships.

## Data Preparation

Each dataset underwent cleaning and preprocessing including:

- Currency symbol removal and numeric conversion.
- Null value imputation or dropping based on column importance.
- Genre normalization and date standardization.
- Creation of engineered fields: `profit`, `ROI`.
- Merging datasets on title, release year, or ID.

## Data Validation

Data profiling, missing value checks, duplicate handling, and outlier detection ensured the reliability of insights. Datasets with missing critical values were cleaned, and outliers filtered using IQR.

##  Key Findings

- **Genres**: Thriller and mixed-genre films show the highest average profits.
- **Ratings**: Higher IMDb ratings correlate with increased worldwide gross.
- **Budgets**: ROI is not guaranteed by large budgets; an optimal mid-range budget is often more effective.
- **Seasonality**: Summer and winter holidays are prime periods for box office performance.
- **Statistical Tests**:
  - ANOVA confirmed genre and rating influence on revenue and vote count.
  - Pearson correlation showed a weak negative relation between runtime and average rating.

## Recommendations

1. **Prioritize High-Yield Genres**: Thriller, Comedy, and genre blends.
2. **Invest in Quality**: Critical acclaim is linked to higher financial success.
3. **Time Releases Strategically**: Target summer and winter holidays for maximum exposure.

## Project Structure

```bash
Talanta-hela
 ┣ data
 ┃ ┣ tn.movie_budgets.csv
 ┃ ┣ bom.movie_gross.csv
 ┃ ┣ rt.movie_info.tsv
 ┃ ┣ rt.reviews.tsv
 ┃ ┣ tmdb.movies.csv
 ┃ ┗ im.db
 ┣ notebooks
 ┃ ┣ StatisticalTesting_on_hypotheses.ipynb
 ┃ ┗ data_validation.ipynb
 ┣ outputs
 ┃ ┗ final_report.docx
 ┗ README.md
```

## Tech Stack

- Python (Pandas, NumPy)
- Matplotlib, Seaborn, Plotly (Visualizations)
- SQLite (IMDb)
- SciPy (ANOVA, correlation tests)
- Jupyter Notebooks

## License

This project is provided for educational and exploratory purposes.

## Link to slides, tabluea
[Canva Designs](https://www.canva.com/design/DAGvKQ2GDdU/Aeiu9X_lKRNWK2BvLeghKg/edit)

[Interactive Tableau dashboard](https://public.tableau.com/app/profile/achieng.otieno/viz/Talanta_Hela/BoxOffice?publish=yes)