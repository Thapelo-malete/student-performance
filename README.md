# Student Performance Prediction

This repository contains code and data for predicting how well students will perform based on their study habits, past scores, sleep, extracurricular activities, and practice history.

## Folder Structure
```
student-performance/
    ├── data/
    │   └── student_performance.csv     - Dataset
    ├── student_performance.ipynb       - notebook
    ├── requirements.txt                - dependencies (pandas, jupyter, scikit-learn)
    └── README.md                       - read (this file)
```

## Installations and Setup
### Prerequisites
- Python (Language)
- Jupyter Notebook
- Pandas, NumPy (Data manipulation)
- Scikit-learn (for machine learning)

### Installation
1.  **Clone the repository**  
```bash
git clone https://github.com/Thapelo-malete/student-performance.git
cd student-performance
```
2. **Setup a virtual environment**
```bash
python -m venv .venv
source .venv/Scripts/activate # .venv\Scripts\activate on windows cmd

```
3. **Install Dependencies**
```bash
pip install -r requirements.txt
```

## Data
### Data Source
The dataset used in this project is the [Student Performance Dataset](https://www.kaggle.com/datasets/nikhil7280/student-performance-multiple-linear-regression) from [Kaggle](https://www.kaggle.com).

## Description
The dataset has 6 variables (5 independent features and 1 dependent target) and 10 000 observation
| Feature                                 | Type      | Description                                                        |
|-----------------------------------------|-----------|--------------------------------------------------------------------|
| `hours_studied`                         | Numeric   | Hours of study per day.                                            |
| `previous_scores`                       | Numeric   | Average score from previous exams.                                 |
| `extracurricular_activities`            | Categorical → One‑Hot Encoded | Whether the student participates in extracurriculars. |
| `sleep_hours`                           | Numeric   | Hours of sleep per night.                                          |
| `sample_question_papers_practiced`      | Numeric   | Number of past papers attempted.                                   |
| `performance_index` _(target)_          | Numeric   | Predicted exam score.                                              |
## Model Evaluation
```python
from sklearn.metrics import r2_score


print(f"R² : {r2_score(y_test, predictions)}")
```
```
Output:
R² : 0.9888721485893653
```

R<sup>2</sup> Score is 0.9889. This suggest that 98.89% of the variation in performance index is explained by the model— excellent fit.