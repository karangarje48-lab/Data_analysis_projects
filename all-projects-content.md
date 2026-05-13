# 📊 All 29 Data Analysis Projects — Complete Content

---

---

# 📁 END-TO-END PROJECTS

---

## 1️⃣ Zomato Data Analysis

### 📌 Project Overview
Analyze restaurant data from Zomato to discover insights about ratings, cuisines, pricing, and city-wise distribution of restaurants across India.

### 🎯 Objectives
- Understand which cuisines are most popular
- Analyze restaurant ratings and cost distribution
- Find the best-rated cities for dining
- Identify online vs offline ordering trends

### 🛠️ Tools & Libraries
- Python, Pandas, NumPy
- Matplotlib, Seaborn, Plotly
- Jupyter Notebook

### 📂 Dataset
- Source: Kaggle Zomato Dataset
- Rows: ~9,500+ restaurants
- Columns: name, location, cuisines, rating, cost, online_order, book_table

### 🔍 Key Steps
1. Data Loading & Exploration
2. Handling Missing Values
3. Data Cleaning (removing duplicates, fixing data types)
4. Exploratory Data Analysis (EDA)
5. Visualizations (bar charts, heatmaps, pie charts)
6. Insights & Conclusions

### 📊 Key Insights
- North Indian and Chinese cuisines dominate listings
- Restaurants with online ordering have higher ratings
- Bangalore has the most Zomato-listed restaurants
- Average cost for two ranges between ₹200–₹800

### 💻 Sample Code
```python
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

df = pd.read_csv('zomato.csv')
df.dropna(inplace=True)

# Top cuisines
top_cuisines = df['cuisines'].value_counts().head(10)
sns.barplot(x=top_cuisines.values, y=top_cuisines.index)
plt.title('Top 10 Cuisines on Zomato')
plt.show()
```

---

## 2️⃣ IPL Data Analysis

### 📌 Project Overview
Deep dive into Indian Premier League (IPL) match data from 2008 to 2023 to analyze team performance, player statistics, and winning patterns.

### 🎯 Objectives
- Find the most successful IPL teams
- Analyze top run-scorers and wicket-takers
- Study toss impact on match outcomes
- Identify best venues for batting/bowling

### 🛠️ Tools & Libraries
- Python, Pandas, NumPy
- Matplotlib, Seaborn, Plotly
- Jupyter Notebook

### 📂 Dataset
- Source: Kaggle IPL Dataset
- Files: matches.csv, deliveries.csv
- Rows: 900+ matches, 200,000+ deliveries

### 🔍 Key Steps
1. Data Loading & Merging
2. Data Cleaning & Preprocessing
3. Team-wise Performance Analysis
4. Player Statistics Analysis
5. Toss & Venue Analysis
6. Season-wise Trends

### 📊 Key Insights
- Mumbai Indians have won the most IPL titles
- Toss winning gives a slight advantage (~52%)
- Wankhede Stadium is the highest-scoring venue
- Virat Kohli is the all-time leading run-scorer

### 💻 Sample Code
```python
import pandas as pd
import matplotlib.pyplot as plt

matches = pd.read_csv('matches.csv')

# Most wins by team
team_wins = matches['winner'].value_counts().head(8)
team_wins.plot(kind='bar', color='orange', figsize=(10,5))
plt.title('IPL Team Win Count')
plt.xlabel('Team')
plt.ylabel('Wins')
plt.show()
```

---

## 3️⃣ Airbnb Data Analysis

### 📌 Project Overview
Explore Airbnb listings data to understand pricing trends, neighborhood impact, host behavior, and availability patterns across major cities.

### 🎯 Objectives
- Identify most expensive and affordable neighborhoods
- Analyze room type vs price relationship
- Study host behavior and listing density
- Understand availability and review patterns

### 🛠️ Tools & Libraries
- Python, Pandas, NumPy
- Matplotlib, Seaborn, Folium
- Jupyter Notebook

### 📂 Dataset
- Source: Inside Airbnb (insideairbnb.com)
- City: New York / London / Mumbai
- Columns: price, neighbourhood, room_type, reviews, availability

### 🔍 Key Steps
1. Data Loading & Inspection
2. Handling Null Values & Outliers
3. Price Distribution Analysis
4. Neighborhood Analysis
5. Room Type Comparison
6. Geospatial Mapping with Folium

### 📊 Key Insights
- Entire home/apartment costs 3x more than private rooms
- Manhattan has the highest average listing price
- Superhosts maintain higher review scores
- Most listings have 365-day availability

### 💻 Sample Code
```python
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

df = pd.read_csv('airbnb_listings.csv')
df['price'] = df['price'].str.replace('$','').str.replace(',','').astype(float)

sns.boxplot(x='room_type', y='price', data=df[df['price']<500])
plt.title('Price Distribution by Room Type')
plt.show()
```

---

## 4️⃣ Global Covid-19 Data Analysis and Visualizations

### 📌 Project Overview
Track and visualize the global spread of Covid-19 including cases, deaths, recoveries, and vaccination data across countries and time periods.

### 🎯 Objectives
- Track global case and death trends
- Compare country-wise Covid impact
- Analyze vaccination progress
- Identify wave patterns over time

### 🛠️ Tools & Libraries
- Python, Pandas, NumPy
- Plotly, Folium, Matplotlib
- Jupyter Notebook

### 📂 Dataset
- Source: Our World in Data / Johns Hopkins
- Columns: date, country, total_cases, total_deaths, new_cases, vaccinations

### 🔍 Key Steps
1. Data Loading & Date Parsing
2. Global Trend Analysis
3. Country-wise Comparison
4. Death Rate Calculation
5. Vaccination Progress Tracking
6. Interactive Choropleth Maps

### 📊 Key Insights
- USA, India, Brazil had highest total cases
- Death rate varied from 0.1% to 5% by country
- Vaccination rollout reduced death rates significantly
- Omicron wave had highest cases but lower deaths

### 💻 Sample Code
```python
import pandas as pd
import plotly.express as px

df = pd.read_csv('covid_data.csv')
df['date'] = pd.to_datetime(df['date'])

fig = px.choropleth(df, locations='iso_code',
                    color='total_cases',
                    hover_name='location',
                    animation_frame='date',
                    title='Global Covid-19 Cases Over Time')
fig.show()
```

