# Project Report

## Preprocessing

- profile_data: customer demographics
- portfolio_data: offer characteristics
- transcript_data: event logs
- unwrapped the values of 'channels' column in portfolio_datawhich are originally lists
- unwrapped 'value' column in the transcript_data
- encoded categorical column 'event'
- dropped rows with '118' as the value for the 'age' column.
- The 3 datasets are merged by 'id' column in profile_data and 'person' column in transcript_data, then merged to portfolio data by 'id'(offer id) column.
- Then following datasets were created for checking the popularity of the offers, the effectiveness of different channels, and the target customers. Which are best_offer, best_channel, and target_customer respectively. targte_customer DataFrame will be used to predict which customers should be targted for the offers.
- After dropping the null values in the merged DataFrame, there are 14825 customers. 15,100 BOGO offer were completed, 16,970 offers were completed, and 0 informational offers were completed.

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



