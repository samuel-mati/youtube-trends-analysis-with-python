# What Drives Video Performance on YouTube Kenya
### A Content, Engagement, and Timing Analysis Using the YouTube Data API

**Prepared by:** Samuel Mati

**Role:** Data Analyst

**Date:** 6th July 2025

---

## Executive Summary

A content creator or media team operating in Kenya needs to know what drives video performance so they can prioritize the right categories, posting times, formats, and engagement strategies. Without this analysis, decisions about content strategy default to intuition rather than evidence.

I collected trending video data for Kenya directly from the YouTube Data API v3, cleaned and structured it in Python, and conducted an end-to-end exploratory analysis covering categories, engagement metrics, posting patterns, creator activity, and video characteristics.

The analysis produced seven findings that directly inform content strategy. The most consequential are:

- Entertainment, Music, and People & Blogs dominate the trending list, which means reach-oriented creators should prioritize these categories.
- Music drives the most views, while Entertainment and Comedy drive the most comments, which means the category choice depends on whether the goal is reach or community engagement.
- Videos posted on Thursdays and Fridays receive the most views, which means publishing schedules should shift toward the end of the week.
- Videos under five minutes are more likely to trend, while videos over thirty minutes consistently underperform in trending metrics.
- Views and likes correlate at 0.83, and likes and comments correlate at 0.88, which confirms that engagement metrics move together and can be used as a single health signal.

These findings give a content team a clear set of priorities for category selection, posting timing, video length, and description optimization.

---

## Business Problem

YouTube is a crowded platform. Every day thousands of videos are uploaded in Kenya alone, and only a small fraction reach the trending list. For creators and media teams, the difference between a video that trends and one that does not can determine whether a channel grows or stalls.

The business question is straightforward:

**What content characteristics and publishing decisions are associated with trending performance in Kenya, and how can those be used to guide content strategy?**

Without structured analysis, creators make decisions about category, length, posting day, and description based on guesswork. This analysis replaces that guesswork with evidence from the platform's own trending data.

---

## Data Source and Method

**Data Source**
YouTube Data API v3, accessed with the following parameters:

- regionCode: KE (Kenya)
- chart: mostPopular
- maxResults: 50

Documentation: https://developers.google.com/youtube/v3

**Method**

1. Data Collection
   - Connected to the YouTube Data API using the Google API Client.
   - Pulled the daily top 50 trending videos for Kenya.
   - Stored raw responses as CSV and JSON for reproducibility.

2. Data Cleaning
   - Removed duplicates and incomplete records.
   - Parsed timestamps into publish date, day of week, and hour of upload.
   - Standardized category names and converted engagement metrics to numeric types.

3. Exploratory Analysis
   - Aggregated views, likes, and comments by category, upload day, and video length.
   - Calculated correlation coefficients between engagement metrics.
   - Analyzed description length against performance.
   - Identified recurring creators in the trending list.

4. Visualization and Insight Generation
   - Built charts for category performance, engagement distributions, and posting patterns.
   - Generated a word cloud from video titles to surface recurring themes.
   - Interpreted results into decisions a content team can act on.

**Tools and Libraries**

- Python
- Pandas for data manipulation
- Matplotlib, Seaborn, and Plotly for visualization
- Google API Client for YouTube API integration
- Wordcloud for title keyword analysis
- Python-dotenv for environment variable handling

---

## Key Findings

### 1. Entertainment, Music, and People & Blogs dominate Kenya's trending list

These three categories consistently appear in the daily top 50. This tells a content team that if the goal is trending reach, these categories offer the highest probability of appearing on the list. Categories outside these three need a differentiated strategy to break through.

### 2. Music drives the most views, while Entertainment and Comedy drive the most comments

Views and comments are driven by different categories. Music videos attract the largest audiences, which makes them the strongest choice for reach and brand exposure. Entertainment and Comedy attract the most comments, which makes them the strongest choice for community building and audience interaction. A creator whose goal is engagement should not default to Music just because it leads on views.

### 3. News and Education content show noticeably lower engagement

News and Education videos trend but do not generate the same level of likes and comments as Entertainment, Music, or Comedy. This means a creator in these categories should not measure success against the same benchmarks. Different content types require different performance expectations.

### 4. Videos posted on Thursdays and Fridays receive the most views

Upload day is associated with performance. Thursday and Friday uploads consistently outperform the rest of the week on views. This suggests audiences are more active heading into the weekend. Wednesday has the highest volume of uploads but does not convert that volume into the highest views, which means upload volume alone does not drive performance.

### 5. Shorter videos are more likely to trend

Videos under five minutes are more likely to appear on the trending list, while videos over thirty minutes underperform in trending metrics. This does not mean long-form content cannot succeed, but it does mean that if trending is the objective, shorter formats have a structural advantage.

### 6. Longer descriptions correlate with slightly better performance

Videos with longer descriptions tend to perform slightly better on views and likes, and having any description at all outperforms having none. Description length is a low-effort lever that a content team can optimize immediately without changing the content itself.

### 7. Engagement metrics move together

Views and likes correlate at 0.83. Likes and comments correlate at 0.88. Views and comments correlate at 0.76. This means engagement metrics are not independent. A video that performs well on one metric tends to perform well on the others, which means a content team can use a single engagement signal to track health rather than monitoring three separate metrics.

### 8. View and engagement distributions are heavily right-skewed

Most trending videos have under one million views, with a small number going viral at five million or more. Likes are concentrated under 100K and comments under 50K for the majority of videos. This means the median trending video is far more modest than the headline viral examples suggest. A creator should benchmark against the median, not the outliers.

### 9. A small group of creators appear repeatedly in the trending list

The same creators show up in trending results far more often than chance would predict, and they are concentrated in Music and Entertainment. This suggests that once a creator reaches trending, they are more likely to return. Building a repeatable content engine matters more than chasing a single viral hit.

---

## Recommendations

1. Category Selection Based on Goal
   - For reach and brand exposure, prioritize Music.
   - For community engagement and interaction, prioritize Entertainment and Comedy.
   - For News and Education, set different performance benchmarks and do not compare against entertainment categories.

2. Publishing Schedule
   - Shift priority uploads to Thursday and Friday when view performance peaks.
   - Do not assume that uploading more frequently on high-volume days like Wednesday will translate into higher views.

3. Video Length
   - For trending-oriented content, prioritize formats under five minutes.
   - Reserve longer formats for content where depth is the value proposition, and expect lower trending performance.

4. Description Optimization
   - Ensure every video has a description.
   - Extend descriptions where possible, since longer descriptions correlate with slightly better performance at no additional production cost.

5. Engagement Tracking
   - Track a single engagement metric rather than three, since views, likes, and comments move together.
   - Use the median trending video as a benchmark, not the viral outliers.

6. Creator Partnerships
   - Consider collaborations with creators who already appear repeatedly in the trending list, since these creators have demonstrated a repeatable ability to reach the list.

---

## Next Steps

- Extend the analysis to multiple regions for comparison across African markets.
- Add a time-series component to track how trending categories shift week over week.
- Incorporate subscriber growth data to measure whether trending appearances convert into channel growth.
- Build an automated dashboard that refreshes daily from the API for ongoing monitoring.
- Add sentiment analysis on comments to measure audience reaction, not just volume.

---

## Project Structure