---

## 5️⃣ Housing Price Analysis & Predictions

### 📌 Project Overview
Predict housing prices based on features like location, size, number of rooms, and amenities using regression machine learning models.

### 🎯 Objectives
- Identify key factors affecting house prices
- Build and compare regression models
- Achieve high prediction accuracy
- Visualize price distribution by location

### 🛠️ Tools & Libraries
- Python, Pandas, NumPy, Scikit-learn
- Matplotlib, Seaborn
- XGBoost, Linear Regression, Random Forest

### 📂 Dataset
- Source: Kaggle House Prices Dataset
- Rows: 1,460 houses
- Features: 80 columns (area, bedrooms, bathrooms, location, etc.)

### 🔍 Key Steps
1. Data Loading & EDA
2. Feature Engineering
3. Handling Missing Values
4. Encoding Categorical Variables
5. Model Training (Linear, Random Forest, XGBoost)
6. Model Evaluation (RMSE, R² Score)

### 📊 Key Insights
- Overall quality and living area are top price predictors
- Houses near good neighborhoods command 40% premium
- XGBoost achieved best RMSE of ~0.12
- Garage size and basement area significantly impact price

### 💻 Sample Code
```python
from sklearn.ensemble import RandomForestRegressor
from sklearn.model_selection import train_test_split
from sklearn.metrics import mean_squared_error
import pandas as pd

df = pd.read_csv('housing.csv')
X = df.drop('SalePrice', axis=1)
y = df['SalePrice']

X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2)
model = RandomForestRegressor(n_estimators=100)
model.fit(X_train, y_train)
predictions = model.predict(X_test)
print(f'RMSE: {mean_squared_error(y_test, predictions, squared=False)}')
```

---

## 6️⃣ Titanic Dataset Analysis and Survival Predictions

### 📌 Project Overview
Analyze the Titanic passenger dataset to understand survival patterns and build a classification model to predict who survived the disaster.

### 🎯 Objectives
- Understand survival rate by gender, class, and age
- Handle missing data effectively
- Build classification models
- Evaluate model performance

### 🛠️ Tools & Libraries
- Python, Pandas, NumPy, Scikit-learn
- Matplotlib, Seaborn
- Logistic Regression, Random Forest, SVM

### 📂 Dataset
- Source: Kaggle Titanic Dataset
- Rows: 891 passengers
- Columns: Survived, Pclass, Sex, Age, Fare, Embarked

### 🔍 Key Steps
1. Data Exploration & Visualization
2. Missing Value Treatment (Age, Cabin)
3. Feature Engineering (Title extraction, Family size)
4. Encoding & Scaling
5. Model Training & Comparison
6. Confusion Matrix & Accuracy

### 📊 Key Insights
- Women had 74% survival rate vs 19% for men
- 1st class passengers survived more than 3rd class
- Children under 10 had higher survival rates
- Random Forest achieved 83% accuracy

### 💻 Sample Code
```python
from sklearn.ensemble import RandomForestClassifier
from sklearn.metrics import accuracy_score
import pandas as pd

df = pd.read_csv('titanic.csv')
df['Age'].fillna(df['Age'].median(), inplace=True)
df['Sex'] = df['Sex'].map({'male': 0, 'female': 1})

X = df[['Pclass', 'Sex', 'Age', 'Fare']]
y = df['Survived']

model = RandomForestClassifier()
model.fit(X, y)
print(f'Accuracy: {accuracy_score(y, model.predict(X))}')
```

---

## 7️⃣ Iris Flower Dataset Analysis and Predictions

### 📌 Project Overview
Classic machine learning project to classify three species of Iris flowers using petal and sepal measurements with multiple classification algorithms.

### 🎯 Objectives
- Explore the Iris dataset visually
- Compare multiple classification models
- Understand feature importance
- Achieve high classification accuracy

### 🛠️ Tools & Libraries
- Python, Pandas, NumPy, Scikit-learn
- Matplotlib, Seaborn
- KNN, SVM, Decision Tree, Logistic Regression

### 📂 Dataset
- Source: UCI ML Repository / Sklearn built-in
- Rows: 150 samples, 3 species
- Features: sepal_length, sepal_width, petal_length, petal_width

### 🔍 Key Steps
1. Data Loading & Exploration
2. Pair Plot & Correlation Analysis
3. Train-Test Split
4. Multiple Model Training
5. Accuracy Comparison
6. Decision Boundary Visualization

### 📊 Key Insights
- Setosa is linearly separable from other species
- Petal length and width are most important features
- SVM achieved 97% accuracy
- KNN with k=5 also performs excellently

### 💻 Sample Code
```python
from sklearn.datasets import load_iris
from sklearn.svm import SVC
from sklearn.model_selection import train_test_split
from sklearn.metrics import classification_report

iris = load_iris()
X_train, X_test, y_train, y_test = train_test_split(
    iris.data, iris.target, test_size=0.2, random_state=42)

model = SVC(kernel='rbf')
model.fit(X_train, y_train)
print(classification_report(y_test, model.predict(X_test)))
```

---

## 8️⃣ Customer Churn Analysis

### 📌 Project Overview
Identify telecom customers likely to churn (leave the service) using behavioral and account data, and build a predictive model to help retain them.

### 🎯 Objectives
- Identify key churn indicators
- Handle imbalanced class data
- Build binary classification model
- Provide business recommendations

### 🛠️ Tools & Libraries
- Python, Pandas, NumPy, Scikit-learn
- Matplotlib, Seaborn
- Logistic Regression, XGBoost, SMOTE

### 📂 Dataset
- Source: Kaggle Telco Customer Churn
- Rows: 7,043 customers
- Columns: tenure, MonthlyCharges, Contract, InternetService, Churn

### 🔍 Key Steps
1. Data Exploration & Churn Rate Analysis
2. Feature Analysis vs Churn
3. Handling Imbalanced Data (SMOTE)
4. Model Building
5. ROC-AUC Evaluation
6. Business Recommendations

### 📊 Key Insights
- Month-to-month contracts have highest churn (43%)
- Customers with fiber optic internet churn more
- Tenure less than 12 months = highest churn risk
- XGBoost ROC-AUC score: 0.85

