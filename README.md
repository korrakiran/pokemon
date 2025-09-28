# Pokémon Classification (Default vs Alternate Forms)

This project explores a Pokémon dataset to predict whether a Pokémon entry is a **default form** or an **alternate form** using **height** and **weight** as features.  
Three machine learning algorithms are compared: **Logistic Regression**, **Random Forest**, and **XGBoost**.

---

## Dataset

Dataset link: [Link](https://raw.githubusercontent.com/veekun/pokedex/master/pokedex/data/csv/pokemon.csv)

The final dataset has the following columns:

- `identifier`: Pokémon name (dropped before training)  
- `height`: Pokémon height  
- `weight`: Pokémon weight  

Rows: **1092**

---

## Models Used

1. **Logistic Regression**  
2. **Random Forest Classifier**  
3. **XGBoost Classifier**

---

## Results

| Model               | Accuracy | Notes                                                   |
|---------------------|----------|---------------------------------------------------------|
| Logistic Regression | ~87.6%   | Best overall accuracy but weak on rare alternate forms. |
| Random Forest       | ~83.1%   | Better recall on rare alternate forms, less precise.    |
| XGBoost             | ~85.8%   | Balanced performance across both classes.               |

- **Class imbalance**: Default forms (class 1) dominate, alternate forms (class 0) are rare.  
- Logistic Regression tends to ignore class 0, while RF and XGBoost catch them more often.

---

## Saving Models

All trained models are saved using **pickle**:

- `logistic_model.pkl`  
- `random_forest_model.pkl`  
- `xgboost_model.pkl`
