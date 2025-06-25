# 🧠 Pokémon Legendary Classification using Decision Tree

This project aims to build a classification model to predict whether a Pokémon is **Legendary** or not based on its attributes like stats, types, and generation. The model is trained using a **Decision Tree Classifier**.

---

## 📌 Problem Statement

In the Pokémon universe, some Pokémon are classified as "Legendary" based on various game-related factors. However, no specific criteria clearly define a Legendary Pokémon.  
Using the dataset of 721 Pokémon, our goal is to identify the key variables that distinguish Legendary Pokémon from others and train a Decision Tree classifier to predict this status.

---

## 📁 Dataset Description

| Column       | Description                                                                 |
|--------------|-----------------------------------------------------------------------------|
| `#`          | ID of the Pokémon                                                           |
| `Name`       | Name of the Pokémon                                                         |
| `Type 1`     | Primary type (e.g., Fire, Water, etc.)                                      |
| `Type 2`     | Secondary type if any                                                       |
| `Total`      | Sum of all base stats                                                       |
| `HP`         | Hit Points – health level                                                   |
| `Attack`     | Attack power                                                                |
| `Defense`    | Defensive capability                                                        |
| `Sp. Atk`    | Special attack power                                                        |
| `Sp. Def`    | Special defensive capability                                                |
| `Speed`      | Speed of the Pokémon                                                        |
| `Generation` | The generation the Pokémon was introduced in                               |
| `Legendary`  | Boolean flag indicating if the Pokémon is Legendary (`True` or `False`)     |

---

## 🔧 Data Preprocessing

- Dropped columns: `#`, `Name`
- Filled null values in `Type 2` with `"None"`
- Stripped whitespaces and removed placeholder values (e.g., `?`, `Unknown`)
- Label Encoded categorical variables: `Type 1`, `Type 2`, `Generation`
- Converted `Legendary` to binary (0 = Not Legendary, 1 = Legendary)
- Outlier detection using boxplots (visual inspection)
- Correlation matrix used to examine multicollinearity

---

## 📊 Modeling: Decision Tree Classifier

- Used `sklearn.tree.DecisionTreeClassifier`
- Train/Test Split: 70/30
- Evaluation Metrics:
  - **Accuracy**
  - **Classification Report (Precision, Recall, F1-score)**
  - **Confusion Matrix**
- Optional:
  - Visualized the tree structure using `plot_tree()`
  - Analyzed feature importances

---

## 📈 Results

- The model was successfully able to classify Pokémon into Legendary and Non-Legendary.
- Features like `Total`, `Sp. Atk`, `Attack`, and `Speed` had significant influence.
- The Decision Tree provided understandable rules for identifying Legendary Pokémon.

---

## ✅ Conclusion

The Decision Tree classifier provided a clear understanding of what characteristics typically define a Legendary Pokémon. This project demonstrates the effectiveness of decision trees in classification problems involving structured datasets.

---

## 📌 Tools & Libraries Used

- Python
- Pandas, NumPy
- Scikit-learn (DecisionTreeClassifier, LabelEncoder, train_test_split)
- Seaborn, Matplotlib

---

## 📂 Project Structure

Pokemon-Decision-Tree/
│
├── Pokemon.csv # Dataset file
├── Pokemon_DecisionTree.ipynb # Jupyter Notebook with all code & analysis
├── README.md # Project overview (this file)


---

## 🧑‍💻 Author

RamKumar N  
_Data Analytics & Machine Learning Enthusiast_

---

## 📚 Acknowledgments

- Dataset from: [Kaggle Pokémon Dataset](https://www.kaggle.com/abcsds/pokemon)
- Inspired by Pokémon fans and data science learners worldwide.