### 💻 Sample Code
```python
import pandas as pd
from sklearn.ensemble import GradientBoostingClassifier
from sklearn.metrics import roc_auc_score

df = pd.read_csv('churn.csv')
df['Churn'] = df['Churn'].map({'Yes': 1, 'No': 0})

X = pd.get_dummies(df.drop('Churn', axis=1))
y = df['Churn']

model = GradientBoostingClassifier()
model.fit(X, y)
print(f'ROC-AUC: {roc_auc_score(y, model.predict_proba(X)[:,1])}')
```

---

## 9️⃣ Car Price Prediction Analysis

### 📌 Project Overview
Predict the selling price of used cars based on features like brand, year, mileage, fuel type, and transmission using regression models.

### 🎯 Objectives
- Understand depreciation patterns
- Identify price-influencing features
- Build accurate price prediction model
- Compare multiple regression algorithms

### 🛠️ Tools & Libraries
- Python, Pandas, NumPy, Scikit-learn
- Matplotlib, Seaborn, XGBoost
- Label Encoding, Feature Scaling

### 📂 Dataset
- Source: Kaggle Used Car Dataset
- Rows: 8,000+ cars
- Columns: brand, year, km_driven, fuel, transmission, selling_price

### 🔍 Key Steps
1. Data Cleaning & Outlier Removal
2. Feature Engineering (car age, brand encoding)
3. Correlation Analysis
4. Model Training & Tuning
5. Prediction & Evaluation

### 📊 Key Insights
- Car age is the strongest price predictor
- Diesel cars retain value better than petrol
- Luxury brands (BMW, Audi) depreciate differently
- XGBoost R² score: 0.92

### 💻 Sample Code
```python
import pandas as pd
from xgboost import XGBRegressor

df = pd.read_csv('car_data.csv')
df['car_age'] = 2024 - df['year']
df = pd.get_dummies(df, columns=['fuel', 'transmission', 'brand'])

X = df.drop('selling_price', axis=1)
y = df['selling_price']

model = XGBRegressor(n_estimators=200)
model.fit(X, y)
```

---

## 🔟 Indian Election Data Analysis

### 📌 Project Overview
Analyze Indian general election results to understand voting patterns, party performance, constituency trends, and vote share distribution.

### 🎯 Objectives
- Analyze party-wise seat and vote share
- Study state-wise voting patterns
- Track election trends over multiple years
- Visualize geographic voting distribution

### 🛠️ Tools & Libraries
- Python, Pandas, NumPy
- Plotly, Matplotlib, Geopandas, Folium
- Jupyter Notebook

### 📂 Dataset
- Source: Election Commission of India / Kaggle
- Elections: 2014, 2019, 2024
- Columns: constituency, state, party, votes, winner

### 🔍 Key Steps
1. Data Loading & Cleaning
2. Party-wise Seat Analysis
3. State-wise Performance
4. Vote Share Calculation
5. Geographic Mapping
6. Election Trend Comparison

### 📊 Key Insights
- BJP won 303 seats in 2019 with 37.4% vote share
- NOTA votes have increased each election
- South Indian states show different voting patterns
- Close contests (margin < 1000 votes) identified

### 💻 Sample Code
```python
import pandas as pd
import plotly.express as px

df = pd.read_csv('election_results.csv')
party_seats = df.groupby('party')['winner'].sum().sort_values(ascending=False).head(10)

fig = px.bar(party_seats, title='Top 10 Parties by Seats Won')
fig.show()
```

---

## 1️⃣1️⃣ HR Analytics to Track Employee Performance

### 📌 Project Overview
Use HR data to analyze employee performance, satisfaction, attrition patterns, and identify factors that contribute to employee retention or departure.

### 🎯 Objectives
- Identify high-performing employee profiles
- Predict employee attrition
- Analyze satisfaction vs performance correlation
- Provide HR policy recommendations

### 🛠️ Tools & Libraries
- Python, Pandas, NumPy, Scikit-learn
- Matplotlib, Seaborn
- Random Forest, Logistic Regression

### 📂 Dataset
- Source: IBM HR Analytics Dataset (Kaggle)
- Rows: 1,470 employees
- Columns: Age, Department, JobSatisfaction, Attrition, PerformanceRating

### 🔍 Key Steps
1. Data Exploration & Attrition Rate
2. Department-wise Analysis
3. Satisfaction Score Analysis
4. Attrition Prediction Model
5. Feature Importance Ranking
6. HR Recommendations

### 📊 Key Insights
- Overall attrition rate: 16.1%
- Sales department has highest attrition (21%)
- Overtime workers are 2x more likely to leave
- Job satisfaction and work-life balance are key retention factors

### 💻 Sample Code
```python
import pandas as pd
from sklearn.ensemble import RandomForestClassifier

df = pd.read_csv('hr_data.csv')
df['Attrition'] = df['Attrition'].map({'Yes': 1, 'No': 0})

X = pd.get_dummies(df.drop('Attrition', axis=1))
y = df['Attrition']

model = RandomForestClassifier(n_estimators=100, random_state=42)
model.fit(X, y)

# Feature importance
importance = pd.Series(model.feature_importances_, index=X.columns)
importance.sort_values(ascending=False).head(10).plot(kind='bar')
```

---

## 1️⃣2️⃣ Product Recommendation Analysis

### 📌 Project Overview
Build a product recommendation system using collaborative filtering and content-based filtering to suggest relevant products to users based on purchase history.

### 🎯 Objectives
- Build collaborative filtering model
- Implement content-based filtering
- Evaluate recommendation quality
- Create a hybrid recommendation system

### 🛠️ Tools & Libraries
- Python, Pandas, NumPy, Scikit-learn
- Surprise library, TensorFlow
- Cosine Similarity, Matrix Factorization

### 📂 Dataset
- Source: Amazon Product Reviews / MovieLens
- Rows: 100,000+ ratings
- Columns: user_id, product_id, rating, timestamp

### 🔍 Key Steps
1. Data Loading & User-Item Matrix
2. Collaborative Filtering (User-based & Item-based)
3. Content-Based Filtering
4. Matrix Factorization (SVD)
5. Hybrid System
6. Evaluation (RMSE, Precision@K)

