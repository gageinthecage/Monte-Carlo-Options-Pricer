# Monte-Carlo-Options-Pricer

This is a beginner friendly project designed to teach me basic Python syntax and a greater understanding of numpy database, but also have real quanitative finance application.

Two functions built to be implemented into the Monte Carlo Options Pricer. 
The first being the simple options payoff equation, taking the final price of the stock, subtracting from the initial price, and maxxing out to make sure the payoff doesn't dip below zero.
The second utilizes the Black-Scholes equation to generate a random stock path using the variables: Z=standard normal random variable, r = risk free rate, o=volatility, t = time to expire, S = starting price. This generates a fixed Geometric Brownian stock motion under fixed volatility. 

The final function combines the two and runs a number of simulated runs, putting each payoff into an empty list, averaging out the payoff and giving you the final average payoff from this call option.

A function that generates a random stock path following a Geometric Brownian path using the Black Scholes equation, computes the max value on a options trading using Strike Price and initial price, runs 10,000 simulations averages out the payoff on the option.
