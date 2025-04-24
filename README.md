# Titanic Dataset - Data Analysis

## Project Purpose
Predict whether passengers survived or not using the **Titanic** dataset. Steps such as data preprocessing, feature engineering, hyperparameter tuning and model optimization were taken to increase the success of the model.

## Dataset Used
The dataset contains passenger information from the **Titanic** disaster. Each passenger has a survival status (`Survived`) and various characteristics (age, gender, ticket class etc.).

**Dataset Columns**:
- `PassengerId`: Passenger ID
- `Survived`: 0 = dead, 1 = alive
- `Pclass`: Ticket class (1 = 1st class, 2 = 2nd class, 3 = 3rd class)
- `Name`: Passenger name
- `Sex`: Passenger gender
- `Age`: Passenger age
- `SibSp`: Passenger number of siblings/spouses
- `Parch`: Passenger number of parents/children
- `Ticket`: Ticket number
- `Fare`: Ticket fare
- `Cabin`: Passenger cabin
- `Embarked`: Passenger port of embarkation (C = Cherbourg, Q = Queenstown, S = Southampton)

## What was done

### 1. **Data Exploration and Preprocessing**
 **Missing Data Detection and Filling**: 
 - Missing data were filled using methods such as mean, mode and median.
 
 **New Features Added**:
- `FamilySize`: Family size (SibSp + Parch).
- `IsAlone`: 1 if the passenger is alone, 0 otherwise.

 **Numericalization of Categorical Values**:
- Categorical variables such as `Sex` and `Embarked` were converted to numerical values ​​using the **Label Encoding** method.

### 2. **Feature Selection and Model Training**
- Important features were identified using **Recursive Feature Elimination (RFE)**. The best 5 features were selected: `Pclass`, `SibSp`, `Parch`, `FamilySize`, `IsAlone`.
- **Logistic Regression** model was created and trained on training data.

### 3. **Model Optimization**
- **Hyperparameter Tuning**: The hyperparameters of the model were optimized using `GridSearchCV` and `RandomizedSearchCV`.

- **Data Scaling**: Data was standardized using **StandardScaler** to make the model work faster and more efficiently.

### 4. **Model Performance Evaluation**
- The success of the model was evaluated with metrics such as **Accuracy**, **Precision**, **Recall**, **F1-Score**.

- The classification success of the model was visualized using **Confusion Matrix**.

## Libraries Used
- **Pandas**: Data manipulation and analysis
- **Numpy**: Numerical computations
- **Scikit-learn**: Model training, hyperparameter tuning, data preprocessing
- **Matplotlib** and **Seaborn**: Data visualization