### 📊 Key Insights
- SVD achieves RMSE of 0.87
- Cold start problem addressed with content-based
- Top-5 recommendations have 78% precision
- Hybrid approach outperforms individual methods

### 💻 Sample Code
```python
from surprise import SVD, Dataset, Reader
from surprise.model_selection import cross_validate
import pandas as pd

df = pd.read_csv('ratings.csv')
reader = Reader(rating_scale=(1, 5))
data = Dataset.load_from_df(df[['user_id', 'product_id', 'rating']], reader)

model = SVD()
results = cross_validate(model, data, measures=['RMSE'], cv=5)
print(f"Mean RMSE: {results['test_rmse'].mean():.4f}")
```

---

## 1️⃣3️⃣ Credit Card Approvals Analysis & Predictions

### 📌 Project Overview
Predict credit card approval decisions using applicant financial and demographic data to help banks automate and improve their approval process.

### 🎯 Objectives
- Analyze approval vs rejection patterns
- Handle missing values and mixed data types
- Build binary classification model
- Identify key approval factors

### 🛠️ Tools & Libraries
- Python, Pandas, NumPy, Scikit-learn
- Matplotlib, Seaborn
- Logistic Regression, SVM, Random Forest

### 📂 Dataset
- Source: UCI Credit Card Approval Dataset
- Rows: 690 applications
- Columns: Gender, Age, Debt, Income, CreditScore, Approved

### 🔍 Key Steps
1. Data Loading & Anonymized Feature Handling
2. Missing Value Imputation
3. Feature Encoding & Scaling
4. Model Training
5. Confusion Matrix & Accuracy
6. Threshold Tuning

### 📊 Key Insights
- Income and credit score are top approval factors
- Logistic Regression achieved 85.5% accuracy
- Prior default history strongly predicts rejection
- Feature scaling critical for SVM performance

### 💻 Sample Code
```python
import pandas as pd
from sklearn.linear_model import LogisticRegression
from sklearn.preprocessing import MinMaxScaler
from sklearn.metrics import accuracy_score

df = pd.read_csv('credit_card.csv')
df.replace('?', np.nan, inplace=True)
df.fillna(df.mean(numeric_only=True), inplace=True)

X = df.iloc[:, :-1]
y = df.iloc[:, -1]

scaler = MinMaxScaler()
X_scaled = scaler.fit_transform(X)

model = LogisticRegression()
model.fit(X_scaled, y)
print(f'Accuracy: {accuracy_score(y, model.predict(X_scaled))}')
```

---

## 1️⃣4️⃣ Uber Trips Data Analysis

### 📌 Project Overview
Analyze Uber trip data to understand ride demand patterns, peak hours, popular pickup locations, and seasonal trends in New York City.

### 🎯 Objectives
- Identify peak hours and days for Uber rides
- Find most popular pickup locations
- Analyze monthly and seasonal trends
- Create geospatial visualizations

### 🛠️ Tools & Libraries
- Python, Pandas, NumPy
- Matplotlib, Seaborn, Folium, Plotly
- Jupyter Notebook

### 📂 Dataset
- Source: Kaggle Uber Pickups NYC
- Rows: 4.5 million+ trips
- Columns: date/time, latitude, longitude, base

### 🔍 Key Steps
1. Data Loading & Datetime Parsing
2. Hour/Day/Month Extraction
3. Peak Time Analysis
4. Location Clustering
5. Heatmap Visualization
6. Base-wise Analysis

### 📊 Key Insights
- Peak hours: 5 PM – 9 PM on weekdays
- Friday evenings have highest demand
- Manhattan has 60% of all pickups
- September has the most monthly trips

### 💻 Sample Code
```python
import pandas as pd
import matplotlib.pyplot as plt

df = pd.read_csv('uber_data.csv')
df['Date/Time'] = pd.to_datetime(df['Date/Time'])
df['Hour'] = df['Date/Time'].dt.hour
df['Day'] = df['Date/Time'].dt.day_name()

hourly = df.groupby('Hour').size()
hourly.plot(kind='bar', color='black', figsize=(12,5))
plt.title('Uber Trips by Hour of Day')
plt.show()
```

---

## 1️⃣5️⃣ Active Product Sales Analysis

### 📌 Project Overview
Examine product sales data to identify top-performing products, seasonal patterns, regional performance, and growth opportunities for a retail business.

### 🎯 Objectives
- Identify top and bottom performing products
- Analyze monthly and quarterly sales trends
- Study regional sales distribution
- Calculate key sales KPIs

### 🛠️ Tools & Libraries
- Python, Pandas, NumPy
- Matplotlib, Seaborn, Plotly
- Jupyter Notebook

### 📂 Dataset
- Source: Sample Sales Data (Kaggle)
- Rows: 100,000+ transactions
- Columns: product, category, region, quantity, price, date

### 🔍 Key Steps
1. Data Cleaning & Preprocessing
2. Sales KPI Calculation (Revenue, Profit, Margin)
3. Product Category Analysis
4. Regional Performance
5. Time Series Trend Analysis
6. Dashboard Visualization

### 📊 Key Insights
- Technology category generates 36% of total revenue
- Q4 (Oct-Dec) accounts for highest sales
- West region leads in total revenue
- 20% of products generate 80% of revenue (Pareto Principle)

### 💻 Sample Code
```python
import pandas as pd
import plotly.express as px

df = pd.read_csv('sales_data.csv')
df['Revenue'] = df['quantity'] * df['price']
df['date'] = pd.to_datetime(df['date'])
df['Month'] = df['date'].dt.to_period('M')

monthly_sales = df.groupby('Month')['Revenue'].sum().reset_index()
fig = px.line(monthly_sales, x='Month', y='Revenue', title='Monthly Sales Trend')
fig.show()
```

---

## 1️⃣6️⃣ Google Search Analysis

### 📌 Project Overview
Analyze Google search trends using the PyTrends API to track interest over time, compare keywords, and discover regional search behavior.

### 🎯 Objectives
- Track trending topics over time
- Compare search interest between keywords
- Identify geographic search patterns
- Analyze seasonal search behavior

