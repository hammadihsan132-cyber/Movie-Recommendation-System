# 🎬 Movie Recommendation System (Content-Based)

## 📌 Project Overview

This project is a **Content-Based Movie Recommendation System** built using **Python, Natural Language Processing (NLP), and Machine Learning**.
The system recommends movies similar to a selected movie based on **genres, titles, and user-generated tags**.

The application also includes a **web interface** developed using **Streamlit**, allowing users to interact with the recommender through a browser.

---

## 🎯 Objective

The goal of this project is to design an intelligent system that can:

* Understand movie characteristics
* Measure similarity between movies
* Recommend relevant movies to users

Instead of using user ratings, the system analyzes the **content of the movies**.

---

## 🧠 Methodology

The recommender system follows a **Content-Based Filtering approach**.

### Steps:

1. Data collection from MovieLens dataset
2. Data preprocessing and cleaning
3. Feature extraction using TF-IDF
4. Similarity computation using Cosine Similarity
5. Recommendation generation
6. Web application deployment with Streamlit

---

## 🗂 Dataset

We used the **MovieLens (ml-latest-small)** dataset which contains:

| File       | Description                     |
| ---------- | ------------------------------- |
| movies.csv | Movie titles and genres         |
| tags.csv   | User-generated descriptive tags |
| links.csv  | Mapping to IMDb and TMDB IDs    |

Note: The dataset does not contain poster images. Posters are fetched using the **TMDB API**.

---

## ⚙️ Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Natural Language Processing (TF-IDF)
* Cosine Similarity
* Streamlit (Web App)
* TMDB API (Movie Posters)

---

## 🧮 Machine Learning Model

### Feature Extraction

We combine:

* Movie title
* Genres
* Tags

Then we convert the text into numerical vectors using:

**TF-IDF (Term Frequency – Inverse Document Frequency)**

This helps the system understand important descriptive words such as:
`sci-fi`, `space`, `alien`, `future`, `war`, `romance`, etc.

---

### Similarity Measurement

We use **Cosine Similarity** to measure how close two movies are in meaning.

If two movies have similar keywords and genres, their similarity score becomes high.

---

## 🌐 Web Application

The project includes a Streamlit interface where users can:

1. Select a movie from a dropdown
2. Click the "Recommend" button
3. View top similar movies with posters

Run the application:

```bash
streamlit run app.py
```

Then open:

```
http://localhost:8501
```

---

## 📊 Example

Input:

```
The Matrix (1999)
```

Output:

* Inception
* Blade Runner
* Minority Report
* Interstellar

---

## 📁 Project Structure

```
Movie-Recommender/
│
├── app.py
├── mrs.py
├── movies.pkl
├── similarity.pkl
├── tfidf_matrix.pkl
├── indices_dict.pkl
├── movies.csv
├── tags.csv
├── links.csv
└── README.md
```

---

## 🚀 How to Install & Run

### 1. Install dependencies

```bash
pip install streamlit pandas numpy scikit-learn requests
```

### 2. Run model (only first time)

```bash
python mrs.py
```

### 3. Start web app

```bash
streamlit run app.py
```

---

## 🔑 TMDB API Setup (For Posters)

1. Create account on [https://www.themoviedb.org](https://www.themoviedb.org)
2. Generate a free API key
3. Add the key inside `app.py`:

```python
TMDB_API_KEY = "YOUR_API_KEY_HERE"
```

---

## 📈 Evaluation

The system is evaluated using recommendation quality analysis such as:

* Precision@K
* Relevance checking
* Manual comparison of recommended movies

---

## ⚠️ Limitations

* Cannot recommend movies from completely new genres
* No user personalization (same recommendation for all users)
* Depends on available tags and genres
* Cold-start problem for new movies

---

## 🔮 Future Improvements

* Hybrid recommender (content + collaborative filtering)
* User rating system
* Deep learning embeddings
* Personalized user profiles
* Mobile application deployment

---

## 👨‍💻 Author

**Hammad Ihsan**
Bachelor of Artificial Intelligence (Student)

---

## 📚 References

* MovieLens Dataset – [https://grouplens.org/datasets/movielens/](https://grouplens.org/datasets/movielens/)
* Scikit-learn Documentation
* Streamlit Documentation
* TMDB API
