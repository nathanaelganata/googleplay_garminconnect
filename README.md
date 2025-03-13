# 📊 Sentiment Analysis of Garmin Connect App Reviews

This project presents a comprehensive sentiment analysis pipeline on **Google Play Store reviews of the Garmin Connect app**. The aim is to extract meaningful user insights, analyze sentiment trends, and provide data-driven recommendations to support product and service improvements.

---

## 📁 Project Structure

```bash
.
├── 01_scraping.ipynb             # Scrapes reviews from Google Play Store
├── 02_raw_eda.ipynb              # Exploratory data analysis on raw reviews
├── 03_preprocessing.ipynb        # Sentiment-aware text preprocessing
├── 04_sentiment_analysis.ipynb   # Sentiment classification using VADER (baseline)
```

---
## 🛠️ Tools and Libraries Used

- Python (Jupyter Notebooks)  
- `google-play-scraper` / `play-scraper`  
- `pandas`, `numpy`  
- `matplotlib`, `seaborn`  
- `nltk`, `spaCy`, `contractions`  
- `wordcloud`  
- `vaderSentiment` (baseline sentiment model)  
- *(Optional)* `scikit-learn`, `transformers` for ML/BERT models

---

## 📌 Workflow Overview

### 1️⃣ `01_scraping.ipynb` - Google Play Scraping
- Scrapes user reviews of **Garmin Connect** from the Google Play Store.  
- Extracts fields like `reviewId`, `userName`, `content`, `score`, `at`, `appVersion`, etc.  
- Saves the dataset for downstream analysis.

### 2️⃣ `02_raw_eda.ipynb` - Exploratory Data Analysis (EDA)
- Explores review distribution by score, time, and hour of posting.  
- Visualizes review volume trends and score trends over time.  
- Investigates patterns in review submission behavior.

### 3️⃣ `03_preprocessing.ipynb` - Sentiment-Aware Text Preprocessing
- Cleans and normalizes review text:
  - Lowercasing, punctuation removal, contraction expansion  
  - Lemmatization using **spaCy**  
  - **Negation tagging** (e.g., `not_good`) for better sentiment preservation  
  - Custom stopword filtering to remove neutral/non-emotive words  
- Generates a `clean_content` column for downstream sentiment modeling.

### 4️⃣ `04_sentiment_analysis.ipynb` - VADER-Based Sentiment Classification
- Performs **lexicon-based sentiment analysis** using **VADER**.  
- Computes **compound sentiment scores** and classifies reviews into:
  - Positive, Neutral, or Negative  
- Visualizes:
  - Sentiment distribution  
  - Sentiment trends over time  
  - Sentiment correlation with review scores
---


## 📌 Notes

- **App analyzed**: Garmin Connect  
- **Platform**: Google Play Store  
- **Language**: English reviews only  
- **Goal**: Extract and visualize actionable sentiment trends

---