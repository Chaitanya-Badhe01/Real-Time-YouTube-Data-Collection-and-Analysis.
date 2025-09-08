# Real-Time YouTube Data Collection and Analysis
**📌 Introduction / Overview**

This project focuses on collecting and analyzing real-time trending YouTube video data using the YouTube Data API v3. The goal is to understand what makes a video trend on YouTube by examining engagement metrics (views, likes, comments), video categories, video lengths, publishing times, and other factors.

**🎯 Problem Statement / Motivation**

YouTube is one of the world’s largest content platforms, but only a few videos make it to the “trending” list.
The motivation behind this project was to answer:

**What factors contribute to a video trending?**

Do shorter videos perform better?

Which categories dominate the trending section?

Does the time of publishing impact engagement?

**📂 Data Sources**

YouTube Data API v3: Trending videos collected in real-time (Region: India).

Data exported as india_trending_videos.csv.

Categories retrieved using the YouTube API’s category mapping endpoint.

**🛠 Tools and Technology**

**Languages:** Python

**Libraries:**

**Data Handling:** Pandas, NumPy

**Visualization:** Matplotlib, Seaborn

**API Access:** googleapiclient

**Data Formatting:** isodate

**Platform:** Jupyter Notebook

**🔎 Analysis and Methodology**
**1. Data Cleaning and Preparation**

Missing descriptions filled with "No description".

Converted published_at column to datetime format.

Converted video duration (ISO 8601) into seconds using isodate.

Added new features: duration_range, publish_hour, and tag_count.

**2. Exploratory Data Analysis (EDA)**

Descriptive statistics of views, likes, and comments.

Histograms showing skewed distributions (few viral videos vs. many low-engagement ones).

Correlation heatmap confirming strong positive correlation between views, likes, and comments.

**3. Category-Level Analysis**

Mapped category IDs to names.

Music, Gaming, and Entertainment dominate the trending list.

Entertainment, Sports, and Music categories had the highest average engagement.

**4. Video Length Analysis**

Categorized into: 0–5 min, 5–10 min, 10–20 min, 20–60 min, 60–120 min.

Shorter videos (0–5 min) had the highest average views and engagement.

**5. Tags & Engagement**

Weak correlation between number of tags and views → tags alone don’t drive popularity.

**6. Publishing Time**

Most videos published between 11 AM – 1 PM.

Weak negative correlation between publish hour and view count.

**📊 Visualizations**

Some of the visual insights include:

Histograms for views, likes, comments.

Correlation heatmap of engagement metrics.

Bar charts: Trending categories, engagement by category.

Scatterplots: Video length vs. views, tags vs. views, publish hour vs. views.

**🔑 Key Findings & Insights**

✅ Strong positive correlation between views, likes, and comments.

✅ Music, Gaming, and Entertainment dominate trending content.

✅ Shorter videos (<5 minutes) perform significantly better.

✅ Optimal posting time is around 11 AM – 1 PM.

❌ Number of tags has minimal impact on view counts.

**💡 Recommendations**

Encourage likes and comments to boost engagement.

Focus on shorter videos (<5 min) for better performance.

Target Music, Entertainment, and Gaming categories for higher visibility.

Schedule uploads between 11 AM – 1 PM for maximum traction.

**📌 Conclusion**

This project demonstrates that video category, engagement metrics, and length play a crucial role in determining whether a video trends. Creators should focus on short, engaging, and interactive videos in popular categories to increase chances of trending.

**🚀 Future Work**

Extend analysis to multiple regions (global comparison).

Use machine learning models to predict probability of a video trending.

Build a dashboard (Tableau / Power BI / Streamlit) for real-time monitoring.

**⚙️ How to Run the Project**

Clone this repository.

Install dependencies:

pip install pandas numpy matplotlib seaborn google-api-python-client isodate


Generate your YouTube Data API v3 Key.

Run the Jupyter notebook to fetch and analyze trending data.

Output CSV (india_trending_videos.csv) will be generated automatically.

**📜 License**

This project is licensed under the MIT License.

**🙏 Acknowledgements:**

YouTube Data API v3 for data access.

Open-source Python libraries: Pandas, Seaborn, Matplotlib.

Tutorials and references from Kaggle & documentation pages.


