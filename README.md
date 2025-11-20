# Podcast Ratings Analysis (2005–2023)

Exploratory Data Analysis • Statistical Testing • ANOVA • Correlation • Time Series

## Introduction

Over the last decade, the podcast industry has grown rapidly, surpassing 4.5 million active podcasts and 70 million episodes worldwide by 2024. Ratings now play a crucial role in:

Understanding listener satisfaction

Driving platform recommendation algorithms

Influencing podcast discoverability, engagement, and profitability

Even small rating shifts can significantly affect visibility and audience growth.

## Purpose of the Project

This project provides a comprehensive statistical and exploratory analysis of podcast ratings from a large-scale dataset.
The goal is to uncover trends, category performance, user behavior patterns, and rating dynamics across the ecosystem.

### The project answers questions such as:

Category Performance:
Which podcast categories perform the best/worst?

Design Trends (2010–2022):
Are there long-term shifts in content quality?

Rating Distribution:
Which categories receive the most 5-star ratings?

Statistical Testing:
Can t-tests, ANOVA, or confidence intervals reveal meaningful differences between categories?

Correlation:
Do more reviews correlate with higher or lower ratings?

User Behavior:
Do users in some categories tend to leave more 5-star reviews than others?

## Dataset Overview

Total Ratings: 2,067,529

Unique Podcasts: 110,024

Categories: 110

Rating Range: 1 to 5

Data Range: 2005–12–10 → 2023–02–16

Tables: reviews, podcasts, categories, runs

Missing Values: None in critical fields

📊 Exploratory Data Analysis (EDA)
1. Rating Summary
Metric	Value
Avg Rating	4.627
Min Rating	1
Max Rating	5

Ratings show strong positive skew (majority 4–5).

2. Top 10 Categories by Review Count

society-culture (441,874)

comedy (350,848)

education (221,831)

business (210,081)

news (180,552)

sports (175,709)

health-fitness (174,310)

3. Top 10 Categories by Average Rating (> 1000 reviews)

business-marketing (4.9371)

business-entrepreneurship (4.9083)

sports-running (4.8920)

science-chemistry (4.8827)

health-nutrition (4.8809)

education-self-improvement (4.8767)

Business subcategories dominate rating performance.

📈 Outlier Analysis (IQR Method)

Outliers identified in:

review_count

mean_rating

std_rating

Findings:

Many categories have tightly clustered average ratings (4.6–4.9).

A few extremely popular podcasts have 100k+ reviews.

Standard deviation varies widely—some categories have polarized audiences.

📉 Correlation: Number of Reviews vs Rating

Pearson r = –0.14

Weak negative correlation

Popular podcasts tend to have slightly lower average ratings.

🎞️ Rating Trends Over Time (2010–2022)
Key Observations

2015 = Peak year for most categories

Declines start after 2019

2022 = Uniform drop across almost all categories

Business, Education, and Health remain consistently high

News maintains the lowest and most volatile ratings

📚 Confidence Intervals
Arts Category (n = 136,508)

95% CI: [4.7231, 4.7325]

Extremely narrow due to large sample size → precise estimate.

🧪 Statistical Hypothesis Testing
1. ANOVA: Arts Subcategories

F-statistic: 112.97, p < 0.001

Significant differences exist across arts subcategories

Ranking (highest → lowest):

arts-visual-arts

arts-design

arts-food

arts-performing-arts

arts-books

arts-fashion-beauty (lowest)

2. Independent T-test: Comedy vs News
Category	Mean
Comedy	4.623
News	4.301

t-statistic: 86.84

p-value < 0.0001

Comedy significantly outperforms News

3. Paired T-test: Ratings 2021 vs 2022

Mean(2021) = 4.6624

Mean(2022) = 4.5897

Difference = –0.0727

p-value < 0.0001

Significant decline (~–1.45%) in 2022

4. ANOVA Across All Main Categories

F = 283.27, p < 0.001

All categories differ significantly

Only Technology vs TV-Film showed no significant difference

Highest-rated categories:

Business (4.851)

Education (4.827)

Health (4.789)

Lowest-rated:

News (4.332)

True Crime (4.16)

⭐ 5-Star Rating Analysis

Most categories show strong 5-star dominance

News, Society-Culture, and Other have elevated 1–2 star rates

Chi-Square test → p < 0.001

Category strongly influences negative rating probability

📝 Comment Length vs Rating

Pearson r = –0.097

Spearman ρ = –0.089

Weak but statistically significant (due to huge sample)

Longer comments slightly more likely to give lower ratings.

🔄 Updates vs Rating Relationship

Pearson = –0.039 (very weak negative)

Spearman = –0.399 (moderate negative monotonic trend)

Heavily updated podcasts tend to have slightly lower average ratings.

📌 Conclusions
1. Category Performance

Business, Education, Health consistently lead (avg ⭐ > 4.80)

News performs the worst (avg ⭐ ≈ 4.33)

2. Temporal Trends

2015 = ecosystem peak

2022 = strongest decline

3. Variability & Distribution

News has the highest variance

Business the most consistent

4. Correlation Insights

Popular podcasts (more reviews) get slightly lower ratings

Comment length negatively correlates (weak)

5. Statistical Tests

Almost all categories significantly differ

Comedy ≫ News

2021 → 2022 decline statistically confirmed

📌 Recommendations
Content & Strategy

Invest in Business, Education, Health categories

Rebuild News content quality: depth, reliability, format

Create separate content strategies for high-volume categories (Society, Comedy)

Rating System Improvements

Consider multi-dimensional feedback

Reduce 5-star inflation

Add metrics like: content quality, production, originality

Algorithm Optimization

Weight ratings by:

Review count

Category distribution

Variance

Improve niche podcast discoverability

Category-Specific Actions

Practical content for Business/Education

High-structure formats for News

Engagement-focused content for Society-Culture & Comedy

📌 Future Work

Deeper analysis of rating declines post-2019

NLP on review text to detect sentiment & themes

Demographic–rating behavior modeling

Seasonal or cyclical trends in rating behavior

Predictive modeling for rating outcomes

Deeper analysis of five-star behavior by audience type

📬 Contact

Mustafa Akgül
Data Analyst & Machine Learning Practitioner
GitHub: https://github.com/mustafaakgl
