# CapstoneProject

This project applies machine learning techniques to a sports analytics problem: predicting whether an NBA player will score 20 or more points in a game (“Good Game”).

Using game-by-game player data, rolling 3-game averages are engineered to capture recent performance trends while preventing data leakage. The project builds a complete ML pipeline, including data cleaning, feature engineering, stratified train/validation/test splitting, and model evaluation.

Multiple models are implemented and compared, including:

Decision Tree Classifier
Naïve Bayes
Multi-Layer Perceptron (MLP) Neural Network

Given the class imbalance in the target variable, the project emphasizes evaluation beyond accuracy, using precision, recall, and F1-score, along with class weighting techniques. It also critically examines model assumptions, particularly the limitations of Naïve Bayes with correlated numerical features.

This project demonstrates how machine learning can be applied to sports performance prediction while showcasing key concepts such as feature engineering for time-series data, model comparison, and handling imbalanced datasets.
