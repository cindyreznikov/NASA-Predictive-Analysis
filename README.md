# machine-learning-challenge - Analysis:

I created 2 models (SVC and Neural Networks with Keras) to examine the data that NASA collects to find hidden planets outside of our solar system.    

For the SVC model, I initially left out all of the err1 and err2 columns but my accuracy was lower than I had hoped (training was .811 and testing was .799)  Adding in all of the err_1 and err_2 columns had better results.  After I learned about RFE, I decided to use it to identify and remove some of the less desirable features.  The best training score I got was .845 and the best testing data score I got was .838.   The hyperparameter tuning worked well(using GridSearch) and gave an improved score of .88.  

The Neural Network model was cleaned and pre-procesesed.  I used 39 feature columns including the err_1 and err_2 columns.  I used the MinMaxScaler as suggested.  Increasing the hidden notes to 6 gave much better results.  This model gave an accuracy of .889 and a loss of .264

Overall, the 2 models performed about the same and either should do a good job of predicting whether new data found by NASA is a hidden planet or not.