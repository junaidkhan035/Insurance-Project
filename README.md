# Insurance Classification using Random Forest

This project demonstrates a machine learning pipeline for classifying insurance costs into high or low categories using the Random Forest classifier. The model is trained on a publicly available dataset (`insurance.csv`) that contains demographic and health-related information.

## 📁 Dataset

The dataset includes the following features:
- `age`: Age of the individual
- `sex`: Gender
- `bmi`: Body Mass Index
- `children`: Number of children covered by health insurance
- `smoker`: Smoking status
- `region`: Residential region
- `charges`: Medical insurance costs

For classification purposes, a new column `high_charges` is created:
- 1 if `charges` > median value of all charges
- 0 otherwise

## 📊 Objective

The objective is to build a binary classification model that predicts whether a person will have **high medical charges** or **low charges** based on their personal data.

## 🔧 Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn

## 🛠️ Pipeline Steps

1. **Data Preprocessing**  
   - One-hot encoding for categorical features (`sex`, `smoker`, `region`)
   - Separation of numerical features (`age`, `bmi`, `children`)

2. **Target Creation**  
   - Binary label `high_charges` based on median split of the `charges` column

3. **Pipeline Setup**  
   - ColumnTransformer for preprocessing
   - RandomForestClassifier for model training

4. **Model Training & Evaluation**  
   - Train-test split (80/20)
   - Accuracy and classification report generation

## 🧪 Evaluation Metrics

- Accuracy
- Precision
- Recall
- F1-score

## 🚀 How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/insurance-classification.git
   cd insurance-classification
