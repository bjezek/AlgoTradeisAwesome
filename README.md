# AlgoTradeisAwesome

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



# Original Algo before Tweaks
![image](https://user-images.githubusercontent.com/106267420/189502821-635f123f-6211-42cb-9b9c-fe9b5ad961e1.png)

# New and Approved Algo after Tweaks
![Uploading image.png…]()

