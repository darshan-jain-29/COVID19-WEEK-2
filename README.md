# COVID19-WEEK-2-Global-Forecasting
Using Machine learning models to predict cases and fatalties.

Link to the competition: https://www.kaggle.com/c/covid19-global-forecasting-week-2
Link to my solution on Kaggle: https://www.kaggle.com/darshanjain29/working-solution-progressing-on-leaderboard/

COVID19 is a serious outbreak of Corona Virus and now it is spreading at a very huge rate across the globe. In that situation Kaggle came up with the dataset of predicting the cases.

About the dataset:

It contains 2 file - train.csv and test.csv
These files holds data for 173 countries and daywise confirmed cases and fatalties of total 70 days. Also, these details are specified province region wise.

Now, firstly I started with feature engineering. 

1. There are null values for Province_Region. So, I have replaced them by the Country names itself in both train and test dataframes.

2. The Date feature is of type Object. So, first that is converted into DateTime type and then various values are extracted from it like Day, Week, Month, Quarter, Year and the original Date feature is droppped.

3. Now, I had to replace all the object type data into numericals. For this I have used 2 methods. Firstly, I have used LabelEncoder by sklearn and then I have used OneHotEncoding because later was giving me better score. Followed by this, I dropped the columns that are ob type object so that the dataframes now have only numerical type features.

Training models on dataframes and generating root mean squared lograthmic error:

After splitting the data into train and test, I have used the following models:

1. SVM

2.Decision Tree Regressor

3. Random Forest Regressor

4. Adaboost regressor

5. Voting Regressor with Random Forest, Bagging and Decision Tree Regressor

6. Bagging Regressor

Out of all I got the best score with 6th Bagging Regressor. Then I have tried to improve the score by doing hyperparameter tuning. But it didn't help. 

Thanks for reading :-)
