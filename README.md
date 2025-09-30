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
          - We used StandardScaler for the numerical features
          - We used OneHotEncoder for the categorical values
      - Target income by making >50 = 1, and <=50 =0
      - The training/testing split was 70/30
- **Part 2 (Preceptron and Adaline)**
  - Preceptron
      -  Used (`GridsearchCV`) (α, penalty, early_stopping).
      -  It found that the best parameters were (`alpha = .0001`), (`Penalty = Elasticnet`), and (`early_stopping=True`)
        -  Performance:
            - CV score: **.81**
            - Test accuracy: **.84**
  - Adaline
      - Used Adaline (`GD`) and (`SGD`)
      - We tracked the MSE across Epochs, this showed effective learning
      - **Results**
          - AdalineSGD test accuracy: **.8395**
          - AdalineGD test accuracy: **.8407**
      - The best settings were (`n = 0.1`) and (`n_iter = 50`)


- **Part 3 (SVM and Logistic Regression)**
    - **Logistic Regression**
        - Tested C = [0.01, 1.0, 100.0]
        - We found that the best C was 1.0 and it got us an accuracy of .8479

    - **SVM**
        - Tested C = [0.01, 1.0, 100.0]
        - We found that the best C was 0.01 and it got us an accuracy of .8477
    
  - **Decision Boundaries**
      - We tested Age and Capital loss on Logistic Regression we realized that there was a diagonal line so both age and Capital loss mattters
      - We tested Age and Capital loss on SVM we realized that there was an horizontal line so what this means was that the model relies more on capital loss



  - **Regularization**
      - We realized that both models did improve with modarate C values
      - Small C it would underfit
      - Large C it would Overfit
      
        

  - **Confusion Matricies**
      - SVM: [[5609, 387], [803, 1016]]
      - Logestic Regression: [[5530, 466], [723, 1096]]
      - They had basicaly the same performance this basicaly means that both models are strong classifiers


  

        
    
    
        
    
    
    
      
            



  
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
- **Documents** -> Reflection_and_Conceptual_Questions.md, Group 16 Slides - Final.pptx
- **Notebook** -> Group_16_sklearn_perceptron_adaline.ipynb
- **ML_outputs** -> output prediction files for adaline, preceptron, SVM, and Logistic Regression