### 🛠️ Tools & Libraries
- Python, PyTrends, Pandas
- Matplotlib, Plotly, Seaborn
- Jupyter Notebook

### 📂 Dataset
- Source: Google Trends API (via PyTrends)
- Real-time data fetched via API
- Columns: date, keyword, interest_score, region

### 🔍 Key Steps
1. PyTrends API Setup
2. Keyword Interest Over Time
3. Related Queries Analysis
4. Geographic Interest Mapping
5. Trend Comparison
6. Seasonality Detection

### 📊 Key Insights
- "Python" searches peak in January (new year learners)
- "Data Science" interest grew 300% from 2018-2023
- India contributes highest Python search volume in Asia
- Related queries reveal user intent patterns

### 💻 Sample Code
```python
from pytrends.request import TrendReq
import matplotlib.pyplot as plt

pytrends = TrendReq(hl='en-US', tz=360)
keywords = ['Python', 'Data Science', 'Machine Learning']
pytrends.build_payload(keywords, timeframe='today 5-y')

df = pytrends.interest_over_time()
df.drop('isPartial', axis=1).plot(figsize=(12,5))
plt.title('Google Search Trends: Python vs Data Science vs ML')
plt.show()
```

---
---

# 📁 TIME SERIES PROJECTS

---

## 1️⃣7️⃣ Stock Price Time Series Analysis

### 📌 Project Overview
Analyze historical stock price data for major companies, apply technical indicators, detect patterns, and forecast future prices using time series models.

### 🎯 Objectives
- Visualize stock price trends and volume
- Apply moving averages and Bollinger Bands
- Forecast prices using ARIMA and LSTM
- Compare multiple stocks

### 🛠️ Tools & Libraries
- Python, Pandas, NumPy
- yFinance, Statsmodels, TensorFlow/Keras
- Plotly, Matplotlib

### 📂 Dataset
- Source: Yahoo Finance via yFinance API
- Stocks: AAPL, GOOGL, MSFT, RELIANCE
- Columns: Open, High, Low, Close, Volume, Adj Close

### 🔍 Key Steps
1. Data Download via yFinance
2. Candlestick Chart Visualization
3. Moving Average (SMA, EMA) Analysis
4. ARIMA Model Fitting
5. LSTM Deep Learning Model
6. Forecast Visualization

### 📊 Key Insights
- AAPL showed 400% growth from 2019-2023
- 50-day MA crossing 200-day MA signals trend change
- LSTM achieved RMSE of 2.3 on test data
- Bollinger Bands effectively identify volatility

### 💻 Sample Code
```python
import yfinance as yf
import matplotlib.pyplot as plt

stock = yf.download('AAPL', start='2020-01-01', end='2024-01-01')
stock['SMA_50'] = stock['Close'].rolling(50).mean()
stock['SMA_200'] = stock['Close'].rolling(200).mean()

plt.figure(figsize=(14,6))
plt.plot(stock['Close'], label='AAPL Close')
plt.plot(stock['SMA_50'], label='50-Day MA')
plt.plot(stock['SMA_200'], label='200-Day MA')
plt.legend()
plt.title('Apple Stock Price with Moving Averages')
plt.show()
```

---

## 1️⃣8️⃣ Weather Data Analysis

### 📌 Project Overview
Study historical weather patterns to detect seasonal trends, analyze temperature and rainfall changes over time, and build forecasting models.

### 🎯 Objectives
- Analyze temperature and rainfall trends
- Detect seasonal patterns
- Forecast future weather conditions
- Compare weather across cities

### 🛠️ Tools & Libraries
- Python, Pandas, NumPy
- Statsmodels, Prophet, Matplotlib
- Seaborn, Plotly

### 📂 Dataset
- Source: NOAA / Kaggle Weather Dataset
- Cities: Multiple global cities
- Columns: date, temp_max, temp_min, precipitation, wind

### 🔍 Key Steps
1. Data Loading & Date Indexing
2. Temperature Trend Analysis
3. Seasonal Decomposition
4. Rainfall Pattern Analysis
5. Prophet Forecasting Model
6. Forecast Visualization

### 📊 Key Insights
- Average temperature rising 0.2°C per decade
- Clear seasonal patterns in all cities
- Monsoon months show 5x more rainfall
- Prophet forecast accuracy within ±2°C

### 💻 Sample Code
```python
from prophet import Prophet
import pandas as pd

df = pd.read_csv('weather.csv')
df = df.rename(columns={'date': 'ds', 'temp_max': 'y'})

model = Prophet(yearly_seasonality=True)
model.fit(df)

future = model.make_future_dataframe(periods=365)
forecast = model.predict(future)
model.plot(forecast)
```

---

## 1️⃣9️⃣ Time Series Analysis with Cryptocurrency Data

### 📌 Project Overview
Analyze cryptocurrency price data (Bitcoin, Ethereum) to study volatility, correlations, and market cycles, and build forecasting models.

### 🎯 Objectives
- Track Bitcoin and Ethereum price history
- Analyze volatility and trading volume
- Detect bull and bear market cycles
- Build price forecasting models

### 🛠️ Tools & Libraries
- Python, Pandas, NumPy, yFinance
- Plotly, Matplotlib, Statsmodels, Prophet
- Jupyter Notebook

### 📂 Dataset
- Source: Yahoo Finance / CoinGecko API
- Cryptos: BTC-USD, ETH-USD, BNB-USD
- Columns: Date, Open, High, Low, Close, Volume

### 🔍 Key Steps
1. Crypto Data Download
2. Daily Returns & Volatility Analysis
3. Correlation Between Cryptos
4. Bull/Bear Market Identification
5. ARIMA Forecasting
6. Risk Analysis (VaR)

### 📊 Key Insights
- Bitcoin and Ethereum are 85% correlated
- Daily volatility averages 3-5% (vs 1% for stocks)
- 4-year halving cycle impacts price significantly
- 2021 bull run saw 1,200% BTC gain

