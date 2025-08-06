# 📺 YouTube Trends Analysis with Python

## 📌 Overview
This project analyzes **YouTube Trending Videos in Kenya** using the YouTube Data API v3.  
The aim is to explore trends in content categories, engagement metrics (views, likes, comments), upload times, and creator activity.  
The analysis is done **end-to-end** in Python — from data collection via API, to cleaning, exploratory data analysis (EDA), visualization, and insight generation.

---

## 🎯 Objectives
- Collect trending video data for Kenya using the YouTube Data API.
- Identify the most popular content categories.
- Compare engagement metrics (views, likes, comments) across categories.
- Explore posting patterns by time of day and day of week.
- Highlight recurring creators in the trending list.

---

## 📊 Data Source
- **YouTube Data API v3**:  
  Documentation → [https://developers.google.com/youtube/v3](https://developers.google.com/youtube/v3)  
- Parameters used:
  - `regionCode='KE'` (Kenya)
  - `chart='mostPopular'`
  - `maxResults=50`

---

## 🛠️ Tools & Libraries
- **Python**
- **Pandas** – data manipulation
- **Matplotlib / Seaborn / Plotly** – visualization
- **Google API Client** – YouTube API integration
- **Wordcloud** – title keyword visualization
- **Python-dotenv** – environment variable handling

---

## 📂 Project Structure
```plaintext
youtube-trends-analysis-with-python/
│
├── data/
│   ├── raw/           # Raw API data (CSV/JSON)
│   ├── processed/     # Cleaned data
│
├── notebooks/
│   ├── 01_data_collection.ipynb
│   ├── 02_data_cleaning.ipynb
│   ├── 03_eda_visualization.ipynb
│
├── visuals/           # Charts and graphics
│
├── README.md
├── requirements.txt
└── .gitignore
```

## 🚀 How to Run

### 1. Clone the repository
```bash
git clone https://github.com/yourusername/youtube-trends-analysis-with-python.git
cd youtube-trends-analysis-with-python
```
### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Set up your API key
 Create a .env file in the project root:
 ```bash
YOUTUBE_API_KEY=your_api_key_here
```
Get an API key from [Google Cloud Console.](https://console.cloud.google.com/)

