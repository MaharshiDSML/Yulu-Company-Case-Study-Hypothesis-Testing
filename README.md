# Yulu-Hypothesis-Testing
### Yulu- Hypothesis Testing

### About Yulu
- Yulu is India’s leading micro-mobility service provider, which offers unique vehicles for the daily commute. Starting off as a mission to eliminate traffic congestion in India, Yulu provides the safest commute solution through a user-friendly mobile app to enable shared, solo and sustainable commuting.
- Yulu zones are located at all the appropriate locations (including metro stations, bus stands, office spaces, residential areas, corporate offices, etc) to make those first and last miles smooth, affordable, and convenient!

### Business Problem
- Yulu has recently suffered considerable dips in its revenues.
- They have contracted a consulting company to understand the factors on which the demand for these shared electric cycles depends.
- Specifically, they want to understand the factors affecting the demand for these shared electric cycles in the Indian market.
- The company wants to know:
  - Which variables are significant in predicting the demand for shared electric cycles in the Indian market?
  - How well those variables describe the electric cycle demands?
 
### Dataset
Dataset Link: yulu_data.csv
- datetime: datetime
- season: season (1: spring, 2: summer, 3: fall, 4: winter)
- holiday: whether day is a holiday or not (extracted from http://dchr.dc.gov/page/holiday-schedule)
- workingday: if day is neither weekend nor holiday is 1, otherwise is 0.
- weather:
  1: Clear, Few clouds, partly cloudy, partly cloudy
  2: Mist + Cloudy, Mist + Broken clouds, Mist + Few clouds, Mist
  3: Light Snow, Light Rain + Thunderstorm + Scattered clouds, Light Rain + Scattered clouds
  4: Heavy Rain + Ice Pallets + Thunderstorm + Mist, Snow + Fog
- temp: temperature in Celsius
- atemp: feeling temperature in Celsius
- humidity: humidity
- windspeed: wind speed
- casual: count of casual users
- registered: count of registered users
- count: count of total rental bikes including both casual and registered

### Concept Used
- Bi-Variate Analysis
- 2-sample t-test: testing for difference across populations
- ANNOVA
- Chi-square

### Approach
- Importing the dataset and doing usual exploratory data analysis steps like checking the structure & characteristics of the dataset.
  - Definition of problem (as per given problem statement with additional views).
  - Observations on shape of data, data types of all the attributes, conversion of categorical attributes to 'category' (If required) , missing value detection, statistical summary.
  - Univariate Analysis (distribution plots of all the continuous variable(s) barplots/countplots of all the categorical variables).
  - Bivariate Analysis (Relationships between important variables such as workday and count, season and count, weather and count.
- Trying to establish a relation between the dependent and independent variable (Dependent “Count” & Independent: Workingday, Weather, Season etc).
- Selecting an appropriate test to check whether:
  - Working Day has effect on number of electric cycles rented.
  - No. of cycles rented similar or different in different seasons.
  - No. of cycles rented similar or different in different weather.
  - Weather is dependent on season (check between 2 predictor variable).
- Set up Null Hypothesis (H0).
- State the alternate hypothesis (H1).
- Checking assumptions of the test (Normality, Equal Variance). We can check it using Histogram, Q-Q plot or statistical methods like levene’s test, Shapiro-wilk test (optional).
- We will continue doing the analysis even if some assumptions fail (levene’s test or Shapiro-wilk test) but double check using visual analysis and report wherever necessary.
- Setting a significance level (alpha).
- Calculating test statistics.
- Deciding whether to accept or reject null hypothesis.
- Inferencing from the analysis.
- Providing insights and recommendations to Yulu to improve their revenue.
