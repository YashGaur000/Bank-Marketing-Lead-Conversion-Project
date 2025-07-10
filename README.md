## Project Summary

In this project, I worked on predicting whether a customer would subscribe to a term deposit after a marketing campaign. What worked well was the overall flow cleaning the data, handling missing values, and using one-hot encoding to prepare the dataset. I used Random Forest as the main model, which gave good results.

Initially, without SMOTE, the model gave a high accuracy of 90.3%, but the recall for the minority class ("yes") was only 0.36, and the F1 score was 0.47. This showed the model was biased toward predicting "no". After applying SMOTE to fix the class imbalance, the accuracy slightly dropped to 89.9%, which was expected, because the model was now also focusing on the minority class. However, both recall (0.37) and F1 score (0.46) for the "yes" class improved slightly, meaning the model became better at catching actual positive cases.

I chose to apply SMOTE before hyperparameter tuning, since tuning wouldn’t help much if the data was already biased. The goal was to improve detection of potential leads, and SMOTE helped move in that direction.

What didn’t work as well was mode-based imputation for the 'poutcome' column, since over 80% of values were "unknown". So instead, I kept "unknown" as a separate category or replaced it with "missing" for better interpretability. Also, while the model did okay overall, it still struggled with false positives.

If I had more time, I’d try hyperparameter tuning, test models like XGBoost, and do some feature engineering like grouping ages or merging similar job roles. I’d also explore feature importance to see what really influences customer decisions

## Setup & Running Instructions

1. (Recommended) Create and activate a virtual environment:

   py -3.11.9 -m venv venv then 
   run ".\venv/bin/activate"

2. Install required packages:

   pip install -r requirements.txt

3. Launch Jupyter Notebook:

   jupyter notebook

4. Open `Analysis.ipynb` and run the cells in order.
