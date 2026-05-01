# 🚨 Fraud Detection On Financial Data: SMOTE vs Baseline Comparative Analysis

A comprehensive Machine Learning project analyzing the impact of **class imbalance handling using SMOTE** on fraud detection performance using:

* Logistic Regression
* Random Forest
* SMOTE Oversampling
* Comparative Evaluation Metrics
* Imbalanced Learning Analysis

---

# 📌 Project Objective

Credit card fraud datasets are highly imbalanced, where fraud transactions represent only a tiny fraction of all transactions.

This project explores:

✅ How Machine Learning models behave on imbalanced data
✅ How SMOTE affects different algorithms
✅ Why Recall and Precision tradeoffs matter in fraud detection
✅ Why SMOTE may help some models more than others
✅ Why model selection itself is critical in imbalanced learning

---

# 🧠 Models Evaluated

| Model               | SMOTE Applied |
| ------------------- | ------------- |
| Logistic Regression | ❌             |
| Logistic Regression | ✅             |
| Random Forest       | ❌             |
| Random Forest       | ✅             |

---

# 📊 Dataset Information

Dataset used:

📁 `creditcard.csv`

Dataset characteristics:

| Property           | Value   |
| ------------------ | ------- |
| Total Transactions | 284,807 |
| Fraud Transactions | 492     |
| Fraud Percentage   | ~0.17%  |
| Features           | 30      |
| Target Column      | `Class` |

Class labels:

| Class | Meaning   |
| ----- | --------- |
| 0     | Non-Fraud |
| 1     | Fraud     |

---

# ⚙️ Technologies Used

| Category             | Tools                    |
| -------------------- | ------------------------ |
| Programming Language | Python                   |
| Data Processing      | Pandas                   |
| Visualization        | Matplotlib, Seaborn      |
| Machine Learning     | Scikit-learn             |
| Imbalanced Learning  | imbalanced-learn (SMOTE) |
| Version Control      | Git & GitHub             |

---

# 🧩 Project Structure

```text
smote-vs-baseline-fraud-detection/
│
├── notebooks/
│   ├── 01_baseline_without_smote.ipynb
│   ├── 02_logistic_regression_with_smote.ipynb
│   ├── 03_random_forest_without_smote.ipynb
│   ├── 04_random_forest_with_smote.ipynb
│   └── 05_final_comparative_analysis.ipynb
│
├── Data/
│   └── creditcard.csv (ignored from Git)
│
├── requirements.txt
├── .gitignore
└── README.md
```

---

# 🔥 What is SMOTE?

SMOTE stands for:

# Synthetic Minority Oversampling Technique

It handles class imbalance by generating synthetic samples for the minority class.

Instead of duplicating fraud transactions, SMOTE creates new artificial fraud points between existing fraud samples.

Mathematical formulation:

```text
x_new = x_i + λ × (x_neighbor - x_i)
```

Where:

| Symbol       | Meaning                      |
| ------------ | ---------------------------- |
| `x_i`        | Existing fraud sample        |
| `x_neighbor` | Nearby fraud sample          |
| `λ`          | Random value between 0 and 1 |
| `x_new`      | Synthetic fraud sample       |

---

# 📈 Final Model Comparison

| Metric          | Logistic Regression Without SMOTE | Logistic Regression With SMOTE | Random Forest Without SMOTE | Random Forest With SMOTE |
| --------------- | --------------------------------: | -----------------------------: | --------------------------: | -----------------------: |
| Accuracy        |                            99.91% |                         97.42% |                      99.96% |                   99.95% |
| Precision       |                            82.89% |                          5.80% |                      94.12% |                   84.54% |
| Recall          |                            64.29% |                         91.84% |                      81.63% |                   83.67% |
| F1 Score        |                            72.41% |                         10.92% |                      87.43% |                   84.10% |
| False Positives |                                13 |                           1461 |                           5 |                       15 |
| False Negatives |                                35 |                              8 |                          18 |                       16 |

---

# 🧠 Key Findings

## ✅ Logistic Regression + SMOTE

* Massive Recall improvement
* Fraud detection became highly sensitive
* Lowest missed frauds
* Very high false positives

### Recall Improvement

```text
64.29% → 91.84%
```

### False Negatives Reduced

```text
35 → 8
```

---

## 🌲 Random Forest Without SMOTE

Best overall balanced model.

### Achieved:

✅ Highest Precision
✅ Highest F1 Score
✅ Very low False Positives
✅ Strong fraud detection capability

---

## ⚠️ Why SMOTE Did Not Improve Random Forest Much

Random Forest already handled imbalance effectively.

SMOTE slightly improved Recall but also:

* increased false positives
* reduced Precision
* reduced overall balance

This demonstrates an important ML insight:

# 🚨 SMOTE is model-dependent.

---

# 🏆 Best Model by Objective

| Objective              | Best Model                     |
| ---------------------- | ------------------------------ |
| Highest Accuracy       | Random Forest Without SMOTE    |
| Highest Precision      | Random Forest Without SMOTE    |
| Highest Recall         | Logistic Regression With SMOTE |
| Highest F1 Score       | Random Forest Without SMOTE    |
| Lowest False Positives | Random Forest Without SMOTE    |
| Lowest False Negatives | Logistic Regression With SMOTE |

---

# 📚 Core Machine Learning Concepts Covered

This project demonstrates:

* Imbalanced Learning
* Binary Classification
* Oversampling Techniques
* Precision vs Recall Tradeoff
* Fraud Detection Systems
* Ensemble Learning
* Decision Trees
* Logistic Regression
* Model Evaluation
* Confusion Matrix Analysis
* Precision-Recall Tradeoff
* False Positive vs False Negative Cost Analysis

---

# 🚀 Final Conclusion

This project demonstrates that:

# Better model selection can sometimes outperform imbalance handling techniques.

Key learning:

* SMOTE significantly improved Logistic Regression Recall
* Random Forest naturally handled imbalance better
* Fraud detection systems require balancing:

  * fraud detection sensitivity
  * false alarm rate
  * customer experience
  * operational cost

The project highlights the real-world challenge of:

# Catching more frauds while minimizing false alarms.

---


# ⭐ If You Found This Project Useful

Consider giving the repository a ⭐ on GitHub.
