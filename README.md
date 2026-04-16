# 🧠 Breast Cancer Classification using Amazon SageMaker (End-to-End ML Pipeline)

## 📌 Project Overview

This project implements a complete **end-to-end machine learning pipeline** on the cloud using Amazon SageMaker to classify breast cancer tumors as **benign** or **malignant**.

The pipeline covers the full ML lifecycle:

* Data ingestion from Amazon S3
* Exploratory Data Analysis (EDA)
* Data preprocessing & feature engineering
* Model training using XGBoost
* Hyperparameter tuning (Bayesian Optimization)
* Model deployment as a real-time endpoint
* Model evaluation and inference
* Cloud resource cleanup

---

## 🎯 Objective

To build a scalable cloud-based ML system that predicts whether a tumor is:

* **Benign (0)** – Non-cancerous
* **Malignant (1)** – Cancerous

---

## 📊 Dataset

* **Breast Cancer Wisconsin Dataset**
* 569 samples, 30 numerical features
* Target variable:

  * `M` → Malignant (1)
  * `B` → Benign (0)

### Key Insights:

* No missing values
* Mild class imbalance:

  * Benign: 62.7%
  * Malignant: 37.3%

---

## ☁️ Technologies Used

* Python
* Amazon SageMaker
* AWS S3
* Boto3 (AWS SDK)
* Pandas & NumPy
* Scikit-learn
* Matplotlib

---

## ⚙️ ML Pipeline Architecture

1. **Data Loading**

   * Dataset retrieved from Amazon S3

2. **Exploratory Data Analysis**

   * Checked data types, distributions, and missing values
   * Visualized class distribution

3. **Data Preprocessing**

   * Dropped irrelevant `id` column
   * Encoded target variable (M → 1, B → 0)
   * Split into train (70%), validation (15%), test (15%)

4. **Data Storage**

   * Processed datasets uploaded to S3 for SageMaker training

---

## 🤖 Model Training

### Algorithm:

* **XGBoost (Binary Classification)**

### Training Setup:

* Instance type: `ml.m5.large`
* Objective: `binary:logistic`
* Evaluation metric: AUC

### Key Hyperparameters:

* max_depth = 5
* eta = 0.2
* gamma = 4
* min_child_weight = 6
* subsample = 0.7
* num_round = 100

---

## 🔍 Hyperparameter Tuning (HPO)

* Strategy: **Bayesian Optimization**
* Total jobs: 10
* Parallel jobs: 2

### Tuned Parameters:

* max_depth (3–10)
* eta (0.01–0.3)
* min_child_weight (1–10)
* subsample (0.5–1.0)
* gamma (0–5)

### Results:

* **Solo Training AUC:** 0.9927
* **Best HPO AUC:** 0.9961

✅ HPO improved model performance

---

## 🚀 Model Deployment

* Deployed best model as a **real-time SageMaker endpoint**
* Endpoint returns probability scores for predictions
* Threshold:

  * > 0.5 → Malignant
  * ≤ 0.5 → Benign

---

## 📈 Model Performance

### Accuracy:

* Training Accuracy: **97.49%**
* Validation Accuracy: **95.29%**
* Test Accuracy: **96.51%**

### Classification Report (Test Set):

```
Precision    Recall    F1-score
Benign (0):     0.97      0.98      0.98
Malignant (1):  0.96      0.92      0.94
```

### Confusion Matrix:

* True Negatives: 59
* False Positives: 1
* False Negatives: 2
* True Positives: 24

---

## 🧪 Inference

* Real-time predictions performed via SageMaker endpoint
* Supports:

  * Single sample prediction
  * Batch inference (loop-based)

---

## 🧹 Resource Cleanup

To avoid unnecessary AWS charges:

* Endpoint deleted
* Endpoint configuration removed
* Model artifacts cleaned up

---

## 📁 Project Structure

```
breast-cancer-prediction/
│── BreastCancerProject.ipynb
│── train.csv
│── validation.csv
│── test.csv
│── README.md
```

---

## 💡 Key Learnings

* Built a full ML pipeline using cloud infrastructure
* Gained hands-on experience with Amazon SageMaker APIs
* Applied hyperparameter tuning using Bayesian Optimization
* Deployed and tested a real-time ML model endpoint
* Understood cost management in cloud ML systems

---

## 🔮 Future Improvements

* Automate pipeline using SageMaker Pipelines
* Deploy via API Gateway for external access
* Add model monitoring and logging
* Optimize inference latency and cost

---

## 👤 Author

**Sandra Paul**


---


