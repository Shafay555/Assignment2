Dataset:Diabetes Prediction Dataset (diabetes_prediction_dataset.csv)
Source:Kaggle – https://www.kaggle.com/datasets/iammustafatz/diabetes-prediction-dataset
Problem type: Binary classification (target column: diabetes)

Summary
This project takes the raw diabetes dataset (100,000 rows, 9 columns) and prepares it for a machine learning model. I explored the data with charts, removed 3,854 duplicate rows, and turned the hidden "No Info" values in smoking_history into real missing values. I also created 2 new features (age_group and bmi_category).
The data is split 80/20 with stratify=y and random_state=42, then preprocessed with a ColumnTransformer (median + StandardScaler for numbers, most frequent + OneHotEncoder for text). Everything is fitted on the train data only, so there is no data leakage.
Final output: X_train (76916, 23), X_test (19230, 23), y_train (76916,), y_test (19230,), with no missing values.

Files
File                               What it is 

Assignment2.ipynb                  The full notebook (Steps 0 to 7) with outputs 
diabetes_prediction_dataset.csv    The dataset 
requirements.txt                   Python libraries needed 

How to run the notebook
1. Clone or download this repository.
2. Install the libraries:

   pip install -r requirements.txt

3. Start Jupyter from inside the project folder 
   jupyter notebook Assignment2.ipynb

4. Click Kernel: Restart & Run All. It runs top to bottom without errors.
