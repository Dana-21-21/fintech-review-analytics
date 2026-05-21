# Fintech Review Analytics

## Project Overview

This project analyzes mobile banking application reviews from the Google Play Store for three Ethiopian banks:

- Commercial Bank of Ethiopia (CBE)
- Bank of Abyssinia (BOA)
- Dashen Bank

The objective is to transform raw user reviews into actionable business insights using data analytics, Natural Language Processing (NLP), and sentiment analysis techniques.

The project focuses on identifying:
- User satisfaction drivers
- Common customer complaints
- Recurring technical issues
- Requested features
- Overall sentiment trends

The analysis is intended to help banks improve customer experience, mobile app performance, and product decision-making.

---

# Project Structure

```text
fintech-review-analytics/
├── .vscode/
├── .github/
│   └── workflows/
├── data/
│   └── raw/
├── notebooks/
├── scripts/
├── src/
├── tests/
├── README.md
├── requirements.txt
└── .gitignore
```

---

# Technologies Used

- Python
- Jupyter Notebook
- pandas
- NumPy
- google-play-scraper
- Matplotlib
- Seaborn
- Git & GitHub

---

# Task 1: Data Collection and Preprocessing

## Data Collection

User reviews were scraped from the Google Play Store using the `google-play-scraper` Python library.

The following information was collected:
- Review text
- Rating (1–5)
- Review date
- Bank/app name
- Source platform

The project targeted at least 400 reviews per bank.

The scraping and preprocessing pipeline was implemented using Python and Jupyter Notebook.

---

# Banks Included

- Commercial Bank of Ethiopia (CBE)
- Bank of Abyssinia (BOA)
- Dashen Bank

---

# Data Preprocessing

The collected data was cleaned and prepared for analysis through the following steps:

- Removed duplicate reviews using review IDs
- Removed rows with missing review text or ratings
- Standardized dates into `YYYY-MM-DD` format
- Selected only required columns for analysis

Final dataset columns:
- review
- rating
- date
- bank
- source

---

# Sentiment Analysis (In Progress)

Early sentiment analysis has started to classify reviews into:
- Positive
- Negative
- Neutral

Initial observations suggest that:
- Users frequently mention transfer speed and login reliability
- Positive reviews often highlight convenience and usability
- Negative reviews commonly reference crashes, OTP issues, and loading delays

Further thematic analysis and sentiment modeling will be completed in later tasks.

---

# CI/CD Workflow

GitHub Actions is configured to automatically install dependencies on every push to the `main` branch.

Workflow file:

```text
.github/workflows/unittests.yml
```

---

# Repository Link

Add your repository link here:

```text
https://github.com/yourusername/fintech-review-analytics
```

---

# Limitations

Some limitations encountered during scraping include:
- Inconsistent review availability across apps
- Possible language limitations due to English-focused scraping
- Rate limits and review count constraints from Google Play

---

# Future Work

Upcoming tasks include:
- Advanced sentiment analysis using NLP models
- Thematic analysis and keyword extraction
- PostgreSQL database integration
- Business insights and recommendation development
- Visualization and reporting

---
# Database Design

The project uses PostgreSQL to store processed banking review data.

Tables:
- banks
- reviews

The schema was designed using relational database principles,
with foreign key relationships between banks and reviews.
# Author

Prepared as part of the Omega Consultancy Fintech Review Analytics Challenge.
