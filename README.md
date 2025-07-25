# Movie-Recommendation-System
# 🎬 Movie Recommendation System

This is a **content-based movie recommender system** built using Python and machine learning libraries. It uses metadata (like genres, cast, crew, keywords, and production companies) from movie datasets to recommend similar movies.

---

## 📁 Dataset Used

Two datasets were used from [Kaggle](https://www.kaggle.com/):
- `movies.csv` – Contains metadata about movies such as title, overview, genres, etc.
- `credits.csv` – Contains cast and crew information for each movie.

---

## 🧰 Technologies Used

- **Python 3**
- **Pandas, NumPy** – data manipulation
- **NLTK** – natural language processing (stopword removal)
- **Scikit-learn** – vectorization and similarity calculation
- **Matplotlib / Seaborn** – optional for visualization
- **Pickle** – for saving models

---

## 🧪 How It Works

1. **Data Loading & Cleaning**
   - Merges `movies.csv` and `credits.csv` using movie IDs.
   - Extracts relevant features: `genres`, `keywords`, `overview`, `cast`, `crew`, `production_companies`.
   - Converts JSON-like columns into clean text.

2. **Feature Engineering**
   - Combines all text fields into one field: `tags`.
   - Removes duplicates, nulls, and stopwords for better results.

3. **Vectorization**
   - Uses `CountVectorizer` with a max feature limit of 5000.
   - Converts text into a numerical matrix.

4. **Similarity Measurement**
   - Computes cosine similarity between movie vectors.

5. **Recommendation Logic**
   - For a given movie name, finds top 5 most similar movies.

6. **Export**
   - Saves the final cleaned dataset and similarity matrix as `.pkl` files for reuse.

---

## 💡 Example

```python
Enter the movie name: Avatar
Recommended Movies:
1. John Carter
2. Guardians of the Galaxy
3. Pirates of the Caribbean: At World's End
4. Star Trek
5. The Avengers
