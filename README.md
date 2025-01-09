# **La Liga Match Predictor**

---

This project predicts the outcomes of La Liga 24/25 matches based on data from the past five seasons (this specific code is for matchdays 19 and 20). Built using JupyterLab and Python, it uses machine learning with scikit-learn's `RandomForestClassifier` to train a predictive model.

---

## **Overview**
1. **Scraping**: Match data is scraped from [Fbref](https://fbref.com/en/comps/12/La-Liga-Stats) using `requests`, `BeautifulSoup`, and `pandas`.
2. **Preprocessing**: : The raw data is cleaned, transformed, and enhanced with rolling averages and other features for training.
3. **Training**: A `RandomForestClassifier` is trained on historical match data to learn patterns and predict outcomes.
4. **Prediction**: The trained model predicts outcomes for Matchdays 19 and 20 of the 24/25 season, using features such as team form, venue, and other factors.

---

## **Future Plans**
This is a **WORK IN PROGRESS**. While this project currently focuses on Matchdays 19 and 20, I plan to expand predictions for the remainder of the 24/25 season and so on. Planned improvements and features include:

### Upcoming Predictions
- **Remainder of the Season**: As new matches are played, I plan to update the dataset and generate predictions for future matchdays.

### Enhancements
As the project grows, I plan to implement the following enhancements to improve the predictions and functionality:

- **Model Improvements**: 
  - Incorporating new features, such as:
    - **Expected Statistics**: Scraping and integrating expected goals (xG), assists (xA), etc., to help predictions.
    - **Player Statistics**: Adding player data to capture individual impacts on match outcomes.
    - **Score Predictions**: Extending the model to predict match scores rather than just match outcomes.
- **Visualization**: 
  - Developing visual tools to better interpret and display results, including:
    - Dashboards showing match probabilities, predicted outcomes, and predicted scores.
    - Charts highlighting trends in team and player performance across the season.
- **Automation**: 
  - Streamlining the workflow to automatically:
    - Scrape new match data after each gameweek.
    - Update rolling averages and other features for predictions.
    - Retrain the model periodically as new data becomes available.

---

## **Documentation of Updates**
Progress and changes will be documented in an `UPDATES.md` file in the repository. This file will include:
- **Prediction Updates**: Matchdays and outcomes added to the model.
- **Feature Enhancements**: New features or improvements made to the training process.

---

## **Note to Readers**
This project is a **WORK IN PROGRESS**, and the current model has been designed and validated for Matchdays 19 and 20. As the 24/25 season progresses, I will continue to make predictions, improve the model, and share updates here.

> **Stay Tuned!** Check the `UPDATES.md` file for the latest developments, including new predictions and features.