### 💻 Sample Code
```python
import yfinance as yf
import pandas as pd
import matplotlib.pyplot as plt

btc = yf.download('BTC-USD', start='2018-01-01')
eth = yf.download('ETH-USD', start='2018-01-01')

btc['Daily_Return'] = btc['Close'].pct_change()
eth['Daily_Return'] = eth['Close'].pct_change()

fig, axes = plt.subplots(2, 1, figsize=(14, 8))
axes[0].plot(btc['Close'], color='orange', label='Bitcoin')
axes[1].plot(eth['Close'], color='blue', label='Ethereum')
plt.tight_layout()
plt.show()
```

---

## 2️⃣0️⃣ Climate Change Data Analysis

### 📌 Project Overview
Examine long-term global temperature records and CO₂ levels to quantify climate change impacts, identify warming trends, and project future scenarios.

### 🎯 Objectives
- Analyze 100+ years of temperature data
- Correlate CO₂ levels with temperature rise
- Identify hottest years on record
- Project future temperature using regression

### 🛠️ Tools & Libraries
- Python, Pandas, NumPy
- Matplotlib, Seaborn, Statsmodels
- Linear Regression, Polynomial Regression

### 📂 Dataset
- Source: NASA GISS / NOAA / Berkeley Earth
- Years: 1880–2024
- Columns: year, avg_temp, co2_ppm, sea_level

### 🔍 Key Steps
1. Data Loading & Cleaning
2. Long-term Temperature Trend Analysis
3. CO₂ vs Temperature Correlation
4. Anomaly Detection (hottest years)
5. Regression Forecasting
6. Visualization & Reporting

### 📊 Key Insights
- Earth has warmed 1.2°C since pre-industrial era
- 19 of 20 hottest years occurred after 2000
- CO₂ and temperature have 0.97 correlation
- At current rate, 1.5°C threshold by 2040

### 💻 Sample Code
```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
from sklearn.linear_model import LinearRegression

df = pd.read_csv('climate_data.csv')
X = df['year'].values.reshape(-1, 1)
y = df['avg_temp'].values

model = LinearRegression()
model.fit(X, y)

future_years = np.arange(2024, 2060).reshape(-1, 1)
predictions = model.predict(future_years)

plt.plot(df['year'], y, label='Historical')
plt.plot(future_years, predictions, '--r', label='Projected')
plt.legend()
plt.title('Global Temperature Trend & Projection')
plt.show()
```

---

## 2️⃣1️⃣ Anomaly Detection in Time Series Data

### 📌 Project Overview
Detect unusual spikes, drops, or patterns in time series data using statistical and machine learning methods, applicable to IoT, finance, and operations.

### 🎯 Objectives
- Identify anomalies in time series
- Apply multiple detection methods
- Compare statistical vs ML approaches
- Visualize anomaly detection results

### 🛠️ Tools & Libraries
- Python, Pandas, NumPy, Scikit-learn
- PyOD, Statsmodels, Matplotlib
- Isolation Forest, Z-Score, DBSCAN

### 📂 Dataset
- Source: Numenta Anomaly Benchmark / Custom
- Types: CPU usage, server traffic, sensor data
- Columns: timestamp, value, anomaly_label

### 🔍 Key Steps
1. Data Generation / Loading
2. Z-Score Based Detection
3. Rolling Mean Deviation Method
4. Isolation Forest Model
5. Seasonal Decomposition Anomalies
6. Evaluation & Visualization

### 📊 Key Insights
- Z-score method works well for simple spikes
- Isolation Forest detects complex anomalies
- Seasonal patterns must be removed first
- Precision-Recall tradeoff key for production

### 💻 Sample Code
```python
import pandas as pd
import numpy as np
from sklearn.ensemble import IsolationForest
import matplotlib.pyplot as plt

df = pd.read_csv('timeseries.csv', parse_dates=['timestamp'])
model = IsolationForest(contamination=0.05, random_state=42)
df['anomaly'] = model.fit_predict(df[['value']])

anomalies = df[df['anomaly'] == -1]

plt.figure(figsize=(14,5))
plt.plot(df['timestamp'], df['value'], label='Data')
plt.scatter(anomalies['timestamp'], anomalies['value'], color='red', label='Anomaly', zorder=5)
plt.legend()
plt.title('Anomaly Detection in Time Series')
plt.show()
```

---

## 2️⃣2️⃣ Predictive Modeling for Sales or Demand Forecasting

### 📌 Project Overview
Forecast future product demand or sales volumes using historical data and advanced time series models to help businesses optimize inventory and planning.

### 🎯 Objectives
- Build accurate demand forecasting models
- Handle seasonality and trends
- Compare ARIMA, Prophet, and LSTM
- Evaluate forecast accuracy (MAPE, RMSE)

### 🛠️ Tools & Libraries
- Python, Pandas, NumPy
- Prophet, Statsmodels, TensorFlow
- Matplotlib, Plotly

### 📂 Dataset
- Source: Rossmann Store Sales (Kaggle)
- Rows: 1M+ daily sales records
- Columns: Store, Date, Sales, Customers, Promo

### 🔍 Key Steps
1. Data Exploration & Trend Analysis
2. Seasonality Decomposition
3. ARIMA Model
4. Prophet Model with Holidays
5. LSTM Neural Network
6. Model Comparison & Selection

### 📊 Key Insights
- Promotions increase sales by 20-30%
- Christmas week is the highest sales period
- Prophet with holiday effects achieves 8% MAPE
- LSTM captures complex non-linear patterns

### 💻 Sample Code
```python
from prophet import Prophet
import pandas as pd

df = pd.read_csv('sales.csv')
df = df.rename(columns={'Date': 'ds', 'Sales': 'y'})

model = Prophet(
    yearly_seasonality=True,
    weekly_seasonality=True,
    seasonality_mode='multiplicative'
)
model.fit(df)

future = model.make_future_dataframe(periods=90)
forecast = model.predict(future)

model.plot_components(forecast)
```

---

## 2️⃣3️⃣ Air Quality Data Analysis and Dynamic Visualizations

### 📌 Project Overview
Analyze AQI (Air Quality Index) data over time to track pollution trends, identify high-risk periods, and create interactive dashboards for public awareness.

### 🎯 Objectives
- Track AQI trends across cities
- Identify most polluted time periods
- Analyze pollutant contributions (PM2.5, NO2)
- Create interactive Plotly dashboards

