# 📺 YouTube Trends Analysis with Python

## Overview
This project analyzes **YouTube Trending Videos in Kenya** using the YouTube Data API v3.  
The aim is to explore trends in content categories, engagement metrics (views, likes, comments), upload times, and creator activity.  
The analysis is done **end-to-end** in Python — from data collection via API, to cleaning, exploratory data analysis (EDA), visualization, and insight generation.

---

## Objectives
- Collect trending video data for Kenya using the YouTube Data API.
- Identify the most popular content categories.
- Compare engagement metrics (views, likes, comments) across categories.
- Explore posting patterns by time of day and day of week.
- Highlight recurring creators in the trending list.

---

## Data Source
- **YouTube Data API v3**:  
  Documentation → [https://developers.google.com/youtube/v3](https://developers.google.com/youtube/v3)  
- Parameters used:
  - `regionCode='KE'` (Kenya)
  - `chart='mostPopular'`
  - `maxResults=50`

---

## Tools & Libraries
- **Python**
- **Pandas** – data manipulation
- **Matplotlib / Seaborn / Plotly** – visualization
- **Google API Client** – YouTube API integration
- **Wordcloud** – title keyword visualization
- **Python-dotenv** – environment variable handling

---
## Insights

### 1. **Category Popularity**
- **Entertainment**, **Music**, and **People & Blogs** dominate Kenya's trending list.
- These categories consistently appear in the daily top 50, showing audience preference for engaging and relatable content.

### 2. **Engagement Metrics**
- **Music** videos attract the most views, while **Entertainment** and **Comedy** lead in comments.
- **News** and **Education** content have noticeably lower engagement.

### 3. **Posting Patterns**
- Videos uploaded on **Thursdays and Fridays** receive the most views, suggesting higher activity heading into the weekend.
- Although **Wednesdays** have the most uploads, they don't always yield high views.

### 4. **Creator Activity**
- A small group of creators appear frequently in trending results.
- These top creators mainly produce **music** and **entertainment** content.

### 5. **Description Length**
- Videos with **longer descriptions** tend to perform slightly better in terms of views and likes.
- Having a description (even a short one) is better than none.

### 6. **Engagement Correlation**
- **Views ↔ Likes**: 0.83 – highly viewed videos are also highly liked.
- **Likes ↔ Comments**: 0.88 – strong audience interaction.
- **Views ↔ Comments**: 0.76 – positive correlation.

### 7. **Distributions**
- Most videos have **< 1 million views**, but a few go viral with **5M+ views**.
- **Like and comment counts** are heavily right-skewed, with most videos under **100K likes** and **50K comments**.

### 8. **Video Length vs Views**
- **Shorter videos (<10 mins)** are more likely to trend.
- **Very long videos (>30 mins)** underperform in trending metrics.
---

## Project Structure
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

## How to Run

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

# License
This project is licensed under the MIT License.

# Author
[Samuel Mati](https://github.com/samuel-mati)

[LinkedIn](https://www.linkedin.com/in/samuel-mati/) | [Portfolio](https://sam-analyst.vercel.app/)

