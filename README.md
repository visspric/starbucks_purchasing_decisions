# Project Report

## Preprocessing
- profile_data: customer demographics
- portfolio_data: offer characteristics
- transcript_data: event logs
- unwrapped the values of 'channels' column in portfolio_data which are originally lists
- unwrapped 'value' column in the transcript_data
- encoded categorical column 'event'
- dropped rows with '118' as the value for the 'age' column.
- The 3 datasets are merged by 'id' column in profile_data and 'person' column in transcript_data, then merged to portfolio data by 'id'(offer id) column.
- Then following datasets were created for checking the popularity of the offers, the effectiveness of different channels, and the target customers. Which are best_offer, best_channel, and target_customer respectively. targte_customer DataFrame will be used to predict which customers should be targted for the offers.
- 
- After dropping the null values in the merged DataFrame, there are 14825 customers. 15,100 BOGO offer were completed, 16,970 discount offers were completed, and 0 informational offers were completed.

## Exploratory Visualization
- Best Channel: web & email
- <img width="508" height="139" alt="Screenshot 2026-03-08 at 15 22 08" src="https://github.com/user-attachments/assets/3c60553e-4b40-458b-9559-10d2a256b612" />
- Best Offer: discount
- <img width="469" height="110" alt="Screenshot 2026-03-08 at 15 22 37" src="https://github.com/user-attachments/assets/a9449299-e541-4fb5-bde9-629a4f200472" />
- Distribution of Age for Customers Who Completed Offers: customers who aged between 45 - 65 are more likely to complete the offer
- <img width="859" height="545" alt="image" src="https://github.com/user-attachments/assets/35d0f6ef-328a-405f-8914-118ecd4c8d4d" />
- Distribution of Income for Customers Who Completed Offers: customers who have income between 50000 - 70000 are more likely to complete the offer
- <img width="859" height="545" alt="image" src="https://github.com/user-attachments/assets/2f2d8057-0f58-4d55-9b8f-be98172dc163" />
- Gender: male customers complete more offers
- <img width="704" height="468" alt="image" src="https://github.com/user-attachments/assets/8c24711d-0a1c-42fc-8c41-db3cc3c4e8e8" />

## Regression Model
- LinearRegression
- RandomForestRegressor
- GradientBoostingRegressor
- Regression model were used to identify among 'member_days', 'income', 'age' and 'gender' which has the greatest impact on the offer completion rate.
- The result:
- <img width="259" height="419" alt="Screenshot 2026-03-08 at 22 52 04" src="https://github.com/user-attachments/assets/af9c97da-8565-4d4b-be80-23daadd92f0e" />

## Classification Model
- LogisticRegression
- RandomForestClassifier
- GradientBoostingClassifer
- Classification model were used to identify the likelihood of a specific customer compelete the offer.
- Part of the restult:
- <img width="1122" height="379" alt="Screenshot 2026-03-08 at 20 07 38" src="https://github.com/user-attachments/assets/b72541e2-0d24-4512-9453-22696fa3872b" />

# Package used for Preprocessing:
- json
- Path
- pandas
- seaborn
- plt

# Package used for Modelling:
- pandas
- Path
- LabelEncoder
- train_test_split
- StandardScaler
- LogisticRegression
- RandomForestClassifier
- GradientBoostingClassifier
- roc_auc_score
- accuracy_score
- precision_score
- recall_score
- f1_score
- LinearRegression
- GradientBoostingRegressor
- plt
- sns
- mean
- numpy
- mean_squared_error
- r2_score



