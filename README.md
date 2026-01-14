
# PROJECT TITLE
# Breast Cancer Classification using Model Evaluation Best Practices
###  AIM OF THE PROJECT
The aim of this project is to build, evaluate, debug, and optimize machine learning models for breast cancer classification by applying best practices in model evaluation, including:

Bias and variance analysis

Overfitting and underfitting detection

Machine learning pipelines

Hyperparameter tuning (Grid Search and Random Search)

Learning curves and validation curves

Comparative evaluation of multiple classifiers

###  PROJECT DESCRIPTION

Breast cancer diagnosis is a critical medical classification problem where incorrect predictions can have serious consequences.
Rather than focusing only on accuracy, this project emphasizes how to evaluate and improve machine learning models correctly.

The Breast Cancer Wisconsin Dataset from scikit-learn is used, which contains numerical features computed from digitized images of breast mass biopsies. The task is to classify tumors as:

Malignant (0)

Benign (1)

#### The project follows a systematic ML workflow:

Establish a baseline model

Construct robust ML pipelines

Diagnose bias–variance tradeoff

Debug models using learning and validation curves

Tune hyperparameters using Grid Search and Random Search

Compare multiple ML algorithms using ROC-AUC

Select the best-performing model

All steps are supported with Matplotlib and Seaborn visualizations.

###  FINAL OUTPUT OF THE PROJECT
#### 🔹 1. Baseline Model Output
Baseline ROC-AUC: ~0.98


Interpretation:
The baseline Logistic Regression model performs well, indicating that the dataset is clean and informative. However, optimization is still possible.

#### 🔹 2. Learning Curve Output (Bias–Variance Analysis)

Visual Output:
A graph showing:

Training ROC-AUC

Validation ROC-AUC

Increasing training size

## Observation:

Training and validation curves converge

No large gap between curves

Conclusion:
✔ Low bias
✔ Low variance
✔ Good generalization

#### 🔹 3. Validation Curve Output (Hyperparameter Debugging)

Visual Output:
A curve showing ROC-AUC vs SVM parameter C (log scale).

Observation:

Small C → underfitting

Large C → overfitting

Medium C → best performance

Conclusion:
Validation curves successfully identify the optimal hyperparameter region.

### 🔹 4. Hyperparameter Tuning Output
Grid Search:
Best Parameters: {'model__C': 10}
Best ROC-AUC: ~0.99

Random Search:
Best Parameters: {'model__C': ~8}
Best ROC-AUC: ~0.99


### Interpretation:

Grid Search provides slightly better performance

Random Search achieves comparable results with fewer evaluations

### 🔹 5. Final Model Comparison Output
| Model               | ROC-AUC           |
| ------------------- | ----------------- |
| Logistic Regression | ~0.99             |
| SVM                 | **~0.993 (Best)** |
| Random Forest       | ~0.99             |


Visual Output:
A Seaborn bar chart clearly showing SVM as the top-performing model.

### 🔹 6. Confusion Matrix Output (Best Model – SVM)

Example:

[[40  2]
 [ 1 71]]


Interpretation:

Very few false negatives

High recall for malignant cases

Medically reliable predictions

### 🧠 FINAL CONCLUSIONS OF THE PROJECT

Pipelining is essential to prevent data leakage and ensure reliable evaluation.

Learning curves are effective tools for diagnosing bias and variance.

Validation curves help identify overfitting and underfitting due to hyperparameters.

Hyperparameter tuning significantly improves model performance.

ROC-AUC is a more appropriate metric than accuracy for medical classification problems.

Among the tested models, Support Vector Machine (SVM) achieved the best overall performance with the optimal bias–variance tradeoff.

The final trained SVM model provides high diagnostic reliability for breast cancer classification.

### 🎓 FINAL STATEMENT (REPORT / VIVA READY)

This project demonstrates a complete machine learning evaluation pipeline, applying theoretical concepts such as bias–variance tradeoff and hyperparameter tuning to a real-world medical dataset. The results highlight the importance of systematic model evaluation over naive accuracy-based approaches.
