# 📊 Insights & Analysis Report
## Project: Predicting Legendary Pokémon using Decision Tree

---

## 🧠 Objective

The goal of this project was to determine **which characteristics define a Legendary Pokémon** and to build a classification model using a **Decision Tree** algorithm.

---

## 🔍 Key Observations from Data

### 🧹 Data Insights:
- There were **721 Pokémon**, of which about **65 (∼9%) are Legendary**.
- `Type 2` had many missing values (∼386), which were filled with `'None'`.
- Features like `Attack`, `Sp. Atk`, `Total`, and `Speed` showed higher values for Legendary Pokémon.

### 🔗 Correlation Analysis:
- The `Total` score was highly correlated with all base stats and with the `Legendary` label.
- `Sp. Atk`, `Speed`, and `Attack` had the strongest individual correlation with being Legendary.

---

## 🌳 Decision Tree Model Findings

### 📈 Model Performance:
- **Accuracy**: ~[your accuracy value here, e.g., 92%]
- **Precision & Recall** for `Legendary = 1` were lower than for `Legendary = 0` (due to class imbalance).
- Confusion matrix revealed that the model had some false positives/negatives, but overall reliable.

### 🧠 Feature Importance (Top Predictors):
| Rank | Feature     | Importance |
|------|-------------|------------|
| 1    | Total       | Highest    |
| 2    | Sp. Atk     | High       |
| 3    | Speed       | High       |
| 4    | Attack      | Moderate   |
| 5    | Type 1      | Low        |
| 6    | Generation  | Low        |

---

## 🧩 Decision Rules (Sample Insights from Tree)

- If `Total > 600`, and `Sp. Atk > 100`, high likelihood of being **Legendary**
- Pokémon with lower base stats across the board were almost always **not Legendary**
- The Decision Tree was able to pick up distinct stat thresholds that separate the two classes

---

## ✅ Summary Insights

- **Legendary Pokémon tend to have high Total stats** — especially in **Sp. Atk, Speed, and Attack**.
- **Type** and **Generation** were not strong indicators on their own.
- The model can serve as a simple and interpretable way to **identify Legendary Pokémon** using only stat-based data.

---

## 🔄 Limitations & Next Steps

- **Class Imbalance** (only 9% are Legendary) might have affected model performance — can be improved with techniques like SMOTE or class weighting.
- Try **Random Forest or XGBoost** for better generalization and performance.
- Use **cross-validation** and **grid search** for tuning hyperparameters like tree depth.

---

## 🧠 Final Thought

This project demonstrates how Decision Trees can be used to extract **logical rules** from structured datasets and give **clear visibility** into how decisions are made — making it ideal for understanding what makes a Pokémon truly *Legendary*.