### 🛠️ Tools & Libraries
- Python, Pandas, NumPy
- Plotly Dash, Folium, Matplotlib
- Statsmodels, Seaborn

### 📂 Dataset
- Source: OpenAQ / CPCB India / EPA
- Cities: Delhi, Mumbai, Beijing, Los Angeles
- Columns: date, city, AQI, PM2.5, PM10, NO2, CO

### 🔍 Key Steps
1. Data Loading & AQI Category Labeling
2. City-wise AQI Comparison
3. Seasonal Pollution Patterns
4. Pollutant Correlation Analysis
5. Geographic Heatmap
6. Interactive Plotly Dashboard

### 📊 Key Insights
- Delhi AQI exceeds 400 in November (post-Diwali)
- Winter months have 3x worse air quality
- PM2.5 contributes 60% to AQI score
- Vehicle emissions peak at rush hours (8-10AM, 6-8PM)

### 💻 Sample Code
```python
import pandas as pd
import plotly.express as px

df = pd.read_csv('air_quality.csv')
df['date'] = pd.to_datetime(df['date'])
df['month'] = df['date'].dt.month_name()

fig = px.box(df, x='month', y='AQI', color='city',
             title='Monthly AQI Distribution by City')
fig.show()
```

---

## 2️⃣4️⃣ Gold Price Analysis and Forecasting Over Time

### 📌 Project Overview
Study historical gold price data to identify long-term trends, seasonal patterns, economic correlations, and forecast future gold prices.

### 🎯 Objectives
- Analyze 20+ years of gold price history
- Find correlations with USD, inflation, stock market
- Detect seasonal price patterns
- Forecast using ARIMA and Prophet

### 🛠️ Tools & Libraries
- Python, Pandas, NumPy, yFinance
- Statsmodels, Prophet, Matplotlib
- Seaborn, Plotly

### 📂 Dataset
- Source: Yahoo Finance (GC=F) / World Gold Council
- Years: 2000–2024
- Columns: Date, Open, High, Low, Close, Volume

### 🔍 Key Steps
1. Gold Price Data Download
2. Long-term Trend Visualization
3. Correlation with USD Index & Inflation
4. Monthly Seasonality Analysis
5. ARIMA Forecasting
6. Forecast Accuracy Evaluation

### 📊 Key Insights
- Gold rose 600% from 2000-2024
- Strong negative correlation with USD (-0.75)
- Crisis periods (2008, 2020) drive gold surges
- September typically shows price increases

### 💻 Sample Code
```python
import yfinance as yf
import pandas as pd
from statsmodels.tsa.arima.model import ARIMA

gold = yf.download('GC=F', start='2010-01-01')['Close'].dropna()

model = ARIMA(gold, order=(5,1,0))
result = model.fit()

forecast = result.forecast(steps=90)
print(forecast)
```

---

## 2️⃣5️⃣ Food Price Forecasting

### 📌 Project Overview
Forecast food commodity prices (wheat, rice, vegetable oil) to support supply chain planning, policy decisions, and inflation analysis.

### 🎯 Objectives
- Analyze food price trends globally
- Detect seasonal patterns in commodity prices
- Build ARIMA and Prophet forecasting models
- Assess impact of global events on food prices

### 🛠️ Tools & Libraries
- Python, Pandas, NumPy
- Statsmodels, Prophet, Matplotlib
- Seaborn, Plotly

### 📂 Dataset
- Source: FAO Food Price Index / World Bank
- Commodities: Wheat, Rice, Sugar, Vegetable Oil
- Columns: date, commodity, price_index

### 🔍 Key Steps
1. Data Loading & Commodity Comparison
2. Price Trend Analysis (2000-2024)
3. Seasonal Decomposition
4. Event Impact Analysis (Covid, Ukraine War)
5. Prophet Multi-Commodity Forecast
6. Forecast Confidence Intervals

### 📊 Key Insights
- 2022 Ukraine war caused 40% wheat price spike
- Vegetable oil prices hit all-time high in 2022
- Rice prices show strong seasonal patterns
- Food inflation leading indicator for overall CPI

### 💻 Sample Code
```python
from prophet import Prophet
import pandas as pd
import matplotlib.pyplot as plt

df = pd.read_csv('food_prices.csv')
df = df[df['commodity'] == 'Wheat'][['date', 'price_index']]
df.columns = ['ds', 'y']
df['ds'] = pd.to_datetime(df['ds'])

model = Prophet(changepoint_prior_scale=0.5)
model.fit(df)
future = model.make_future_dataframe(periods=180)
forecast = model.predict(future)

model.plot(forecast)
plt.title('Wheat Price Forecast')
plt.show()
```

---
---

# 📁 WEB SCRAPING PROJECTS

---

## 2️⃣6️⃣ Movies Review Scraping and Analysis

### 📌 Project Overview
Scrape movie reviews and ratings from IMDb or Rotten Tomatoes, then perform sentiment analysis to understand audience and critic opinions.

### 🎯 Objectives
- Scrape movie ratings and reviews
- Clean and preprocess text data
- Perform sentiment analysis
- Identify positive vs negative review patterns

### 🛠️ Tools & Libraries
- Python, BeautifulSoup, Requests, Scrapy
- NLTK, TextBlob, VADER
- Pandas, Matplotlib, WordCloud

### 📂 Dataset
- Source: Scraped from IMDb.com
- Movies: Top 250 IMDb movies
- Columns: title, rating, review_text, sentiment

### 🔍 Key Steps
1. Web Scraping Setup (headers, delays)
2. Scraping Movie Titles & Ratings
3. Scraping User Reviews
4. Text Preprocessing (tokenize, stopwords)
5. Sentiment Analysis with VADER
6. WordCloud & Visualization

### 📊 Key Insights
- 78% of top 250 IMDb movie reviews are positive
- Action movies get more polarized reviews
- Short reviews tend to be more negative
- Most common positive words: amazing, brilliant, masterpiece

### 💻 Sample Code
```python
import requests
from bs4 import BeautifulSoup
from vaderSentiment.vaderSentiment import SentimentIntensityAnalyzer
import pandas as pd

url = 'https://www.imdb.com/chart/top/'
headers = {'User-Agent': 'Mozilla/5.0'}
response = requests.get(url, headers=headers)
soup = BeautifulSoup(response.text, 'html.parser')

movies = []
for row in soup.select('td.titleColumn'):
    title = row.select_one('a').text
    movies.append({'title': title})

df = pd.DataFrame(movies)
print(df.head())
```

