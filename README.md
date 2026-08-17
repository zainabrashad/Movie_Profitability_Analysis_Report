# Movie Profitability Analysis   
An in-depth analysis of what truly drives movie financial success using TMDb data, API enrichment, Wikipedia web scraping, statistical modelling, and machine learning.

##  Project Overview  
This project explores the key factors behind movie profitability by integrating:

- Financial data (budget, revenue, profit)  
- Genre classifications  
- Production company metadata  
- Audience engagement metrics (vote_count, popularity)  
- Digital visibility (Wikipedia page length)

The dataset includes a random sample of **1,000 movies** from TMDb, enriched with API metadata and Wikipedia scraping.



##  Research Questions  
This analysis answers seven core questions:

1. Which factors (budget, genre, production company) most influence movie profit?  
2. Which movie genres generate the highest average profit?  
3. Which production companies consistently produce high-profit movies?  
4. Does a higher movie budget lead to higher profit?  
5. Is there a relationship between movie ratings and revenue?  
6. How has movie profitability changed over the years?  
7. Do movies with more online information (Wikipedia) earn more money?



##  Dataset  
### **Primary Data**
- TMDb 5000 Movies Dataset (Kaggle)

### **API Enrichment**
- TMDb API (ratings, popularity, vote_count)

### **Web Scraping**
- Wikipedia page length (proxy for online visibility)



##  Tools & Libraries  
- **Python**  
- Pandas, NumPy  
- Matplotlib, Seaborn  
- Statsmodels (OLS Regression)  
- Scikit-learn (Random Forest Regressor, Cross-Validation)  
- Requests, JSON  
- Jupyter Notebook  



##  Methodology  

### **Data Cleaning**
- Missing value handling  
- JSON parsing (genres, production companies)  
- Feature engineering (profit, year, log transformations)

### **API & Scraping**
- TMDb API for real-time metadata  
- Wikipedia scraping for page length

### **Exploratory Data Analysis (EDA)**
- Log transformation of skewed financial variables  
- Outlier detection (boxplots)  
- Correlation heatmaps  
- Pivot tables (genres & production companies)

### **Statistical Analysis**
- VIF (multicollinearity check)  
- OLS Multiple Linear Regression  
- ANOVA (impact of online information on revenue)

### **Machine Learning**
- Random Forest Regressor  
- 5-fold cross-validation  
- Feature importance ranking



##  Key Findings  

###  1. Audience Engagement Is King  
- **vote_count = 68.1% feature importance**  
- Strongest predictor of revenue  
- Engagement > budget, ratings, genre

###  2. Budget & Ratings
 2. Budget & Ratings Matter Less  
- log_budget = **9.3%**  
- api_rating = **6.4%**  
- Statistically significant (p < 0.01)  
- But practical impact is small compared to vote_count

###  3. Top Performing Genres  
- **Family, Adventure, Fantasy**  
- Highest average profits  
- Broad audience appeal drives commercial success

### 4. Studio Dominance  
- Disney, Pixar, Lucasfilm, Warner Bros.  
- Consistently produce high-profit movies

###  5. Online Visibility Matters  
- Longer Wikipedia pages → higher revenue  
- ANOVA: **F = 88.82, p < 0.001**  
- Digital presence strongly correlates with financial success

###  6. Profitability Over Time  
- Sharp increase since the 1990s  
- Peak profitability in late 2000s  
- Driven by global distribution & franchise filmmaking



##  Conclusions & Recommendations  

###  Focus on Audience Engagement  
Marketing, social media campaigns, and interactive content boost vote_count.

###  Choose High-Performing Genres  
Adventure, Fantasy, Family films consistently outperform niche genres.

###  Strengthen Online Presence  
Invest in digital media coverage, Wikipedia content, and online visibility.

###  Budget Smartly  
Higher budgets help, but **do not guarantee success** without strong engagement.

###  Use Predictive Models  
Integrate Random Forest + OLS insights into planning:  
- Revenue forecasting  
- Budget allocation  
- Genre selection  
- Studio partnerships



##  Project Structure  
-   Raw + enriched datasets  
-  TMDb API scripts  
-  Wikipedia scraping scripts  
-  EDA, regression, ML models  
-  Charts & plots  
-  Random Forest + OLS outputs  

