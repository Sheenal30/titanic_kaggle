
# Titanic Survival Prediction

## Project Overview
This project aims to predict the survival of passengers on the Titanic using machine learning techniques. It is a Kaggle competition entry that achieved top 23% on the leaderboard.

## Data Source
The data is provided by Kaggle and consists of two files: `train.csv` (891 passengers) and `test.csv` (418 passengers). The dataset includes features such as passenger class, sex, age, fare, and cabin information.

## Key Steps
1. **Data Preprocessing**: 
   - Handled missing values (age, fare, embarked)
   - Created new features (family size, title, deck, etc.)
   - Engineered interaction features (sex_pclass, age_sex, etc.)
   - Performed one-hot encoding for categorical variables
   - Selected features based on correlation and importance

2. **Modeling**:
   - Compared 11 models (LR, RF, CatBoost, LightGBM, etc.)
   - Performed hyperparameter tuning for top models (LR, RF)
   - Analyzed overfitting and selected the best model (LR)
   - Created a simplified model using top features

3. **Evaluation**:
   - Used cross-validation and holdout validation
   - Analyzed overfitting with learning curves
   - Achieved 77.99% accuracy on the test set (top 23%)

4. **Submission**:
   - submission_simple.csv (accuracy 77.75%): Tuned LR with full feature set
   - submission_top_features.csv (accuracy 77.99%): Tuned LR with top 12 features based on feature importance

## Results
submission_top_features.csv placed in the top 23% of the leaderboard

## Lessons
- In small datasets, simpler models with carefully selected features outperformed complex approaches
- Feature engineering is crucial, but too many features can lead to overfitting
- Logistic Regression showed minimal overfitting and generalized well
- Complex models (Random Forest, CatBoost) were prone to overfitting on this small dataset

### Taught me that simplicity often trumps complexity, especially with limited data 😊
