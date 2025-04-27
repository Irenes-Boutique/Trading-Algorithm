# Trading-Algorithm

*Currently in-progress*

**Summary:**

Trading Algorithm Framework that automatically executes trading strategies based on code along with a separate backtester to test strategies performances.

**Project Description:**

The Purpose of this project was to figure out how the process of algorithmic trading is done. This project is broken up into 2 parts: the trading algorithm and the backtester. The trading algorithm itself is executed through Interactive Brokers Trader Work Station Python API. The example strategy uses a trading strategy composed of multiple technical indicators including MACD, Stochastic Oscillator, and the Chaikin Oscillator.

The Backtester is done through multiple functions for organization purposes. The strategy is backtested by generating buy and sell signals, 1 being buy and -1 being sell. A signal column is then returned and then the strategy is tested by buying or selling the close price when the appropriate signal appears in each row, where each row is date time index based on your trading time frame (ex: 1 min, 5 min, 1 day, etc...). The trades are then processed into pandas series and the strategy performance is evaluated and metrics are outputed like max drawdown, net PnL, number of trades, win rate, etc... Monte carlo simulations generated with Levy distributions are used to simulate how a strategy would perform in a large negative price change or market swing.

The backtester is made for general use for multiple trading strategies, not just technical indicators. In the future I would like to use this framework for other trading strategies like Pairs Trading and High Frequency Trading. **Please feel free to try the backtester and let me know of any problems. I hope you learn something from this project and it helps you with starting any beginner trading projects of your own!**

**Future Improvements:**
- factor in fees and commissions into the backtests
- implement risk management like stop losses and take profits
