# portfolio_optimization

The main preference of this project is the paper “An online portfolio selection algorithm using clustering approaches and considering transaction costs” (2020) written by Majid Khedmati and Pejman Azin.

I discovered that this famous model has a huge drawback. 
The historical data is the closing price of stocks. 
Suppose that you must optimize your portfolio on day n to get the return on day n+1, so you want to predict the relative price of day n. 
To do that, you need to use the data from day i to day n. 
However, when do you know the closing price of day n? 
When the trading session of day n ends! 
After that, you cannot trade, so you cannot use this model to get the return on day n+1.

I improved the model. 
To predict the relative price of day n+1, I use only the data from day i to day n-1. 
Therefore, I can trade at day n to get the return at day n+1.
Of course, my pattern matching algorithm is differnt from theirs.

Additionally, my model has some other improvements. 
First, I created a stock filter by statistical techniques such as a stationary test and a heavy-tailed-distribution test for risk reduction. 
Second, I added cash to the portfolio, so if the predicted returns of all stocks are negative, the portfolio can hold full cash.

I hope this model is useful to you. Please feel free to ask if you have any questions.
