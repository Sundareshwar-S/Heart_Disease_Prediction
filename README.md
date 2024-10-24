# Heart Disease Prediction Dataset

## Overview

This dataset is designed for predicting the likelihood of heart disease based on a set of clinical and demographic features. It can be used for training machine learning models to determine risk factors and patterns related to heart disease. Each row in the dataset represents an individual, and the dataset includes a mix of numerical and categorical data points, which reflect various health metrics and conditions.

## File Details

- **File name:** `Heart_Disease_Prediction.csv`
- **File format:** CSV (Comma-Separated Values)
- **Encoding:** UTF-8
- **Number of rows (samples):** Varies based on dataset, typically representing the number of individuals
- **Number of columns (features):** 14

## Columns Description (Detailed)

1. **Age**: 
   - Represents the age of the individual in years.
   
2. **Sex**: 
   - The gender of the individual, commonly encoded as:
     - 0: Female
     - 1: Male

3. **Chest Pain Type**:
   - Describes the type of chest pain the individual is experiencing.

4. **Resting Blood Pressure (mm Hg)**:
   - The individual's blood pressure measured in millimeters of mercury when at rest.

5. **Cholesterol (mg/dL)**:
   - The cholesterol level in milligrams per deciliter of blood.

6. **Fasting Blood Sugar (> 120 mg/dL)**:
   - Binary variable indicating whether the individual's fasting blood sugar is greater than 120 mg/dL.

7. **Resting ECG Results**:
   - Results from the resting electrocardiogram.

8. **Max Heart Rate**:
   - The maximum heart rate achieved during exercise testing.

9. **Exercise-Induced Angina**:
   - Binary variable indicating whether the individual experienced angina (chest pain) during exercise.

10. **ST Depression (mm)**:
    - The amount of ST depression observed in the ECG during peak exercise.

11. **Slope of the ST Segment**:
    - Describes the slope of the ST segment during peak exercise.

12. **Number of Major Vessels (0-3)**:
    - The number of major coronary arteries colored by fluoroscopy.

13. **Thalassemia**:
    - A blood disorder that affects hemoglobin and red blood cells.

14. **Target**:
    - The presence or absence of heart disease:
      - 0: No heart disease
      - 1: Heart disease present

## Algorithms Used

In this project, several algorithms were applied to predict heart disease based on various clinical and demographic features. Each algorithm was chosen for its unique properties and potential to capture important patterns in the dataset. Below is a summary of the algorithms used:

### 1. Artificial Neural Network (ANN) using Random Seeds
   - A neural network was trained using various random seeds to enhance model robustness.
   - The network consists of multiple layers (input, hidden, and output) with activation functions applied at each node.
   - Random seeds help ensure reproducibility and improve model generalization.
   - The ANN attempts to capture complex, non-linear relationships between input features and the likelihood of heart disease.

### 2. Naive Bayes
   - The Naive Bayes classifier was applied, assuming that the features are conditionally independent given the target.
   - It’s a simple but effective algorithm for probabilistic classification, particularly useful when dealing with categorical data.
   - This method calculates the probability of each class and selects the most likely outcome based on the input features.

### 3. Heart Disease Prediction using LightGBM
   - LightGBM (Light Gradient Boosting Machine) is a fast, distributed, high-performance gradient-boosting framework.
   - It was used to create a highly accurate and efficient predictive models for heart disease.
   - The LightGBM model iteratively adds decision trees to correct the errors of the previous trees, focusing on the hardest-to-predict samples.

### 4. Logistic Regression with Hyperparameter Tuning
   - A standard Logistic Regression model was applied to the dataset to predict the binary target (heart disease presence).
   - Hyperparameter tuning was done using **GridSearchCV** to optimize:
     - `C`: The inverse of regularization strength.
     - `penalty`: Regularization type (L1 or L2).
   - This model is particularly useful for its interpretability and its ability to estimate probabilities for each class.

Each of these algorithms contributed uniquely to understanding the dataset, providing both probabilistic insights and complex decision boundaries for heart disease prediction.
