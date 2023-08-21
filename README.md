**NOTE:** The interactive plots in this script will not show up on GitHub. To view them, please visit: https://nbviewer.org/github/JaredBalbona/Predicting-Age-Related-Decline/blob/main/identifying-age-related-conditions.ipynb 
----------------------------------

# Identifying Age-Related Conditions using Machine Learning #

This code was written as part of an entry in the following Machine Learning competition: 

> _They say age is just a number but a whole host of health issues come with aging. From heart disease and dementia to hearing loss and arthritis, aging is a risk factor for numerous diseases and complications. The growing field of bioinformatics includes research into interventions that can help slow and reverse biological aging and prevent major age-related ailments. Data science could have a role to play in developing new methods to solve problems with diverse data, even if the number of samples is small._

> _Currently, models like XGBoost and random forest are used to predict medical conditions yet the models' performance is not good enough. Dealing with critical problems where lives are on the line, models need to make correct predictions reliably and consistently between different cases._

> _Founded in 2015, competition host InVitro Cell Research, LLC (ICR) is a privately funded company focused on regenerative and preventive personalized medicine. Their offices and labs in the greater New York City area offer state-of-the-art research space. InVitro Cell Research's Scientists are what set them apart, helping guide and defining their mission of researching how to repair aging people fast._

> _In this competition, you’ll work with measurements of health characteristic data to solve critical problems in bioinformatics. Based on minimal training, you’ll create a model to predict if a person has any of three medical conditions, with an aim to improve on existing methods._

> _You could help advance the growing field of bioinformatics and explore new methods to solve complex problems with diverse data._

> _The goal of this competition is to predict if a person has any of three medical conditions. You are being asked to predict if the person has one or more of any of the three medical conditions (Class 1), or none of the three medical conditions (Class 0). You will create a model trained on measurements of health characteristics._

> _To determine if someone has these medical conditions requires a long and intrusive process to collect information from patients. With predictive models, we can shorten this process and keep patient details private by collecting key characteristics relative to the conditions, then encoding these characteristics._

> _Your work will help researchers discover the relationship between measurements of certain characteristics and potential patient conditions._

## Code Overview
The code is organized as follows:

1. **Import Data**: Read the CSV files containing training, testing, and additional data.

2. **Exploratory Data Analysis**:
- Display basic statistics of the training data.
- Identify non-numeric columns and display their statistics.
- Identify missing values in columns and display their counts and percentages.
- Visualize class distribution using a pie chart.

3. **Data Preprocessing and Feature Engineering**:
- Apply various transformations to numerical features to reduce skewness and kurtosis.
- Remove outliers from the data.
- Perform KNN imputation to fill missing values.
- Scale the data using StandardScaler.

4. **Model Training with Optuna**:
- Define hyperparameters for XGBoost, LightGBM, and CatBoost models.
- Optimize weights for the ensemble of these models using Optuna.

5. **Bagging Models**:
- Train multiple bagged models using resampling.
- Calculate predictions for the test set using the bagged models.

6. **Submission Generation**:
- Generate a submission CSV file containing predictions.

## Results
The trained ensemble model was within the top 5% of submissions in the Kaggle competition, demonstrating the effectiveness of the approach in identifying age-related conditions.
