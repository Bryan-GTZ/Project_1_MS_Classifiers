# Project 1: Machine Learning Classifiers
## By: Bryan Gutierrez and Zach Lanter

## Introduction  
This project explores and compares the linear machine learning classifiers we went over in class on and tested them on the **UCI Adult Income dataset**. Our goal is to predict whether an individual’s income is over \$50K per year based on demographic and employment attributes.  



| Attribute          | Attribute        |
|--------------------|------------------|
| Age                | Occupation       |
| Workclass          | Relationship     |
| Education          | Race             |
| Marital Status     | Sex              |
| Capital Gain        | Hours Per Week   |
| Native Country     |    Capital Loss              |


We used both **custom algorithms** from *Machine Learning with PyTorch and Scikit-Learn* (Raschka, Liu, & Mirjalili, 2022) and **scikit-learn**, so we can see the differences in performance, convergence, and generalization. The purpose of the project is to learn the classic algorithms and there optimized counterparts.  



## Objectives  
- **Start from scratch**: Perceptron, Adaline, Linear SVM, and Logistic Regression
- **Train with scikit-learn**: Perceptron, Adaline ( `SGDRegressor`), Logistic Regression, and Linear SVM.  
- **Preprocessing**: Handle missing values, encode categorical features, and standardize numeric features using `ColumnTransformer` and `Pipeline`.  
- **Model selection**: Apply `GridSearchCV` for hyperparameter tuning with cross-validation.
- **Evaluation**: Compare training/test performance, visualize decision boundaries, and analyze validation predictions.


## Parts of the notebook 
- **Part 1 (Preprocessing)**
  -  Data: (`Project_adult.csv`) and (`project_validation_inputs.csv`)
      -  Steps:
      -  Fixed the missing values
          -  Numerical were filled with the median
          -  categorical was filled with the mode
      -  What was applied
          - We used Standa


  
 ## Reflection and Conceptual Questions:
 
  - Why is feature scaling important for gradient-based algorithms?
  - Explain the difference between batch gradient descent and stochastic gradient descent.
  - Why does scikit-learn Perceptron and Adline algorithms outperform book code?
  - Compare the decision boundaries of logistic regression and SVM.
  - What is the role of regularization in preventing overfitting?
  - Vary the C values of the scikit-learn LogisticRegression and linear SVC models with  [0.01, 1.0, 100.0] .

## Deliverables  
- **Jupyter Notebook**: Code, preprocessing steps, model training, evaluation, and plots (`Group_16_sklearn_perceptron_adaline.ipynb`).  
- **CSV Files**: Predicted outputs on the validation dataset for each model (`Group_16_Model_PredictedOutputs.csv`).  
- **Recording/Slides**: Summarize of report, results, and reflections.


## Location of Repository
- **Documents** -> Reflection_and_Conceptual_Questions.md
- **Notebook** -> Group_16_sklearn_perceptron_adaline.ipynb
- **ML_outputs** -> output prediction files for adaline, preceptron, SVM, and Logistic Regression
