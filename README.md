# AlgoTradingIsAwesome

# Libaries Used
 Imports
import pandas as pd
import numpy as np
from pathlib import Path
import hvplot.pandas
import matplotlib.pyplot as plt
from sklearn import svm
from sklearn.preprocessing import StandardScaler
from pandas.tseries.offsets import DateOffset
from sklearn.metrics import classification_report

# Analysis of baseline modle
  The Baseline model perfomed average on the original data with a 55% accuracy score using the SVC() model
  ![image](https://user-images.githubusercontent.com/106267420/189503450-af0dc0b1-39c3-42d2-8c2d-22704f343ab4.png)
  
  Using a new classifer LinearRegression and running the original data with the new modle achieved an accuracy score 
  of 52% 
 ![image](https://user-images.githubusercontent.com/106267420/189503546-8cb7b5f8-ca73-46f0-a8d0-35be1546cc68.png)

  Using the SVC classifer, even though it had a better accuracy score it did not test well on the sell signal almost being not exsistant.
  On the other hand using the LogisticRegression classifier tested much better on the sell data and having better recall information 
  the SVC Classifer may see under or overfit needing to implement oversimplified or undersimplified classifier to see if it makes a difference.
  With that beeing said even though the SVC() had a slightly better accuracy score its clear to me that the LogisticRegression modle performed much better
  overall on the data it self. 


# Analysis of Re-tooled Algo
  I left the trading Short and Long window the same but updated the trading period from 3 months to 36 months
  and changed the time frame of the algo to recongnize price movement from 1 hour to 24 hours giving it a whole day to 
  learn on price moving data instead of every hour which is too volatile or not volatile enough for me. The SVC Classifer did
  not test at all on the testing data it was giving but came the same accuracy score of 55% while at this time the LogisticRegression
  Classifer performed better at 56% and tested much better than the SVC() on the selling signals for data it's never seen before.
  updating the Window's had a small affect on the Algo increasing compared to the actual returns but not much of a differnce the biggies
  change came from the start and end data for the Algo to train & test on improving the Algo significantly 
  
  
  # Final Analysis
  I would recommend using the LogisticRegression modle with the new parameters as it shows to outperform the baseline
  modle as well showing that is outperformed  the actual returns of the Emerging Markets returns over time. It is clear 
  to see that the more data the LogisticRegression modle has to train on the better it does compared to the actual returns as you
  can see from the difference in the graphs below. If you would have allowed the algo to trade and stopped it before January 2021
  you would have outpeformed the Emerging Markets index for 36 months and could re-tool from their if you have a long strategy 
  but a short strategy does not seem sufficent in outperforming the Actual returns unless some oversampling is done and backtest for 
  analysis to see what short startegy would be sufficent. 
  
  ![image](https://user-images.githubusercontent.com/106267420/189504004-574bc6e7-020e-4a13-a452-9c0ddacbc0cc.png)


# Original Algo before Tweaks
![image](https://user-images.githubusercontent.com/106267420/189502821-635f123f-6211-42cb-9b9c-fe9b5ad961e1.png)

# New and Approved Algo after Tweaks
![image](https://user-images.githubusercontent.com/106267420/189504020-38ded29d-ffd9-4444-b0a1-d9f6f6dac32e.png)


