Titanic Survival Prediction 🚢⚓
📌 Project Overview

The sinking of the RMS Titanic in 1912 is one of the most infamous shipwrecks in history. Using real passenger data, this project predicts the likelihood of survival based on features such as age, gender, ticket class, and family members onboard.

This project demonstrates the end-to-end machine learning workflow — from data preprocessing to model training, evaluation, and potential improvements. It is a great starting point for anyone exploring classification problems in data science.

📂 Dataset

Source: DatascienceDojo Titanic Dataset

Size: 891 rows × 12 columns

Target Variable: Survived (0 = Did not survive, 1 = Survived)

Key Features

Pclass → Ticket class (1st, 2nd, 3rd)

Sex → Gender (male/female)

Age → Age of passenger

SibSp → Number of siblings/spouses aboard

Parch → Number of parents/children aboard

Fare → Ticket price

Embarked → Port of embarkation (C = Cherbourg, Q = Queenstown, S = Southampton)

🛠️ Workflow
1. Data Loading

The dataset is imported directly from GitHub.

2. Data Preprocessing

Handling Missing Values:

Filled missing Embarked values with the most frequent category.

Replaced missing Age and Fare values with median values.

Encoding Categorical Features:

Converted Sex into numerical values (0 = Male, 1 = Female).

One-hot encoded Embarked (dropping the first column to avoid dummy variable trap).

3. Feature Selection

Selected relevant features:
['Pclass', 'Sex', 'Age', 'SibSp', 'Parch', 'Fare', 'Embarked']

4. Train-Test Split

Data split into 80% training and 20% validation sets.

5. Model Training

Random Forest Classifier was chosen for its robustness and high accuracy in classification problems.

The model was trained on the processed dataset.

6. Model Evaluation

Predictions were made on the validation set.

Accuracy was calculated using accuracy_score from scikit-learn.

(Add your accuracy result here, e.g., ~82-85% based on typical runs)

📊 Results

The Random Forest model successfully predicted survival outcomes with strong accuracy.

Key insights:

Gender (Sex) played a critical role (females had higher survival chances).

Higher class passengers (Pclass = 1) were more likely to survive.

Younger passengers had better survival rates.

🚀 Technologies Used

Python

Pandas & NumPy → Data preprocessing & manipulation

Scikit-learn → Machine learning algorithms, model evaluation

🔮 Future Improvements

Implement other models (Logistic Regression, SVM, Gradient Boosting, XGBoost).

Perform hyperparameter tuning for Random Forest.

Add feature engineering (e.g., family size, passenger title extraction).

Include data visualization for insights into survival patterns.

Deploy the model as a web app using Flask or Streamlit.

📌 How to Run

Clone the repository

git clone https://github.com/your-username/titanic-survival-prediction.git
cd titanic-survival-prediction


Install dependencies

pip install -r requirements.txt


Run the notebook

jupyter notebook "Titanic Survival Prediction.ipynb"


✨ This project highlights how machine learning can uncover survival patterns from historical tragedies while also serving as a beginner-friendly ML classification example.