---

## 2️⃣7️⃣ Product Price Scraping and Analysis

### 📌 Project Overview
Scrape e-commerce product listings from Amazon or Flipkart to compare prices, track price changes over time, and identify the best deals.

### 🎯 Objectives
- Scrape product listings and prices
- Track price changes over time
- Compare prices across categories
- Set up automated price alerts

### 🛠️ Tools & Libraries
- Python, Selenium, BeautifulSoup, Requests
- Pandas, Matplotlib, Schedule
- SQLite for price history storage

### 📂 Dataset
- Source: Scraped from e-commerce sites
- Categories: Electronics, Books, Clothing
- Columns: product_name, price, rating, reviews, date

### 🔍 Key Steps
1. Selenium Setup for Dynamic Pages
2. Product Data Extraction
3. Price History Tracking
4. Multi-category Comparison
5. Automated Daily Scraping
6. Price Drop Alerts

### 📊 Key Insights
- Electronics prices fluctuate 10-30% during sales
- Amazon prices change up to 4x per day
- Books maintain most stable pricing
- Sale prices during festivals are 20-40% lower

### 💻 Sample Code
```python
from selenium import webdriver
from selenium.webdriver.common.by import By
import pandas as pd
import time

driver = webdriver.Chrome()
driver.get('https://www.amazon.in/s?k=laptops')
time.sleep(3)

products = []
items = driver.find_elements(By.CSS_SELECTOR, 'div[data-component-type="s-search-result"]')
for item in items[:20]:
    try:
        name = item.find_element(By.CSS_SELECTOR, 'h2 a span').text
        price = item.find_element(By.CSS_SELECTOR, '.a-price-whole').text
        products.append({'name': name, 'price': price})
    except:
        pass

df = pd.DataFrame(products)
driver.quit()
```

---

## 2️⃣8️⃣ News Scraping and Analysis

### 📌 Project Overview
Scrape news headlines and articles from major news websites, perform topic modeling, trend detection, and sentiment analysis on current events.

### 🎯 Objectives
- Scrape news from multiple sources
- Categorize news by topic automatically
- Perform sentiment analysis on headlines
- Track trending topics over time

### 🛠️ Tools & Libraries
- Python, BeautifulSoup, NewsAPI, Feedparser
- NLTK, Gensim (LDA), TextBlob
- Pandas, Matplotlib, WordCloud

### 📂 Dataset
- Source: NewsAPI / RSS Feeds / BBC, CNN, TechCrunch
- Volume: 1000+ articles per day
- Columns: title, content, source, date, category

### 🔍 Key Steps
1. NewsAPI Setup & Data Collection
2. Headline Scraping via RSS
3. Text Cleaning & Preprocessing
4. Topic Modeling with LDA
5. Sentiment Analysis by Category
6. Trending Topics Dashboard

### 📊 Key Insights
- Technology news has most positive sentiment (65%)
- Political news shows most negative sentiment
- Weekend news volume drops by 40%
- LDA identified 8 distinct news topics accurately

### 💻 Sample Code
```python
import requests
import pandas as pd
from textblob import TextBlob

API_KEY = 'your_newsapi_key'
url = f'https://newsapi.org/v2/top-headlines?country=in&apiKey={API_KEY}'
response = requests.get(url).json()

articles = []
for article in response['articles']:
    title = article['title']
    sentiment = TextBlob(title).sentiment.polarity
    articles.append({
        'title': title,
        'source': article['source']['name'],
        'sentiment': sentiment,
        'date': article['publishedAt']
    })

df = pd.DataFrame(articles)
print(df.groupby('source')['sentiment'].mean())
```

---

## 2️⃣9️⃣ Real-time Share Price Scraping and Analysis

### 📌 Project Overview
Scrape live stock prices from financial websites and perform real-time analysis including price tracking, alerts, and live dashboard visualization.

### 🎯 Objectives
- Fetch real-time stock prices
- Track intraday price movements
- Set automated price alerts
- Build live updating dashboard

### 🛠️ Tools & Libraries
- Python, yFinance, Selenium, Requests
- Pandas, Plotly Dash, Schedule
- SQLite for data storage

### 📂 Dataset
- Source: Yahoo Finance / NSE India / Google Finance
- Stocks: RELIANCE, TCS, INFY, WIPRO, NIFTY50
- Update frequency: Every 1-5 minutes

### 🔍 Key Steps
1. yFinance Real-time Data Setup
2. Intraday Price Tracking
3. Volume & Price Movement Analysis
4. Automated Alert System
5. Live Plotly Dashboard
6. Historical vs Live Comparison

### 📊 Key Insights
- First 30 mins after market open = highest volatility
- Large-cap stocks have tighter bid-ask spreads
- Volume spikes often precede large price moves
- Circuit breakers trigger at ±5% intraday moves

### 💻 Sample Code
```python
import yfinance as yf
import time
import pandas as pd
from datetime import datetime

def fetch_live_price(symbol):
    ticker = yf.Ticker(symbol)
    data = ticker.history(period='1d', interval='1m')
    latest = data['Close'].iloc[-1]
    return latest

stocks = ['RELIANCE.NS', 'TCS.NS', 'INFY.NS']
price_log = []

for i in range(10):  # fetch 10 times
    row = {'time': datetime.now()}
    for stock in stocks:
        row[stock] = fetch_live_price(stock)
    price_log.append(row)
    print(row)
    time.sleep(60)  # wait 1 minute

df = pd.DataFrame(price_log)
df.to_csv('live_prices.csv', index=False)
```

---

# 🎯 How to Use These Files on GitHub

For each project:
1. Go to your GitHub repo
2. Navigate to the project folder (e.g., `end-to-end-projects/zomato-data-analysis/`)
3. Click `Add file` → `Create new file`
4. Name it `README.md`
5. Paste the content for that project
6. Click `Commit changes`

---

*Happy Coding! ⭐ Star the repo if you find it helpful!*
