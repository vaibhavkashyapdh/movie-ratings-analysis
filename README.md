# Movie Ratings Analysis (TMDB 5000)

Analyze and visualize 5,000+ movies to understand how **genre, directors, budget, and revenue** relate to IMDb-style ratings using NumPy, Pandas, and Matplotlib.

## 1. Project Goal

- Explore which genres and directors achieve higher average ratings.
- Study rating trends over time (by release year).
- Check relationships between budget/revenue and rating.

## 2. Dataset

- **Source:** TMDB 5000 Movie Dataset (Kaggle)  
- **Link:** https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata  
- **Main columns used:**
  - `vote_average` – movie rating
  - `budget`, `revenue` – production cost and box office
  - `genres` – list of genres in JSON format
  - `release_date` – converted to `release_year`
  - `director` – extracted from `tmdb_5000_credits.csv`

> Note: Raw CSV files are not committed because of size; download them from Kaggle and place them in the project folder.

## 3. Tech Stack & Methods

- **Libraries:** NumPy, Pandas, Matplotlib, Seaborn
- **Key steps:**
  - Clean and merge `tmdb_5000_movies.csv` and `tmdb_5000_credits.csv`
  - Parse JSON fields (`genres`, `crew`) to extract primary genre and director
  - Handle missing values and convert numeric columns
  - Compute NumPy statistics (mean, median, std) for ratings, budget, revenue
  - Group analysis with Pandas by genre, director, and release year

## 4. Results & Insights

- Average movie rating is around 6 out of 10.
- Documentary/War/History tend to have higher average ratings than Action/Comedy.
- A few directors (e.g., well-known auteurs) consistently achieve higher mean ratings.
- Higher budget and revenue show weak correlation with rating; big spend does not guarantee quality.
- Ratings are relatively stable over years with small fluctuations.

## 5. Visualizations

The script generates a 2x3 dashboard:

1. Bar: Average rating by genre (Top 10).
2. Bar: Average rating by director (Top 10 with ≥2 movies).
3. Line: Average rating by year.
4. Scatter: Budget vs rating.
5. Scatter: Revenue vs rating.
6. Horizontal bar: Top 10 highest-rated movies.

<img width="5967" height="4131" alt="movie_dashboard" src="https://github.com/user-attachments/assets/1df12f47-37cd-4bf1-9ce5-ad65a14fdb3b" />

## 6. How to Run

### Google Colab

1. Open the notebook / script in Colab.
2. Upload `tmdb_5000_movies.csv` and `tmdb_5000_credits.csv`.
3. Run all cells to generate stats and plots.
