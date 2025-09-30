# # Project 1: Machine Learning Classifiers

## Introduction  
This project explores and compares several linear machine learning classifiers on the **UCI Adult Income dataset**. The primary goal is to predict whether an individual’s income exceeds \$50K per year based on demographic and employment attributes.  

We implement both **custom algorithms** from *Machine Learning with PyTorch and Scikit-Learn* (Raschka, Liu, & Mirjalili, 2022) and **scikit-learn equivalents**, highlighting differences in performance, convergence, and generalization. The project emphasizes hands-on understanding of classic algorithms and their modern, optimized counterparts.  

## Objectives  
- **Implement from scratch**: Perceptron and Adaline (batch gradient descent and SGD).  
- **Train with scikit-learn**: Perceptron, Adaline ( `SGDRegressor`), Logistic Regression, and Linear SVM.  
- **Preprocessing**: Handle missing values, encode categorical features, and standardize numeric features using `ColumnTransformer` and `Pipeline`.  
- **Model selection**: Apply `GridSearchCV` for hyperparameter tuning with cross-validation for the Preceptron.
- **Evaluation**: Compare training/test performance, visualize decision boundaries, and analyze validation predictions.
- Vary the C values of the scikit-learn LogisticRegression and linear SVC models
- **Reflection**:
- Why is feature scaling important for gradient-based algorithms?
- Explain the difference between batch gradient descent and stochastic gradient descent.
- Why does scikit-learn Perceptron and Adline algorithms outperform book code?
- Compare the decision boundaries of logistic regression and SVM.
- What is the role of regularization in preventing overfitting?
- Vary the C values of the scikit-learn LogisticRegression and linear SVC models with  [0.01, 1.0, 100.0] .


## Deliverables  
- **Jupyter Notebook**: Code, preprocessing steps, model training, evaluation, and plots.  
- **CSV Files**: Predicted outputs on the validation dataset for each model (`Group_16_Model_PredictedOutputs.csv`).  
- **Report/Slides**: Summarize methodology, results, and reflections.


## Location of Repository
- **Documents** -> Reflection_and_Conceptual_Questions.md
- **Notebook** -> Group_16_sklearn_perceptron_adaline.ipynb
- **ML_outputs** -> output prediction files for adaline, preceptron, SVM, and Logistic Regression
