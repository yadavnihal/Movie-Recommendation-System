# 🎬 Movie Recommendation System

A **Streamlit-based Movie Recommendation Web App** that suggests movies using **Content-Based Filtering** with **TF-IDF, Tokenization, Lemmatization (NLTK), and Cosine Similarity**, along with **Genre-Based Recommendations** and **TMDB API integration** for posters and movie details.

---

## 🚀 Features

- 🔍 Movie Search with Autocomplete Suggestions  
- 🧠 **TF-IDF Based Similar Movie Recommendations**
- 🎭 **Genre-Based Recommendations**
- 📄 Detailed Movie Page (Poster, Genres, Overview, Release Date)
- 🎨 Netflix-Style Modern Dark UI
- ⚡ FastAPI Backend Integration
- 🌐 TMDB API for Posters & Metadata
- 📱 Responsive Poster Grid Layout

---

## 🧠 Recommendation Logic

### 1. Text Pre-Processing (NLP)

Movie overviews/descriptions are cleaned and processed using **Natural Language Processing (NLP)**:

- **Tokenization** – Splitting sentences into words  
- **Lowercasing** – Standardizing text  
- **Stopword Removal** – Removing common words (*the, is, and, of…*)  
- **Lemmatization (NLTK)** – Converting words to base form  
  - `running → run`  
  - `movies → movie`

**Libraries Used**
- `nltk`
- `re` (Regular Expressions)
- `string`

---

### 2. TF-IDF Vectorization

**TF-IDF (Term Frequency – Inverse Document Frequency)** converts processed text into numerical vectors.

- Highlights important/unique words
- Reduces weight of frequent/common words
- Enables mathematical comparison of movie content

**Library**
- `sklearn.feature_extraction.text.TfidfVectorizer`

---

### 3. Cosine Similarity

After TF-IDF vectorization, **Cosine Similarity** measures similarity between two movie vectors.

- **Range:** `0 → 1`
- `1` → Highly Similar  
- `0` → Completely Different

**Library**
- `sklearn.metrics.pairwise.cosine_similarity`

---

### 4. Genre-Based Recommendation

If TF-IDF similarity is limited or unavailable, additional recommendations are generated based on **shared genres** using TMDB metadata.

---

## 🛠️ Tech Stack

### Frontend
- **Streamlit**
- Custom HTML + CSS Styling
- Responsive Grid Layout

### Backend
- **FastAPI**
- Python

### Machine Learning / NLP
- **Scikit-Learn**
- **NLTK**
- TF-IDF Vectorization
- Cosine Similarity

### External APIs
- **TMDB API** – Posters, Movie Metadata, Trending/Popular Lists

---

## 📂 Project Structure

# Movie Recommendation System

- **app.py** – Handles the Streamlit user interface (Frontend).
- **main.py** – Runs the FastAPI server (Backend APIs).
- **requirements.txt** – Contains all Python dependencies.
- **README.md** – Project documentation file.
- **assets/** – Stores images, posters, or static files.
- **data/** – Contains datasets used for recommendation.



---

## ▶️ Run Locally

### 1. Clone Repository
```bash
git clone https://github.com/yourusername/Movie-Recommendation-System.git
cd Movie-Recommendation-System
## ▶️ Run Locally

###2. Install Dependencies
pip install -r requirements.txt

###3. Run Backend
uvicorn main:app --reload

###4. Run Frontend
streamlit run app.py

```

## 🌐 Deployment

- **Frontend:** Streamlit Community Cloud  
- **Backend:** Render / Railway / Localhost  
- **Live App:** [Movie Recommendation System](https://movie-recommendation-system-tfidf-cosine.streamlit.app/)

---

## 🎨 UI Highlights

- Dark Netflix-Inspired Theme  
- Poster Hover Animations  
- Dynamic Grid Layout  
- Movie Details Page with Backdrop  
- Search Suggestions + Results View  

---

## 📈 Future Improvements

- Collaborative Filtering  
- User Accounts & Watchlists  
- Personalized AI Recommendations  
- Voice Search  
- Mobile Optimization  

---

## 👨‍💻 Author

**Nihal Yadav**  

---

## 📜 License

This project is for **educational and portfolio purposes**.
