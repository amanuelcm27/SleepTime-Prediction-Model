# 🛌 Sleep Time Prediction Model

This is a machine learning project that predicts the sleep time you will get based on daily activity and lifestyle habits. It aims to help users improve their sleep schedule using data-driven insights.

## 📊 Project Description

The model takes in a user's daily time usage (in hours) for various activities and outputs the number of hours of sleep they will probably get.

### 📟 Features Used:

* `WorkoutTime`: Hours spent working out
* `ReadingTime`: Hours spent reading
* `PhoneTime`: Hours spent on phone
* `WorkHours`: Hours spent working
* `CaffeineIntake`: Cups of coffee or other caffeine consumed
* `RelaxationTime`: Hours spent relaxing
* `SleepTime`: Target variable — number of hours the person actually slept

## 🧠 Model Information

* **Algorithms Used:**

  * Linear Regression
  * Polynomial Regression
  * Decision Tree Regressor
  * Random Forest Regressor

* **Libraries:**

  * Python
  * pandas
  * numpy
  * scikit-learn
  * matplotlib / seaborn (for visualization)

---

## ⚙️ How to Run the Models

Once you've trained the models and saved them into the `models/` directory, you can use the provided Jupyter notebook to run predictions on new input data.

### 📁 Folder Structure (Important Files Only)

```
├── models/
│   ├── decision_tree_model.pkl
│   ├── linear_regression_model.pkl
│   ├── polynomial_regression_model.pkl
│   ├── random_forest_model.pkl
│   ├── poly_transformer.pkl
│   └── standard_scaler.pkl
├── run_models.ipynb
├── requirements.txt
├── README.md
```

### 🛠️ Setup Instructions

1. **Clone the Repository** (if not done yet):

```bash
git clone <your-repo-url>
cd <your-project-folder>
```

2. **Create a Virtual Environment (optional but recommended):**

```bash
python -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate
```

3. **Install Dependencies:**

```bash
pip install -r requirements.txt
```

4. **Run the Jupyter Notebook:**

```bash
jupyter notebook run_models.ipynb
```

> ✅ **Make sure you have Jupyter installed.** You can install it via `pip install notebook` if needed.

---

## 🧪 Example Prediction

In the notebook, you can edit the following sample input to match your own lifestyle:

```python
sample_input = {
    "WorkoutTime": [1.0],
    "ReadingTime": [0.5],
    "PhoneTime": [3.0],
    "WorkHours": [8.0],
    "CaffeineIntake": [2],
    "RelaxationTime": [1.5]
}
```

Each model will then predict how many hours of sleep you might get based on this input.

### ✅ Output Example:

```
Predicted Sleep Time (hours):
Decision Tree Model:     3.44
Linear Model:            4.18
Polynomial Model:        4.02
Random Forest Model:     3.51
```

---

## 📝 Notes

* **Linear & Polynomial Regression** use **Standard Scaler** and require scaled input.
* **Polynomial Regression** also needs transformation using the saved `PolynomialFeatures` object.
* **Decision Tree** and **Random Forest** use raw inputs as they were trained without scaling.

