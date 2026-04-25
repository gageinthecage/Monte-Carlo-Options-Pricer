# Monte-Carlo-Options-Pricer

Two functions built to be implemented into the Monte Carlo Options Pricer. 
The first being the simple options payoff equation, taking the final price of the stock, subtracting from the initial price, and maxxing out to make sure the payoff doesn't dip below zero.

The second utilizes the Black-Scholes equation to generate a random stock path using the variables: Z=standard normal random variable, r = risk free rate, o=volatility, t = time to expire, S = starting price. This generates a fixed Geometric Brownian stock motion under fixed volatility. 

Another functioncombines the two and runs a number of simulated runs, putting each payoff into an empty list, averaging out the payoff and giving you the final average payoff from this call option.

A function that generates a random stock path following a Geometric Brownian path using the Black Scholes equation, computes the max value on a options trading using Strike Price and initial price, runs 10,000 simulations averages out the payoff on the option.

Now we apply real world data, pull strike price and closing price from yfinance. We now find annualized volatility through a basic log function, taking the log of both closes, subtracting it from the previous day and then squaring it to find realized volatility. Take the standard deviation and multiply it by the square root of the total number of days open in the market to annualize it. We can insert the historic volatility and run simulations off the same strike price using the Monte Carlo Option pricer and plot the predicted premium prices compared to the real ones in order to see accuracy between the two.

The model and market allign extremely well, the greatest divergence happening around the 200 dollar strike price which is very close to at the money of Apple's current stock (4/25/2026). Using this data we can conclude that the market places greater uncertainty than historic volatility when the strike price is close to the current price of the stock. 
