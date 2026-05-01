**Final Capstone Project Reflection**

**Reflection**  
This project focused on predicting whether an NBA player would have a “Good Game” (scoring 20 or more points) using machine learning models and recent performance data. Throughout the process, several key decisions, challenges, and learning moments shaped the final outcome. 

**Key Decisions**  
One of the most important decisions was defining the target variable using a fixed scoring threshold of 20 points. This choice made the problem easy to interpret and aligned well with common benchmarks used in basketball analysis. However, I also recognized that this approach does not account for differences in player roles (role players vs. superstars), which could be explored in future work.

Another major decision was to use rolling 3-game averages as features. This was critical because it allowed the model to capture recent player performance trends while avoiding data leakage by excluding the current game’s stats. This approach made the model more realistic and aligned with how analysts evaluate player momentum. 

I also chose to compare three different models: Decision Tree, Naïve Bayes, and an MLP neural network. This decision allowed me to evaluate tradeoffs between interpretability, simplicity, and complexity. Instead of assuming a more advanced model would perform best, I prioritized comparing results using consistent evaluation metrics. 

Finally, I selected the F1-score as the primary metric for model selection due to class imbalance. Since “Good Games” were relatively rare, accuracy alone would have been misleading. This decision ensured the evaluation focused on balancing precision and recall.

**Challenges**  
One of the biggest challenges in this project was class imbalance, with only about 16% of games labeled as “Good Games.” This made it difficult for models to correctly ID positive cases without overpredicting. To address this, I used stratified train/validation/test splits, applied class weights in the Decision Tree, and focused on metrics like recall and F1-score.  
Another challenge was handling missing and inconsistent data. The dataset included missing shooting percentages and non-numeric formats (minutes played as strings). I had to preprocess the data by converting formats and filling NaNs appropriately to ensure model compatibility.

A more conceptual challenge involved understanding the limitations of certain models. For example, Naïve Bayes assumes feature independence, but many basketball statistics (such as points, field goal attempts, and game score) are highly correlated. While the model still performed well, this required me to critically evaluate its results rather than blindly trusting performance metrics.

Additionally, balancing model performance tradeoffs was challenging. For example:

- The Decision Tree had high recall but low precision  
- The MLP had high accuracy and precision but low recall  
- Naïve Bayes provided the best balance

Choosing the “best” model required understanding the problem context, not just the highest score.

**What I Learned**  
This project reinforced several important machine learning concepts. First, I learned that feature engineering is just as important as model selection. The use of rolling averages significantly improved the model’s ability to capture meaningful patterns in the data. 

I also gained a deeper understanding of evaluation metrics, especially in imbalance datasets. Accuracy alone can be misleading, and metrics like precision, recall, and F1-score provide a more complete picture of model performance. 

Another key takeaway was that simpler models can perform just as well, or potentially better, than more complex ones. Despite its limitations, Naïve Bayes achieved the best overall balance, showing that model effectiveness depends on the problem and data, not just complexity.

Finally, I learned the importance of critical thinking in model evaluation. Rather than assuming results were correct, I analyzed why each model performed the way that it did, including understanding tradeoffs and limitations. This is especially important in real-world applications like sports analytics, where decisions depend on how predictions are used.   
**Overall Takeaway**  
This project demonstrated how machine learning can be applied to real-world sports analytics problems. While the models were not perfect, they successfully captured meaningful patterns in player performance and highlighted the importance of thoughtful feature engineering, evaluation, and model selection. 

