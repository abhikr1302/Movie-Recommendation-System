# 🎬 Movie Recommendation System

A content-based movie recommendation system built using Python, NLP techniques, and machine learning. The system suggests movies similar to a selected movie by analyzing textual features such as genres, keywords, cast, and overview.

The project demonstrates how Natural Language Processing and similarity algorithms can power recommendation engines used in platforms like streaming services and e-commerce websites.

# 📌 Project Overview

Recommendation systems help users discover relevant content by analyzing patterns and similarities in data.

This project implements a content-based filtering approach where movies are recommended based on their similarity to a selected movie.

The system:

Processes movie metadata

Converts textual data into numerical vectors

Calculates similarity between movies

Recommends the Top-N most similar movies

# 🚀 Features

Content-based recommendation engine

NLP-based feature extraction

Cosine similarity for similarity scoring

Interactive interface using Streamlit

Fast recommendations based on vector similarity

Easy to extend with additional datasets

# 🧠 Machine Learning Approach

The recommendation system follows this pipeline:

## ML Pipeline

```
Movie Dataset
      ↓
Data Preprocessing
      ↓
Feature Engineering (NLP)
      ↓
Text Vectorization
      ↓
Cosine Similarity Calculation
      ↓
Recommendation Engine
```

# 📂 Dataset

The dataset contains movie metadata such as:

Feature	Description
title	Movie title
genres	Movie genres
keywords	Important movie keywords
cast	Main actors
crew	Director and crew
overview	Movie description

These features are combined into a single textual representation for similarity comparison.

# ⚙️ Data Preprocessing

The preprocessing steps include:

Handling missing values

Merging multiple text columns

Text normalization

Tokenization

Removing unnecessary characters

Example transformation:

```
Genres + Keywords + Cast + Overview
                ↓
        Combined Text Feature
```
        
# 🔍 Feature Engineering

The project uses CountVectorizer from Scikit-Learn to convert text data into numerical vectors.

This technique represents each movie as a bag-of-words vector based on word frequency.

Example:

Movie A → [0, 1, 3, 0, 2]
Movie B → [1, 0, 2, 1, 0]

# 📊 Similarity Calculation

To determine movie similarity, the system uses Cosine Similarity.

Cosine similarity measures the similarity between two vectors based on the angle between them.

Formula:

Similarity = (A · B) / (||A|| ||B||)

Higher similarity scores indicate more similar movies.

# 🎯 Recommendation Logic

When a user selects a movie:

The system retrieves the movie index.

Cosine similarity scores are calculated with all other movies.

Movies are sorted based on similarity.

The Top 5 most similar movies are recommended.

Example:

Input Movie: Avatar

Recommended Movies:
1. Avatar: The Way of Water
2. Guardians of the Galaxy
3. Star Trek
4. Interstellar
5. Gravity
   
# 📁 Project Structure

```
movie-recommendation-system/
│
├── data/                        # Dataset files
│   └── movies.csv
│
├── notebooks/                   # Jupyter notebooks for experimentation
│   └── movie_recommendation.ipynb
│
├── src/                         # Core source code
│   ├── preprocessing.py         # Data cleaning and preprocessing
│   ├── feature_engineering.py   # NLP feature creation
│   ├── vectorization.py         # Text vectorization using CountVectorizer
│   └── recommender.py           # Recommendation logic
│
├── models/                      # Saved ML models
│   └── similarity.pkl
│
├── app/                         # Streamlit application
│   └── app.py
│
├── requirements.txt             # Project dependencies
├── README.md                    # Project documentation
└── .gitignore                   # Ignored files
```

# 🛠️ Technologies Used

Python

Pandas

NumPy

Scikit-learn

NLP (CountVectorizer)

Streamlit

Cosine Similarity

# 📦 Installation

Clone the repository:

git clone https://github.com/yourusername/movie-recommendation-system.git

Navigate to the project folder:

cd movie-recommendation-system

Install dependencies:

pip install -r requirements.txt

# ▶️ Running the Application

To start the Streamlit app:

streamlit run app.py

The application will open in your browser where you can select a movie and get recommendations.

# 📈 Future Improvements

Possible enhancements for this project:

Implement collaborative filtering

Use word embeddings (Word2Vec / BERT)

Add user-based personalization

Deploy using Docker and cloud platforms

Integrate movie posters and API data

# 🎯 Learning Outcomes

Through this project, I gained experience in:

Natural Language Processing (NLP)

Feature engineering for text data

Similarity-based recommendation systems

Building ML applications with Python

Developing interactive data applications using Streamlit

# 👨‍💻 Author

Abhishek Kumar

Email: kabhikr74@gmail.com

GitHub: https://github.com/abhikr1302

LinkedIn: https://linkedin.com/in/abhishek-kumar1302
