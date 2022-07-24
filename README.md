# Deep-Learning-Models-for-Prognostics
In this repository, I implemented some models for remaining useful lifetime (RUL) prediction  by different deep learning and machine learning models.

Based on my own experiment, using windowing for the raw data can improve the performance of convolutional neural network (CNN), Long short-term memory (LSTM), and Temporal convolutional network (TCN). For this reason, for these networks, we used windowing with size = 50 and stride = 1 for data before feeding it to the networks. While for simple neural networks and linear regression, we just feed raw data after some basic preprocessing such as normalization.

Experiments have been done with N-CMAPSS (DS002). For reproducing the result, you need to download the data first.

We used 3 units (16, 18, 20) for training and 3 units (11, 14, 15) for testing. Moreover, we just used X_s and W features.

Results show that TCN did the best among other networks.

| Models | RMSE  | 
| :------------ |:---------------:| 
| Linear Regression      | 10.68 | 
| ANN      | 7.84 | 
| LSTM      | 6.12 | 
| CNN      | 5.99        |
| TCN | 5.26        |
