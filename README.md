# NBA Player Performance Prediction

**Overview**

This project predicts whether an NBA player will have a **"Good Game"** using machine learning models trained on rolling 3-game performance averages.

**Problem Statement**

The goal is to identify strong player performances based on recent trends, simulating real-world sports analytics applications such as scouting and performance forecasting.

**Dataset**

- Game-by-game NBA player statistics
- Multiple rows per player
- Rolling 3-game averages used for feature engineering

**Feature Engineering**

- Created rolling averages (last 3 games) for: points, minutes, shooting percentage, assists, rebounds, etc.
- Used .shift(1) to prevent data leakage
- Dropped early games without sufficient history

**Models Used**

- Decision Tree (class-balanced)
- Naïve Bayes
- MLP (Neural Network)

**Results (Validation Set)**

| Model         | Accuracy | Precision | Recall | F1 Score |
|--------------|----------|----------|--------|---------|
| Decision Tree | 0.80     | 0.44     | **0.78**   | 0.56    |
| Naïve Bayes   | 0.81     | 0.45     | 0.75   | **0.56**  |
| MLP           | 0.86     | **0.62**     | 0.44   | 0.52    |

**Final Model Insights**

- Decision Tree captured the most "Good Games" (high recall)
- Naïve Bayes provided the best balance between precision and recall (F1 score)
- MLP produced the most precise predictions but missed more positives
- Naïve Bayes offered the strongest overall tradeoff for this imbalanced classification problem

**Final Model Choice**

The Naïve Bayes model was selected as the final model because it achieved the strongest balance between precision and recall, as reflected in its F1 score. While the Decision Tree achieved higher recall and the MLP achieved higher precision, Naïve Bayes provided the most balanced performance for predicting "Good Game" outcomes

This choice is appropriate given the class imbalance in the dataset. Accuracy alone can be misleading when most games belong to the "Not Good Game" class. The F1 score is more informative because it considers both false positives and false negatives.

**Confusion Matrix Insights**

- Naïve Bayes successfully identified the majority of "Good Game" instances
- Some FPs indicate over-prediction of strong performances
- Tradeoff between recall and precision is clearly demonstrated

**Key Takeaway**

This project demonstrates how different machine learning models handle imbalanced classification problems and highlights the importance of selecting evaluation metrics aligned with the problem objective

**Tools & Technologies**

- Python
- pandas
- scikit-learn
- Google Colab

**Author**

DeJanee McAtee

**Presentation Link**

[McAteeCapstoneProject](https://canva.link/mcateecapstonefinalproject)
