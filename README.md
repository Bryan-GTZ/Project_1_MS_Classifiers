# # Project 1: Machine Learning Classifiers

## Introduction  
This project explores and compares several linear machine learning classifiers on the **UCI Adult Income dataset**. The primary goal is to predict whether an individual’s income exceeds \$50K per year based on demographic and employment attributes.  

We implement both **custom algorithms** from *Machine Learning with PyTorch and Scikit-Learn* (Raschka, Liu, & Mirjalili, 2022) and **scikit-learn equivalents**, highlighting differences in performance, convergence, and generalization. The project emphasizes hands-on understanding of classic algorithms and their modern, optimized counterparts.  

## Objectives  
- **Implement from scratch**: Perceptron and Adaline (batch gradient descent).  
- **Train with scikit-learn**: Perceptron, Adaline (via `SGDRegressor`), Logistic Regression, and Linear SVM.  
- **Preprocessing**: Handle missing values, encode categorical features, and standardize numeric features using `ColumnTransformer` and `Pipeline`.  
- **Model selection**: Apply `GridSearchCV` for hyperparameter tuning with cross-validation.  
- **Evaluation**: Compare training/test performance, visualize decision boundaries, and analyze validation predictions.  
- **Reflection**: Discuss why scikit-learn implementations outperform the simplified textbook code.  

## Deliverables  
- **Jupyter Notebook**: Code, preprocessing steps, model training, evaluation, and plots.  
- **CSV Files**: Predicted outputs on the validation dataset for each model (`Group_XX_Model_PredictedOutputs.csv`).  
- **Report/Slides**: Summarize methodology, results, and reflections.  
