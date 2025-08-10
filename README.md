# amazonPrimeMovieAndTVShowsDataAnalysis

---

# 📺 Amazon Prime Titles Analysis

## 📝 Project Overview
This project performs a comprehensive analysis of Amazon Prime's content catalog, focusing on trends in movies and TV shows across countries, genres, durations, ratings, and more. It uses Python for data cleaning, transformation, and visualization to uncover insights from the dataset.

---

## 📂 Dataset
- **Source**: `amazon_prime_titles.csv`
- **Size**: ~9,668 entries
- **Fields**:
  - `show_id`, `type`, `title`, `director`, `cast`, `country`, `date_added`, `release_year`, `rating`, `duration`, `listed_in`, `description`

---

## 🧼 Data Cleaning Steps
Performed in `In [151]`:
- Removed duplicates
- Stripped extra spaces from column names
- Handled missing values:
  - Dropped rows missing `title`
  - Filled missing `director`, `cast`, `country`, `rating` with `"Unknown"`
  - Converted `date_added` to datetime and filled nulls with `"2000-01-01"`
- Standardized `type` column values
- Cleaned `duration` and text columns using regex
- Converted `release_year` to integer and filtered valid years (1900–2025)
- Reset index after cleaning

---

## 📊 Analysis Questions & Highlights

### Q1: Which country has produced the most Amazon Prime titles?
- 🇺🇸 United States: 4,129 titles
- 🇮🇳 India: 3,961 titles

### Q2: How has the number of movies and TV shows changed over the years?
- Line plot shows a sharp rise post-2015, peaking around 2021.

### Q3: What are the most common genres?
- Top genres: Drama, Comedy, Action, Suspense, Horror

### Q4: Who are the top 10 most frequently appearing directors?
- Most frequent: Jay Chapman, Mark Knight, Manny Rodriguez

### Q5: Which actors appear most often?
- Top appearances: Cassandra Peterson, Maggie Binkley, Eddie Izzard

### Q6: What is the distribution of ratings?
- Most common: 13+, 16+, 18+, R

### Q7: Which year had the highest number of new titles added?
- 📈 2021 tops the chart with 13,637 titles

### Q8: How do average durations compare?
- Movies: ~90–100 minutes
- TV Shows: ~1–2 seasons

### Q9: Most popular genres in the last 5 years?
- Drama, Comedy, Action, Suspense, Horror

### Q10: Which countries dominate the production of TV shows vs. movies?
- **Movies**:
  - 🇮🇳 India: 3,388
  - 🇺🇸 United States: 3,354
  - 🇬🇧 United Kingdom: 637
- **TV Shows**:
  - 🇺🇸 United States: 775
  - 🇮🇳 India: 573
  - 🇬🇧 United Kingdom: 80

---

## 📈 Visualizations
- Bar plots for top countries, genres, ratings, durations
- Line plots for yearly trends
- Exploded columns for multi-value fields like `listed_in` and `country`

---

## 🛠️ Technologies Used
- **Python**: Core language
- **Pandas**: Data manipulation
- **NumPy**: Numerical operations
- **Matplotlib & Seaborn**: Visualization

---

## 📌 How to Run
1. Clone the repo or download the notebook
2. Place `amazon_prime_titles.csv` in the working directory
3. Run the notebook step-by-step
4. Ensure required libraries are installed:
   ```bash
   pip install pandas numpy matplotlib seaborn
   ```

---

## 📚 Future Enhancements
- Add interactive dashboards using Plotly or Streamlit
- Perform sentiment analysis on descriptions
- Cluster genres using NLP techniques
- Compare with Netflix or Disney+ datasets

---

## 🙌 Acknowledgments
Dataset obtained from Kaggle

---
