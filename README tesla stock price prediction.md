# README for Tesla Stock Price prediction

**Summary**

I predicted a section of the Tesla Stock Price chart using LSTM. The dataset contains the daily stock price of Tesla from the 2010s, where the model is trained on the first 80% of data. There are two predictions- one made using Linear regression and the other using Long-Short term memory (LSTM).

**Business case**

The stock market can be described as dynamic and non-linear. Factors linked to politics, physchology and economics can all be responsible for this. So using machine learning to predict the stock price is important as there are many unexpected events that could happen to alter the stock price. By properly analysing the data, automated trading strategies can be executed when necessary

**Methodology**

Linear Regression
1) Convert the dates column from an object data type to a date
2) Plot the stock price- both the whole dataset and the first 20 rows. I noticed here that the price wasn't recorded in linear intervals, so I made sure that I used the day number on the x axis later on
3) Reshape the dataset into a 2D array
4) Make predictions with linear regression model and calculate R2 Score

LSTM
1) Split data into training (first 80%) and testing data
2) Scale the training data to reduce feature dominance
3) Extract 60 data points, and reshape X_train to add another dimension for these input features
4) Build Sequential model with a dropout on every layer (4) to reduce overfitting
5) Repeat steps 2-3 with the test data
6) Make predictions
7) Inverse transform predictions to original values for plotting
8) Plot the predicited stock price against the actual stock price (for testing data)

**Skills**

Data preprocessing, data manipulation/visualisation, mathematical/statistical analysis, pandas, matplotlib, sklearn, Linear Regression, LSTM

**Results**

As expected, linear regression did not produce an accurate result. It is a basic model which just captures the overall trend of the dataset. The R2 score of 86% was misleading as the peaks and troughs of the graph weren't counter for

Using LSTM, a more complex algorithm, meant that the general trend of the test data was predicted accurately. A possibilty as to why the predicted curve is of a lower price is because there is a sudden spike at the start of the period. The model will have been trained on many spikes previously, any may think that it has already reached the maximum price

**Further Improvements**

I could have used cross-validation techniques when training the data, and incorporate more performance metrics
