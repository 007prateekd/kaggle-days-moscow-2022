# Kaggle-Days-Moscow
This is my submission for the KaggleDays x Z by HP Championship Meetup in Moscow for which about 300 participants are selected.
The competition link (along with all the data and problem statement) can be found [here](https://www.kaggle.com/c/now-you-are-playing-with-power/overview).

# Approach
I performed the following steps:
- Since there were missing values in each column, I decided to use Iterative Imputation essentially creating a model to 
predict missing values for each column separately using some metric like mean (for numerical columns) and mode (for categorical columns).
- Selecting an appropriate supervised model was important. After experimenting with XGBoost and LighGBM, the latter gave better results in both MAE and efficiency.
- After training the model with custom defined hyperparameters, the MAE on the validation data was 0.83 and on the test data was 2.21.

# Conclusion
I achieved a rank of 44 / 130 teams with this approach which you can see below:
<img src='Rank.png'>
