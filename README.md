# 🎬 Movie Recommendation System - File Descriptions

## 🔹 `.env` (Environment File)
The `.env` file is used to securely store sensitive information such as the TMDB API key. Instead of hardcoding the key inside the program, it is kept separately to maintain security and flexibility. This key is used to fetch real-time movie data like posters, ratings, and descriptions.

---

## 🔹 `movies.ipynb` (Core Machine Learning Code)
The `movies.ipynb` file contains the main logic of the project where the recommendation system is actually built. In this notebook, the movie dataset is processed, cleaned, and transformed. A TF-IDF model is applied to convert textual information like movie descriptions into numerical form. Based on this, similarity between movies is calculated using cosine similarity.
This file is responsible for generating the `.pkl` files such as dataset, indices, and TF-IDF matrix, which are later used in the backend. In simple terms, this is where the "brain" of the recommendation system is created.

---

## 🔹 `app.py` (Streamlit Frontend)
The `app.py` file represents the user interface of the application. It allows users to search for movies, view posters, explore detailed information, and receive recommendations. The interface is interactive and user-friendly, making it easy for users to navigate through the system. It communicates with the backend APIs to fetch and display data.

---

## 🔹 `main.py` (FastAPI Backend)
The `main.py` file contains the backend logic of the system. It handles API requests from the frontend, processes the data using pre-trained models, and returns the results. It also integrates with the TMDB API to fetch additional movie details such as posters and genres. This file acts as a bridge between the frontend and the machine learning model.

---

## 🔹 `df.pkl` (Dataset File)
The `df.pkl` file stores the movie dataset in a structured format. It contains important information such as movie titles, genres, and descriptions, which are used as the base for generating recommendations.

---

## 🔹 `indices.pkl` (Index Mapping File)
The `indices.pkl` file is used to map movie titles to their respective index positions in the dataset. This helps in quickly locating a movie and improves the efficiency of the recommendation process.

---

## 🔹 `tfidf.pkl` (TF-IDF Model)
The `tfidf.pkl` file contains the trained TF-IDF vectorizer. It is used to convert textual movie data into numerical vectors so that similarity between movies can be calculated.

---

## 🔹 `tfidf_matrix.pkl` (Similarity Matrix)
The `tfidf_matrix.pkl` file stores the numerical representation of all movies. It is used to compute similarity scores and find movies that are most similar to the user's input.

---

## 🔹 System Flow
The user interacts with the system through the Streamlit frontend (`app.py`) by searching for a movie. The request is sent to the FastAPI backend (`main.py`), which processes it using pre-trained models stored in `.pkl` files. The backend calculates similarity and fetches additional details from the TMDB API. Finally, the recommended movies are displayed to the user.

---

## 🔹 Final Output
The final output of this project is an interactive movie recommendation system. When a user searches for a movie, the system displays:

- Movie details such as title, genre, overview, and poster  
- A list of similar movies based on content similarity (TF-IDF)  
- Additional recommendations based on genre  

The system provides a smooth and user-friendly experience where users can explore movies and discover new content easily.
