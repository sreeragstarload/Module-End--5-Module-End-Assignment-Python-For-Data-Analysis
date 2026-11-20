5-Module-End-Assignment-Python-For-Data-Analysis
(Social Media Engagement Analytics)

📌 Project Overview
This repository contains the end-to-end Exploratory Data Analysis (EDA) and statistical evaluation of **5,000 social media posts** (`social_media_engagement_5000.csv`). The project demonstrates data cleaning, feature engineering, statistical profiling, and multi-library data visualization to uncover actionable insights across content formats, user demographics, device usage, and audience sentiment.

---

🎯 Objectives
1. **Data Import & Setup:** Load raw CSV records, parse `DD-MM-YYYY` date fields, and execute vectorized NumPy array computations.
2. **Data Cleaning & Validation:** Handle missing values, standardize categorical labels, extract hashtag counts, and correct unrealistic engagement records where interactions exceed total impressions.
3. **Exploratory Data Analysis (EDA):** Inspect distributions, correlations, and multi-dimensional aggregations across post types, countries, and categories.
4. **Feature Engineering & Wrangling:** Construct weighted `engagement_score`, recalculated `engagement_rate`, and log-transformed reach metrics.
5. **Statistical Profiling:** Calculate central tendency, dispersion, percentiles, skewness, and kurtosis across core engagement metrics.
6. **Data Visualization:** Build 13 static and interactive charts using **Matplotlib**, **Seaborn**, and **Plotly**.

---

## 📂 Repository Structure
```text
├── data/
│   └── social_media_engagement_5000.csv        # Raw dataset (5,000 rows, 19 columns)
├── notebooks/
│   └── module_5_assignment_social_media_engagement.ipynb  # Complete Jupyter Notebook with code & outputs
├── reports/
│   └── Social_Media_Engagement_Summary.pdf     # One-page executive summary report
└── README.md                                   # Project documentation

🛠️ Tech Stack & LibrariesLanguage: Python 3.xData Manipulation: pandas, numpyStatistical Analysis: scipy, numpyVisualization: matplotlib, seaborn, plotlyEnvironment: Jupyter Notebook / Anaconda


 🧹 Data Cleaning & Preprocessing HighlightsMissing Value Imputation:

Imputed 150 missing records each in age, likes, comments, and shares using column medians, and 150 missing records each in gender and sentiment using mode imputation.Anomaly Correction: Identified and proportionally scaled 600 records where likes + comments + shares exceeded impression_count, restoring realistic engagement_rate bounds (0 to 1).Feature Engineering:engagement_rate = (likes + comments + shares) / impression_countengagement_score = likes + (2 * comments) + (3 * shares)hashtag_count extracted via string parsing of # tokens.



📊 Key Analytical InsightsTop Content Format & Category:

 Image posts lead in weighted engagement_score (15,086), while Music (15,262 score) and Food (15,168 score) are the top-performing content categories.Geographic Performance: Australia achieves the highest average engagement rate (39.54%), while India drives the highest average reach (52,462 impressions/post).Audience Demographics: Users aged 13–24 show the highest engagement rate (38.05%), whereas users aged 25–34 generate the highest overall engagement score (15,180).Device Behavior: Mobile users record the longest average watch time (4,088 seconds) compared to tablet and desktop users.Sentiment Dynamics: Positive posts achieve the highest overall engagement score (15,099) and likes, while Neutral and Negative posts drive higher average comment counts (1,438 and 1,410 vs. 1,394), indicating higher debate/discussion activity
.🚀 How to Run LocallyClone the repository:

Bashgit clone [https://github.com/](https://github.com/)<sreeragstarload>/social-media-engagement-analytics.git
cd social-media-engagement-analytics

Install required packages:Bashpip install pandas numpy matplotlib seaborn plotly scipy jupyter
Launch Jupyter Notebook:Bashjupyter notebook notebooks/module_5_assignment_social_media_engagement.ipynb
