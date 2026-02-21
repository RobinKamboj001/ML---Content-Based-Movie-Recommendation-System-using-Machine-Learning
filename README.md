# 🎬 Movie Recommendation System

A **Content-Based Movie Recommendation System** built with **Machine Learning & Natural Language Processing (NLP)** that recommends movies similar to a selected movie based on its:

* Overview
* Genre
* Keywords
* Cast
* Crew (Director)

This system uses the **TMDB 5000 Movie Dataset** and applies **Cosine Similarity** to find the most relevant movie recommendations.

---

## 🚀 Project Overview

Recommendation systems are used by platforms like Netflix and Amazon to personalize user experience.

This project builds a **content-based filtering recommendation system** that suggests movies based on movie metadata rather than user ratings.

If a user likes a movie such as:

```
Avatar
```

The system will recommend 5 similar movies based on content similarity.

---

## 🧠 Machine Learning Workflow

### 1️⃣ Data Collection

Dataset used:

* tmdb_5000_movies.csv
* tmdb_5000_credits.csv

---

### 2️⃣ Data Preprocessing

* Merged Movies & Credits dataset
* Selected important features:

  * movie_id
  * title
  * overview
  * genres
  * keywords
  * cast
  * crew
* Removed null values
* Extracted:

  * Top 3 cast members
  * Director from crew

---

### 3️⃣ Feature Engineering

Combined the following features into a single column called **tags**:

```
overview + genres + keywords + cast + crew
```

---

### 4️⃣ Text Processing

Applied:

* Lowercasing
* Tokenization
* Stemming using Porter Stemmer
* Stopword removal

---

### 5️⃣ Vectorization

Used:

```
CountVectorizer (max_features = 5000)
```

To convert text data into numerical vectors.

---

### 6️⃣ Similarity Calculation

Used:

```
Cosine Similarity
```

To calculate similarity between movie vectors.

---

### 7️⃣ Recommendation Function

Recommends top 5 movies similar to the selected movie.

Example:

```python
recommend("Avatar")
```

---

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Scikit-Learn
* NLTK
* Matplotlib
* Seaborn
* Pickle

---

## 📦 Model Files Generated

After running the notebook, two files are created:

| File Name      | Description              |
| -------------- | ------------------------ |
| movies_df.pkl  | Processed movie data     |
| similarity.pkl | Cosine similarity matrix |

These files can be used to deploy the recommendation system in a web app (Streamlit / Flask).

---

## ▶️ How to Run the Project

### Step 1: Clone the Repository

```bash
git clone https://github.com/your-username/movie-recommendation-system.git
```

### Step 2: Install Dependencies

```bash
pip install -r requirements.txt
```

### Step 3: Run Jupyter Notebook

```bash
jupyter notebook
```

### Step 4: Execute all cells

---

## 📈 Future Improvements

* Add Collaborative Filtering
* Hybrid Recommendation System
* Deploy using Streamlit
* Add Movie Posters using TMDB API
* Improve NLP using TF-IDF or Word2Vec

---

## ⭐ If you like this project, don't forget to star the repository!
