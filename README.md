# Predict future sales
Predicting monthly sales using time series forecasting with tensorflow.
<img width="567" alt="image" src="https://user-images.githubusercontent.com/22840423/188516787-38ffeaed-ee45-4168-9221-42a65ca7ee0f.png">


The data used to train the models came from [this Kaggle competition](https://www.kaggle.com/competitions/competitive-data-science-predict-future-sales/overview). It was selected one time series to train the models, the largest one.

The reference for this implementation was the [tensorflow tutorial on time series forecasting](https://www.tensorflow.org/tutorials/structured_data/time_series).

The models trained were:
1. Linear
2. Dense
3. Convolutional
4. RNN
5. Autoregressive

<img width="583" alt="image" src="https://user-images.githubusercontent.com/22840423/188516753-eaf8c4cb-ec61-4a59-a2c3-81b9d648dc37.png">

The convolutional model achieved the best performance, with MAE of 0.54 on (normalized) test data. Apparently the increase on models complexity did not benefit on solving this problem.
The window used for training had 50 days of input and generated expected total sales after 30 days. 

<img width="1035" alt="image" src="https://user-images.githubusercontent.com/22840423/188516908-8a4fde25-6196-4e40-b540-c96da700835d.png">

The final model seemed to exacerbate the predicted data. That is likely because the first 2 years, the main part of the test data, had greater sales than the last year. Using more data, and a wider window could enhance the model performance.
