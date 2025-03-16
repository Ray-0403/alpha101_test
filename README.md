Overview

This project explores over half of the alpha signals from the well-known Alpha101 paper, applied to Russell 1000 index stocks spanning 2005 to 2024 (data pulled from Bloomberg). I use ridge regression to predict the next day’s returns, updating the model in a monthly walk-forward fashion. Each trading day, the strategy ranks all stocks based on predicted returns, then buys the top 50 and sells the bottom 50, rebalancing daily with MOC (Market on Close) and MOO (Market on Open) orders to avoid overnight exposure.

Strategy & Results

Model: Ridge regression predicting next-day returns
Universe: Russell 1000 stocks (2005–2024)
Execution: Buy top 50, sell bottom 50 each day; no overnight holding
Performance Metrics: Cumulative log return, annual returns, and annual Sharpe ratios
The attached figures show that early years (2005–2010) exhibit strong performance and high Sharpe ratios. After 2016, however—shortly following the Alpha101 paper’s publication—these alphas appear to degrade significantly, with lower annual returns and Sharpe ratios. This shift suggests that once a popular factor or alpha is published, it may lose its edge over time.

<img width="905" alt="Screenshot 2025-03-16 at 11 30 56" src="https://github.com/user-attachments/assets/cf440517-d3d9-45c3-8595-9a403e1adef1" />
<img width="913" alt="Screenshot 2025-03-16 at 11 31 08" src="https://github.com/user-attachments/assets/97eec95b-f8fc-49c7-9928-338bfde776a1" />
<img width="917" alt="Screenshot 2025-03-16 at 11 31 15" src="https://github.com/user-attachments/assets/2ad21fb6-39c4-46d7-9973-e740f2bf0238" />
