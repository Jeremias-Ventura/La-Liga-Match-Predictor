# **Project Updates - La Liga Match Predictor**

## **Latest Update - 02/06/2025**

### **Overview**
This update improves the model’s accuracy from **67% to 77%** by incorporating **recent form and past encounters** more effectively. The previous model didn’t properly account for these factors, leading to skewed predictions. Now, the model better evaluates team performance based on historical matchups and form trends.

Predictions for **Matchday 22 and Matchday 23** have been generated and are stored in `04_prediction/`.

---

## **Key Improvements (Stored in `03_training/`)**  

### **Feature Engineering Adjustments**  
The previous model struggled with **inconsistent predictions** due to an **overreliance on raw stats** without properly factoring in **recent form and head-to-head results**. The updated model now includes:  

- **Past Encounters Score**: Now evaluates **both teams’ historical performances against each other**, rather than applying a flat score. This ensures that head-to-head records contribute meaningfully to predictions.  
- **Recent Form Score**: Adjusted to **factor in both win percentage and goal difference** over the last six matches, giving a more accurate picture of a team's momentum.  
- **Key Stats Score**: Previously, a team could receive **maximum points for dominating a single stat** (e.g., goals scored). Now, scoring is more balanced, preventing **statistical outliers from skewing predictions**.  
- **Unpredictability Factor**: Retained as a way to introduce **a small degree of randomness**, accounting for the natural volatility of football.  

### **Model Refinements**  
The model continues using **RandomForestClassifier**, but several refinements were made to **improve probability calibration and decision-making**:  

- **CalibratedClassifierCV Implementation**: This was added to refine probability outputs, ensuring the model’s confidence in predictions is **more realistic** rather than extreme.  
- **Feature Contribution Balance**: The model is now structured to prevent any **one feature from dominating predictions**, ensuring **more well-rounded decision-making**.  
- **Hyperparameter Adjustments**: A **more controlled depth** and **minimum sample requirements** were set to improve **generalization and avoid overfitting**.  

These refinements **significantly boosted accuracy**, improving from an initial **67% to 77%** during model validation. The updated training process is stored in `03_training/`, where the trained model (`match_predictor.pkl`) and predictor features (`predictors.pkl`) are saved for use in match predictions.  

### **Matchday 22 Predictions - 60% Accuracy**
- **6/10 correct predictions** for MD22.
- Predictions stored in `04_prediction/md22_predictions_final.csv`.

This was the first test using the updated model, and the results were solid despite a few unexpected match outcomes. A 60% accuracy rate is a good step in the right direction, considering soccer is quite unpredictable.

### **Matchday 23 Predictions**
- Predictions for MD23 have been generated using the updated model.
- Results are stored in `04_prediction/md23_predictions_final.csv`.
- Accuracy will be evaluated once matches are completed.

---

## **Next Steps**
- **Evaluate MD23 Accuracy** once results are available.
- **Further refine feature weighting** for better prediction reliability.
- **Implement additional predictive factors**, including:
  - **Home Advantage Factor** once it’s properly integrated.
  - **Expected Goals (xG) and Player Stats** to improve predictive accuracy.
  - **Automate data updates** after each gameweek.

---

## **Conclusion**
The **accuracy improvement to 77%** shows that integrating **recent form and past encounters** made a significant difference. The model remains **machine learning-based**, using **RandomForestClassifier with probability calibration** to refine predictions.

Both **Matchday 22 and Matchday 23 predictions** are stored in `04_prediction/`, with future improvements planned.