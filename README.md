# Monte-Carlo-Options-Pricer

Two functions built to be implemented into the Monte Carlo Options Pricer. 
The first being the simple options payoff equation, taking the final price of the stock, subtracting from the initial price, and maxxing out to make sure the payoff doesn't dip below zero.
The second utilizes the Black-Scholes equation to generate a random stock path using the variables: Z=standard normal random variable, r = risk free rate, o=volatility, t = time to expire, S = starting price. This generates a fixed Geometric Brownian stock motion under fixed volatility. 

The final function combines the two and runs a number of simulated runs, putting each payoff into an empty list, averaging out the payoff and giving you the final average payoff from this call option.

A function that generates a random stock path following a Geometric Brownian path using the Black Scholes equation, computes the max value on a options trading using Strike Price and initial price, runs 10,000 simulations averages out the payoff on the option.

Now we take real world data of Apple's stock price, pull strike price and premium price, and plot the data compared to the model price of the premium using the same strike price but with the fixed historic volatility. Using January 2026 historical volatility of 20.2% as the σ input, my Monte Carlo pricer values a 30-day AAPL $260 call at $7.33. The same option trades in the market at $6.25 with an implied volatility of 43.75%; more than double the historical estimate. This discrepency shows how implied volatility is far greater than the historic estimate and that divergence of volatility skews the modelled price of premium. With a greater liklihood of crashing, the premium price drops. 
