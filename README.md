# PREDICTIVE-ANALYSIS-USING-MACHINE-LEARNING

### DESCRIPTION

This process builds a Linear Regression model to predict the growth_rate based on key features in the dataset. Below is a step-by-step explanation of the workflow:

### 1) Load & Explore Data
Goal: Load the dataset, understand its structure, and check basic statistics.
Import essential libraries: pandas, numpy, seaborn, matplotlib.
Read the dataset (surv_variants.csv).
Display dataset information (df.info()) and preview the first few rows (df.head()).
This step helps us understand the number of records, column types, and whether any data preprocessing is needed.

### 2) Data Preprocessing (Handling Missing Values & Feature Selection)
Goal: Clean and prepare the dataset for training.
Check for missing values (df.isnull().sum()).
Drop rows with missing values in the target variable (growth_rate).
Select relevant numerical features for regression (num_seqs, duration, mortality_rate, total_cases, total_deaths).
Extract features (X) and target (y) for training the model.
Ensures that we have clean data with the most relevant features.

### 3) Train-Test Split & Scaling
Goal: Split data into training & testing sets and standardize numerical features.
Train-test split:
80% of the data is used for training.
20% of the data is reserved for testing.
Feature Scaling:
Standardization (StandardScaler) is applied to normalize features.
This helps improve model performance by bringing all features to the same scale.

### 4) Train Regression Model
Goal: Train a Linear Regression Model to predict growth rate.
A Linear Regression model is initialized and trained using model.fit(X_train_scaled, y_train).
The model learns relationships between the input features and the growth rate.
Predictions are made on the test set using model.predict(X_test_scaled).

### 5) Model Evaluation
Goal: Measure how well the model predicts growth rate.
Use different metrics to evaluate performance:
Mean Absolute Error (MAE): Average absolute difference between actual and predicted values.
Mean Squared Error (MSE): Penalizes larger errors more than MAE.
Root Mean Squared Error (RMSE): More interpretable than MSE (in the same units as growth_rate).
R² Score: Measures how well the model explains the variance in the data (closer to 1 = better fit).

### 6) Visualizing Results
Goal: Compare actual vs. predicted values with a scatter plot.
A scatter plot is generated to visually assess how well predictions match the actual values.
Helps identify patterns, outliers, and potential issues with the model.

### OUTPUT

![Image](https://github.com/user-attachments/assets/015d9000-998d-467d-b9a5-6b80d25cc391)
