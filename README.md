# breast-cancer-prediction


# 🧠 Breast Cancer Classification using Machine Learning

## 📌 Project Overview

This project builds a machine learning model to classify breast tumors as **benign** or **malignant** using diagnostic features. Early and accurate detection of breast cancer is critical for effective treatment, and this model demonstrates how data-driven approaches can support medical decision-making.

---

## 🎯 Objective

To develop and evaluate a classification model that predicts whether a tumor is:

* **Benign (0)** – Non-cancerous
* **Malignant (1)** – Cancerous

---

## 📊 Dataset

* Source: Breast Cancer dataset (commonly available in `sklearn`)
* Features include:

  * Radius
  * Texture
  * Perimeter
  * Area
  * Smoothness
  * Compactness
* Total samples: 569
* Target classes: Binary (Benign / Malignant)

---

## ⚙️ Technologies Used

* Python
* Jupyter Notebook
* NumPy & Pandas
* Scikit-learn
* Matplotlib / Seaborn

---

## 🔍 Methodology

1. Data Loading and Exploration
2. Data Preprocessing (feature scaling, train-test split)
3. Model Training using classification algorithms:

   * Logistic Regression
   * Random Forest
   * XGBoost
4. Model Evaluation using:

   * Accuracy
   * Precision
   * Recall
   * F1-score

---

## 📈 Results

* Achieved approximately **97% accuracy**
* Strong performance in identifying both benign and malignant cases
* Balanced precision and recall across classes

---

## 🧪 Sample Output

Classification Report:

```
Precision    Recall    F1-score
Benign (0):     0.97      0.98      0.98
Malignant (1):  0.96      0.92      0.94
```

---

## 🚀 How to Run the Project

1. Clone the repository:

```
git clone https://github.com/your-username/breast-cancer-classification.git
```

2. Navigate to the project folder:

```
cd breast-cancer-classification
```

3. Open the notebook:

```
jupyter notebook
```

4. Run all cells to reproduce results

---

## 📁 Project Structure

```
breast-cancer-classification/
│── BreastCancerProject.ipynb
│── README.md
```

---

## 💡 Key Learnings

* Applied supervised machine learning techniques to a real-world dataset
* Gained experience in model evaluation and performance metrics
* Understood the importance of data preprocessing in ML pipelines

---

## 🔮 Future Improvements

* Hyperparameter tuning for better performance
* Deploying the model using a web app (Flask/Streamlit)
* Adding more advanced models and cross-validation

---

## 👤 Author

Sandra Paul

---

## ⭐ If you found this project useful, feel free to star the repository!
