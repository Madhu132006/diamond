# Diamondpricemodel

# This is our Website link:
https://diamond-9f69.onrender.com

---

# 💎 Diamond Price Prediction using Random Forest

This project is a machine learning application that predicts the price of a diamond based on its physical and qualitative characteristics such as cut, color, clarity, and size. It uses a **Random Forest Regressor** trained on a dataset of diamonds.

---

## 📁 Files

* `test1.csv`: The dataset used to train the model.
* `diamond_price_predictor.py`: The main script for training the model and interacting with users to make predictions.

---

## 📦 Dependencies

Make sure you have the following Python packages installed:

```bash
pip install pandas numpy scikit-learn
```

---

## 📊 Dataset

The CSV file should include the following columns:

* `carat`: Weight of the diamond.
* `cut`: Quality of the cut (Fair, Good, Very Good, Premium, Ideal).
* `color`: Diamond color grading from D (best) to J (worst).
* `clarity`: A measurement of how clear the diamond is (I1, SI2, SI1, VS2, VS1, VVS2, VVS1).
* `depth`: Total depth percentage.
* `table`: Width of the top of the diamond.
* `x`, `y`, `z`: Physical dimensions in mm.
* `price`: Target variable — price of the diamond in USD.

> ⚠️ The first column in the CSV is assumed to be an index and will be dropped during processing.

---

## ⚙️ How It Works

1. **Data Preprocessing**

   * Drops the index column.
   * Encodes categorical values (`cut`, `color`, `clarity`) using `LabelEncoder`.

2. **Model Training**

   * Splits the dataset into training and test sets.
   * Trains a `RandomForestRegressor` model.

3. **Evaluation**

   * Outputs R² Score and Mean Squared Error on test data.

4. **Prediction**

   * Prompts the user to input diamond characteristics.
   * Predicts price using the trained model.
   * Handles unseen categories using fallback logic.

---

## 🚀 Running the Script

Run the script in your terminal:

```bash
python diamond_price_predictor.py
```

You will be prompted to enter values for:

* Carat
* Cut
* Color
* Clarity
* Depth
* Table
* x (length in mm)
* y (width in mm)
* z (depth in mm)

Example:

```
Carat: 0.9
Cut: Ideal
Color: G
Clarity: VS2
Depth (%): 61.5
Table (%): 56
x length (mm): 6.2
y width (mm): 6.3
z depth (mm): 3.8
```

Output:

```
Predicted Diamond Price: $5,689.42
```

---

## 🧠 Model Specs

* **Algorithm**: Random Forest Regressor
* **Hyperparameters**:

  * `n_estimators=200`
  * `max_depth=10`
* **Encoding**: Label Encoding with unseen category handling

---

## 🛠 Improvements You Can Make

* Replace Label Encoding with One-Hot Encoding or Ordinal Encoding.
* Optimize model using GridSearchCV.
* Save trained model with `joblib` or `pickle`.
* Build a GUI using `tkinter` or a web app using `Flask` or `Streamlit`.

---

## 📜 License

MIT License – Feel free to use and modify.

---
