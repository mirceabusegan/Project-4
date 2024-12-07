# Project-4
Machine Learning Trading Algorithm

Objective: 
Predict the direction of the next move in the price of a stock. 

Sources: The data is retrived from Yahoo finance. 

The algorithm uses the RandomForestClasifier made of decision trees. The output of the algorithm is a binary choice: 1 for UP and 0 for Down. 
The model takes as input the stock prices for the past 25 years. That represents over 6,000 rows. 
In the initial phase, the model is trained on the first 5700 rows and tested on the last 300 rows. 
The predictors used are: Open, High, Low, Close prices and the Volume. 

Optimization
In the next phase, the model is optimized by adding other predictors:
         SMA 5 days, SMA 50 days, SMA 200 days,  
         RSI,
         Trend 5, 50, 200 days
         Close ratio 5, 50, 200 days
In this phase I used the Backtesting method: 
        the model is trained on the first 2500 rows - coresponding to 10 years of data
        the model is tested on the next 250 rows (the 11th year)
        the 11th year is added to the testing dataset and model is trained on the first 11 years
        the model is tested on the 12 year and son on. 

Results 
The algorithm was  run on a selection of 10 stocks, and the results were compiled into an external file, 'accuracy.csv',
wich reflects the accuracy of the initial model, the accuracy of the optimezed model and the predictions for the next trading day. 
