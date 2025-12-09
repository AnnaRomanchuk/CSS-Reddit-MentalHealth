# CSS Reddit Mental Health
## Overview
This repository contains experimental analysis and preprocessing of Reddit comments related to mental health during the COVID-19 pandemic between February and September 2020. The goal is to clean up the raw text, explore patterns in the data, and prepare features that could support further tasks such as classification, topic modeling, or trend monitoring. In other words, to explore community activity dynamics, emotional trends, and the relationship between content and user engagement.

## Repository Structure
- `comments_cleanup.ipynb` – text cleaning workflow for Reddit comments, including noise removal and normalization steps.
- `eda.ipynb` – exploratory data analysis notebook that inspects dataset composition, comment length distributions, and other descriptive statistics.

## Getting Started
1. **Clone the repository**
   ```bash
   git clone https://github.com/<your-username>/CSS-Reddit-MentalHealth.git
   cd CSS-Reddit-MentalHealth
   ```
2. **Create a virtual environment** 
   ```bash
   python -m venv .venv
   source .venv/bin/activate
   ```
3. **Install required dependencies**
   ```bash
   pip install -r requirements.txt
   ```
## Data
- Source: Pushshift Reddit Archive (archive of Reddit comments).
- Collection period: February–September 2020.
- Dataset: 1.8m rows
- Thematic subreddits: `r/COVID19`, `r/coronavirus`, `r/depression`, `r/anxiety`, `r/offmychest`, `r/covid19_support`, `r/mentalhealthsupport`.
- Main fields: `id`, `author`, `subreddit`, `topic`, `month`, `event_time`, `text`, `text_len`, `score`.
- Publication time is restored by file name (`RC_YYYY-MM.csv`), which allows you to build monthly snapshots.
  
## Methodology
- **EDA:** descriptive statistics, grouping by month and subreddit, visualization of text length distributions and activity metrics.
- **Sentiment analysis:** VADER (Valence Aware Dictionary and sEntiment Reasoner); threshold values: `compound ≥ 0.05` – positive, `compound ≤ -0.05` – negative, otherwise – neutral.

## Authors
Bakalyna Anastasiia
Romanchuk Anna
