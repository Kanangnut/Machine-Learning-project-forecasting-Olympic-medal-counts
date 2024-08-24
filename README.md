
### End-to-End Machine Learning Project Summary: Predicting Olympic Medal Counts

#### Project Objective:
The goal of this project is to predict a country's future Olympic medal count using machine learning techniques based on historical data.

#### Data Source:
120 years of Olympic history: athletes and results:<br>https://www.kaggle.com/datasets/heesoo37/120-years-of-olympic-history-athletes-and-results

#### Data Exploration:
The dataset includes various columns such as country code, year, number of athletes, average athlete age, and past medal counts. Key columns used for prediction are **athletes** and **previous medals**, both of which show a strong correlation with the current medal count.

#### Data Cleaning:
The dataset was cleaned by removing rows with missing values, particularly in the **previous medals** column. The data was split into training and test sets, with recent Olympic years (2012 and 2016) serving as the test set.

#### Model Training:
A **Linear Regression** model was trained using **athletes** and **previous medals** as predictors. After training, predictions were made, and adjustments were applied to ensure that all predictions were non-negative and rounded to whole numbers, as fractional and negative medal counts are not realistic.

#### Model Evaluation:
The performance of the model was evaluated using the **Mean Absolute Error (MAE)**, which was found to be approximately 3.3 medals. While the model performed well for countries with historically high medal counts (e.g., USA, Australia), it struggled with countries that have fewer athletes or lower medal counts, such as India. Errors were calculated on a country-by-country basis, and a histogram was used to visualize the distribution of error ratios.

#### Key Findings:
- **Predictive Accuracy**: The model predicted well for larger, historically successful Olympic nations, but had higher error rates for countries with fewer participants.
- **Error Ratio**: The error ratio, which compares prediction errors to actual medals earned, revealed that predictions were within 50% of actual medals for many countries. However, some countries exhibited higher deviations.
  
#### Potential Improvements:
- **Incorporating More Features**: Adding more predictors like age or events could improve predictions.
- **Exploring Other Models**: Experimenting with advanced machine learning algorithms like random forests or neural networks may enhance accuracy.
- **Finer-Grained Data**: Building models based on individual athlete data rather than aggregate country data could offer more precise predictions.

