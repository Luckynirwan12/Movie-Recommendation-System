# 🎬 Movie Recommendation System 
## 📌 Objective:
This project is a **Movie Recommendation System** built using Python, Streamlit, and the TMDB API. It suggests 5 similar movies based on a user's selected favorite — with movie posters fetched live from TMDB. It is a content-based recommender system using cosine similarity on movie features.

---

## 📊 Workflow Diagram

Here’s a visual overview of the system pipeline:
<img width="1727" height="979" alt="image" src="https://github.com/user-attachments/assets/563379ff-5b81-4f04-b101-c7999e03f889" />

---

## 🚀 Tech Stack

| Technology | Purpose |
|------------|---------|
| **Python** | Core programming language |
| **Streamlit** | Web application UI |
| **Pandas** | Data manipulation |
| **Pickle** | Load pre-trained data |
| **TMDB API** | Fetch movie posters |
| **Scikit-learn** | Cosine similarity for recommendation |

---

## 🧱 1. Data Collection & Preprocessing
- Loaded the dataset with movie metadata.

- Extracted and merged features like `genres`, `keywords`, `cast`, and `crew`.

- Created a unified tags field for each movie.

- Cleaned and tokenized the text, and applied stemming using nltk.

---

## ⚙️ 2. Feature Engineering
- Used CountVectorizer to convert text into numerical vectors.

- Applied cosine similarity to compute similarity between all movie pairs.

- Saved:

    - `movies_dict.pkl`: dictionary of movies and metadata.

    - `similarity.pkl`: similarity matrix of all movie pairs.

---

## 🔍 How It Works

1. **Data Loading**:
   - Movie metadata and similarity matrix are loaded using `pickle`.

2. **Recommendation Logic**:
   - Finds the most similar movies using **cosine similarity** between feature vectors.

3. **Poster Fetching**:
   - The Movie Database (TMDB) API is used to fetch poster URLs for each movie.

4. **User Interface**:
   - Streamlit app provides an easy-to-use UI for selecting a movie and displaying recommendations with posters.

---

## 🌐 API Used
TMDB API

  - Used to fetch movie poster images dynamically.

  - API Key must be included in `fetch_poster()` function.

  - Get your API key: `https://www.themoviedb.org/`

---

## 📁 Project Structure
📦 Movie_Recommendation_System/

├── Movie_Recommendation_System.ipynb   # Development notebook

├── movie.csv                           # Training DataSet

├── app.py                              # Streamlit app script

├── movies_dict.pkl                     # Preprocessed movie metadata

└── similarity.pkl                      # Precomputed similarity matrix

---

## ⚙️ How to Run the Project Locally
- Run the Streamlit App

      pip install streamlit
      streamlit run app.py
