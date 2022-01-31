

# Hedge Fund Analysis

This Jupyter Notebook evaluates performance of four hedge fund investment options

---

## Technologies

Project uses:

[Pandas](https://pandas.pydata.org/)

[Numpy](https://numpy.org/)

[PatLib](https://docs.python.org/3/library/pathlib.html)

[matplotlib](https://matplotlib.org/)

---

## Installation Guide

Run this program in Jupyter notebook and have a folder destination for CSV imports.



---

## Usage

Utilize Jupyter Labs to interact with the software program

!["Jupyter Labs Example"](https://miro.medium.com/max/955/1*mXGu0MeYgnUkyR9ybVlQpg.png)

**Key example code for creating and plotting Sharpe Ratios**
```
  # Calculate the covariance using a 60-day rolling window 
covarience_tiger = whale_daily_returns['TIGER GLOBAL MANAGEMENT LLC'].rolling(window=60).cov(whale_daily_returns['S&P 500'])
covarience_tiger.tail()

# Calculate the beta based on the 60-day rolling covariance compared to the market (S&P 500)
tiger_beta = covarience_tiger / variance_market
tiger_beta.tail()

# Calculate the average of the 60-day rolling beta
tiger_rolling_avg_beta = tiger_beta.rolling(window=60).mean()

# Plot the rolling beta 
# Include a title parameter and adjust the figure size
tiger_rolling_avg_beta.plot(figsize=(10,7), title="Tiger Global 60-Day Rolling Average Beta")
```

---

## Contributors

Hugo Kostelni

---

## License

Open Source
