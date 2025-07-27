# stock-prediction-using-sentiment-analysis-by-vader-and-LSTM
we have two datasets that ine is for news haedlones and the other is for stock data, from 2008 to 2016
# sentiment analysis by Vader
we have used VADE, a pre-built lexicon and rule-based, sentiment analysis to give each headline a sentiment score, Each headline got a score from -1 (very negative) to +1 (very positive)
Then we aggregated the scores for each day to capture the overall market sentiment for a given time.
 so We analyze each headline separately and then aggregate.
# stock price prediction:
Our methodology is using Long Short-Term Memory (LSTM) networks, which are
a type of recurrent neural network (RNN).
we have merged the stock dataset with sentiment scores and feed into LSTM model. inother words, We combine the sentiment scores (from VADER) with the stock price data. This gives the model both numerical trends (prices) and emotional context (news sentiment).
•	The dataset included past stock prices, LSTM was selected because it works very well for time-series data like stock prices.
•	Since we wanted to predict actual future prices, this was a regression task. 
we have trained the LSTM model with epochs of 800 and the batch size of 8, there is no overfitting durin the traingof LSTM and the results of R2 confirm this
Train R²: 0.9951390512510572
Val R²: 0.9163633247857362
To measure how well the model performed, we used standard regression evaluation metrics:
•	Mean Squared Error (MSE)
•	Root Mean Squared Error (RMSE)
•	Mean Absolute Error (MAE)
•	R² Score
the results that we have got are:
📊 MSE: 35202.5655
📉 RMSE: 187.6235
📈 MAE: 147.9095
🎯 R² Score: 0.9126
MAPE: 0.86%


