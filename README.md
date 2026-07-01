
Title: Movie Profitability Analysis: Budget, Genre, and Audience Engagement

Overview: This project explores the factors that influence movie financial success using data from The Movie Database (TMDb), API enrichment, and Wikipedia web scraping.

Research Questions: List the 7 questions from the report.

Data Collection: TMDb 5000 movies dataset, TMDb API for real-time metadata, and web scraping for Wikipedia page length.

Tools: Python, Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, Statsmodels, Requests.

Methodology: EDA (log transformation, outlier detection, correlation heatmaps), Pivot tables (Genres & Production Companies), OLS Multiple Linear Regression, Random Forest Regressor (with cross-validation), Hypothesis Testing (ANOVA).

Key Findings: Vote count is the #1 predictor (68.1% importance). Budget (9.3%) and ratings (6.4%) matter less. Genres like Adventure/Family dominate. Wikipedia length significantly correlates with revenue (ANOVA p < 0.001).


Movie Profitability Analysis: Budget, Genre, and Audience Engagement

Project Overview
This project performs an in-depth exploratory data analysis (EDA) and predictive modeling to identify the key drivers of movie profitability. By integrating financial data, genre classifications, production studio details, and digital visibility metrics (scraped from Wikipedia), this study determines what truly makes a movie commercially successful. 

The analysis leverages a random sample of 1,000 movies from The Movie Database (TMDb) and applies a mixed-method approach including statistical testing, linear regression, and machine learning.

Research Questions
The analysis is guided by the following questions:
1. Which factors (budget, genre, production company) most influence movie profit?
2. Which movie genres generate the highest average profit?
3. Which production companies consistently produce high-profit movies?
4. Does a higher movie budget lead to higher profit?
5. Is there a relationship between movie ratings and revenue?
6. How has movie profitability changed over the years?
7. Do movies with more online information (Wikipedia) earn more money?

Dataset
- Primary Data: [TMDB 5000 Movies Dataset](https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata) (Kaggle).
- API Enrichment: TMDb API (`api.txt`) used to fetch up-to-date ratings and popularity scores.
- Web Scraping: Wikipedia pages scraped to extract page length as a proxy for online information availability.

Tools & Libraries
- Languages: Python 
- Data Manipulation: Pandas, NumPy
- Data Visualization: Matplotlib, Seaborn
- Statistical Modeling: Statsmodels (OLS Regression)
- Machine Learning: Scikit-learn (Random Forest Regressor, Cross-Validation)
- Web Scraping: Requests, JSON
- Environment: Jupyter Notebook

Project Workflow
1. Data Cleaning: Handled missing values, parsed JSON columns (genres, production companies), and created new features (`profit`, `year`).
2. API & Scraping: Enriched the dataset using the TMDb API and scraped Wikipedia page lengths.
3. Exploratory Data Analysis (EDA):
   - Applied log-transformation to financial variables to correct skewness.
   - Outlier detection using Boxplots.
   - Correlation heatmaps to check linear relationships.
4. Statistical Analysis:
   - VIF (Variance Inflation Factor) check to ensure no multicollinearity.
   - OLS Multiple Linear Regression to quantify predictor importance.
   - ANOVA (Analysis of Variance) to test the impact of online information on revenue.
5. Machine Learning: Trained a Random Forest Regressor with 5-fold cross-validation to validate feature importance.
6. Visualizations: Created bar charts, scatter plots, and line charts to represent genre profitability, studio performance, and year-over-year trends.

 Key Findings
- Audience Engagement is King: vote_count (audience participation) is the strongest predictor of revenue, accounting for 68.1% of feature importance in the Random Forest model.
- Budget vs. Ratings: While log_budget (9.3%) and api_rating (6.4%) are statistically significant (p < 0.01), their practical impact on revenue is far smaller than user engagement.
- Top Performing Genres: Family, Adventure, and Fantasy films generate the highest average profits.
- Studio Dominance: Major studios like Disney and Warner Bros. consistently lead in average profitability.
- Digital Visibility Matters: Movies with longer Wikipedia pages (more online information) achieve significantly higher revenue (ANOVA: F = 88.82, p < 0.001).
- Temporal Trends: Profitability has increased sharply since the 1990s, peaking in the late 2000s.

Conclusions & Recommendations
For investors and filmmakers, the data suggests focusing on:
- Audience Engagement: Prioritize marketing and interactive campaigns to boost vote_count.
- Genre Selection: Target high-appeal genres (Adventure, Fantasy, Family) over niche categories.
- Online Presence: Invest in digital content and media coverage to increase online visibility.
- Budgeting: While budgets help, higher spending doesn't guarantee success if other factors (like genre and engagement) are ignored.
