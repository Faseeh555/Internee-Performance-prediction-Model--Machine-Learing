# Internee Performance Prediction Model (Machine Learning)

A machine learning project that predicts an intern's overall performance score using workplace performance indicators such as task completion, attendance, feedback, engagement, consistency, learning progress, and deadline management.

The project demonstrates a complete regression pipeline, including data preprocessing, model training, evaluation, feature importance analysis, visualization, prediction on new data, and model serialization.

---

## Project Overview

Organizations often evaluate interns based on multiple performance indicators instead of a single metric. This project uses those indicators to train a machine learning model capable of estimating an intern's overall performance score.

The primary objective is to assist supervisors in identifying high-performing interns as well as those who may require additional guidance or support.

---

## Problem Statement

Given historical internship data, build a regression model that predicts an intern's **Performance Score** based on measurable workplace attributes.

The model learns relationships between various performance indicators and produces a numerical performance score for unseen interns.

---

## Features Used

The model is trained using the following input features:

| Feature | Description |
|----------|-------------|
| Tasks_Assigned | Total number of tasks assigned |
| Tasks_Completed | Total number of completed tasks |
| Avg_Task_Time_Hours | Average time required to complete a task |
| Attendance_Percentage | Overall attendance percentage |
| Consistency_Score | Consistency in daily performance |
| Engagement_Score | Participation and engagement level |
| Feedback_Score | Supervisor feedback rating |
| Learning_Progress | Learning and skill improvement |
| Deadline_Misses | Number of missed deadlines |

### Target Variable

- Performance_Score

---

## Machine Learning Workflow

The project follows a complete supervised learning pipeline:

1. Import required libraries
2. Load dataset
3. Data cleaning
4. Remove duplicate records
5. Feature selection
6. Train-test split
7. Train Random Forest Regression model
8. Generate predictions
9. Evaluate model performance
10. Analyze feature importance
11. Visualize results
12. Predict performance for a new intern
13. Save the trained model

---

## Model

**Algorithm**

- Random Forest Regressor

**Configuration**

```python
RandomForestRegressor(
    n_estimators=100,
    random_state=42
)
```

Random Forest was selected because it:

- Handles nonlinear relationships effectively
- Reduces overfitting compared to a single Decision Tree
- Works well on tabular datasets
- Provides feature importance scores
- Produces stable regression predictions

---

## Model Evaluation

The trained model is evaluated using standard regression metrics:

- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- R² Score

These metrics provide different perspectives on prediction accuracy and model performance.

---

## Feature Importance

Random Forest provides built-in feature importance scores that indicate how much each feature contributed during training.

The project includes:

- Feature Importance Table
- Horizontal Bar Chart
- Pie Chart

These visualizations help interpret the model and understand which factors have the greatest influence on intern performance.

---

## Example Prediction

Example input:

```python
new_intern = {
    "Tasks_Assigned": 20,
    "Tasks_Completed": 18,
    "Avg_Task_Time_Hours": 4.5,
    "Attendance_Percentage": 94,
    "Consistency_Score": 8.8,
    "Engagement_Score": 9.0,
    "Feedback_Score": 8.7,
    "Learning_Progress": 8.9,
    "Deadline_Misses": 1
}
```

Example output:

```
Predicted Performance Score: 80.77

Prediction:
Likely to Excel
```

---

## Repository Structure

```
Internee-Performance-prediction-Model--Machine-Learning
│
├── dataset/
│   └── intern_performance_regression_dataset_v2.csv
│
├── notebook/
│   └── Internee_Performance_Prediction.ipynb
│
├── model/
│   └── random_forest_model.pkl
│
├── requirements.txt
└── README.md
```

---

## Installation

Clone the repository:

```bash
git clone https://github.com/your-username/Internee-Performance-prediction-Model--Machine-Learning.git
```

Move into the project directory:

```bash
cd Internee-Performance-prediction-Model--Machine-Learning
```

Install the required packages:

```bash
pip install -r requirements.txt
```

Run the Jupyter Notebook or Google Colab notebook.

---

## Project Dependencies

- Python 3.x
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- xgboost
- joblib

Install all dependencies using:

```bash
pip install -r requirements.txt
```

---

## Saving the Trained Model

The trained model is saved using Joblib.

```python
import joblib

joblib.dump(rf_model, "random_forest_model.pkl")
```

To load the model later:

```python
model = joblib.load("random_forest_model.pkl")
```

---

## Learning Outcomes

This project demonstrates practical experience with:

- Data preprocessing
- Regression modeling
- Random Forest Regression
- Train-test splitting
- Model evaluation
- Feature importance analysis
- Data visualization
- Predictive modeling
- Model serialization using Joblib
- End-to-end machine learning workflow

---

## Future Improvements

Possible extensions for this project include:

- Hyperparameter tuning using GridSearchCV or RandomizedSearchCV
- Cross-validation for improved model evaluation
- Comparison with XGBoost, CatBoost, and Gradient Boosting
- Feature engineering
- Web deployment using Flask or FastAPI
- Interactive dashboard using Streamlit
- Integration with a real internship management system

---

## Author

**Faseeh ur Rehman Anjum**

BS Computer Science Student  
Machine Learning Enthusiast | Python Developer | Frontend Developer

GitHub: https://github.com/Faseeh555

LinkedIn: www.linkedin.com/in/faseeh-ur-rehman-anjum-503b62306

---

## License

This project is intended for educational, research, and learning purposes.
