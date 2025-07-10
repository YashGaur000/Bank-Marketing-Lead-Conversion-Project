Project Summary

This project aimed to predict whether a customer would subscribe to a term deposit based on a marketing campaign dataset. Initially, I tried a basic Random Forest model after cleaning and one-hot encoding the data. It gave decent accuracy approx. 90%, but I noticed a strong class imbalance most people in the dataset said "no", which biased the model.

To improve performance, I used SMOTE to balance the training data. After applying SMOTE, the overall accuracy dropped slightly, but the recall and F1 score for the minority class (those who said "yes") improved. Since the goal is to identify more potential leads, this trade-off was actually a good thing.

Some features like 'pdays' and 'default' didn’t seem to contribute much and might be dropped in future versions. Also, after one-hot encoding, the number of columns increased a lot, which I handled using drop_first=True.

If I had more time, I would try tuning the model hyperparameters, testing ensemble methods like XGBoost, and exploring more meaningful feature engineering. I’d also like to experiment with calibration to get better probability scores instead of just hard classifications.

Overall, this was a great hands-on project to understand EDA, preprocessing, and model evaluation, especially with imbalanced data.