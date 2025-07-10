## Project Summary

In this project, I worked on predicting whether a customer would subscribe to a term deposit after a marketing campaign. What worked well was the overall flow of the project cleaning the data, handling missing values, and using one-hot encoding to prepare the dataset. I used Random Forest as the main model, which gave good results, especially after applying SMOTE to fix the class imbalance. The recall and F1 score for the “yes” class improved, which was the main goal.

What didn’t work as well was mode-based imputation for the 'poutcome' column, since over 80% of the values were "unknown". Replacing such a large chunk of data didn’t seem helpful, so I decided to keep "unknown" as its own category and replace it with "missing" only for my convenient further analysis. Also, while the model did okay, it still struggled a bit with false positives.

If I had more time, I would explore hyperparameter tuning to boost performance, try models like XGBoost, and do some feature engineering like grouping age into bins or combining similar job types. I’d also look into model explainability to understand which features mattered the most.

## Setup & Running Instructions

1. (Recommended) Create and activate a virtual environment:

   py -3.11.9 -m venv venv then 
   run ".\venv/bin/activate"

2. Install required packages:

   pip install -r requirements.txt

3. Launch Jupyter Notebook:

   jupyter notebook

4. Open `Analysis.ipynb` and run the cells in order.