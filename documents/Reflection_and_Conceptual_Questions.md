# Reflection and Conceptual Questions
--

# Feature Scaling

In the Dataset we worked with, certain features, like age, would range from 17 years all the way to 90 years. We also had another feature, education number, which would only go from 1 to 16. Gradient algorithms, such as Adaline and Logistic Regression, have a habit of treating features as more important just because the numbers are larger. Since the features have been standardized, this allows the algorithm to converge faster, and the decision boundaries will not be influenced negatively by the units.

---

# Batch vs. Stochastic Gradient Descent

Batch Gradient Descent uses the whole dataset for each update, while Stochastic Gradient Descent updates its weights after every sample. They each have their pros and cons. 

- Batch Gradient Descent has a stable convergence, but it works very slowly on large datasets.  
- On the other hand, Stochastic Gradient Descent works well on big data because it is fast and scalable, but it does have a noisy path because it jumps around until it gets up to the optimum. 

---

# Perceptron and Adaline

In the Machine Learning with PyTorch and Scikit-Learn, Raschka et al. It talks about how it made the Perceptron and Adaline simple on purpose; they both use batch gradient descent, fixed learning rate, and barely any stopping logic. As a result, this makes these implementations more of an example.  

As we can see, the scikit-learn perceptron and SGDRegressor/SGDClassifier are tailored to fit the situation. We added stochastic or mini-batch gradient descent, shuffling, and regularization. Since we implemented all of these features, this has improved generalization and convergence speed, as mentioned in the textbook. They are also being fed through pipelines and are being cross-validated.  

*Raschka, S., Liu, Y., & Mirjalili, V. (2022). Machine Learning with PyTorch and Scikit-Learn. Packt Publishing. (see Chapter 2 on Adaline and gradient descent, and Chapter 3 on scikit-learn’s Perceptron).*

---

# Compare Decision Boundaries: Logistic Regression vs. SVM

Both Logistic Regression and the SVM classifiers create straight line decision boundaries to separate and classify the data. The difference between the two models is their objective. 

- The SVM finds a boundary that maximizes the difference between the closest points of the support vector. It focuses on the most critical points only.  
- The Logistic Regression classifies its boundary by finding the probability that a given point belongs to a certain class.  

The difference is shown in my visuals, where I used Age and Capital Lost to create my decision boundaries. The Logistic Regression model’s boundary is a steep line, and the SVM model has no slope. This implies that the SVM model is not considering the "Age" index as much as it is the "Capital Loss" when classifying.  

---

# Regularization and Overfitting

Regularization prevents overfitting, which is when the model learns the training data’s noise and not its patterns. Overfitting creates an inefficient and complex model that performs poorly when new data is introduced. To prevent this, regularization adds a penalty to the loss function. In doing this, there are fewer large coefficients, which makes the model simple and more successful.  

In my project, the C parameter is what controls regularization. A smaller C value relates to a stronger regularization, and a large C value means a weaker regularization, which makes it more prone to overfitting.  

---

# Varying C Values

Varying the C values for Logistic Regression and SVM showed different results for both models. The smaller C value shows stronger regularization, which creates a simpler model. A larger C value allows for more complex work.  

- For the Logistic Regression, the best performing model was present when the C Values was 1.0, and it had an accuracy of 0.8479. This leads me to believe that a moderate regularization prevents underfitting from a small C Values and overfitting from a large one.  
- The SVM model performed best when the C Value was 0.01, achieving an accuracy of 0.8477. As the C Value increased, the accuracy got slightly worse, which hints at the fact that SVM was more likely to experience overfitting and a stronger penalty helped improve accuracy.  

*Raschka, S., Liu, Y., & Mirjalili, V. (2022). Machine Learning with PyTorch and Scikit-Learn. Packt Publishing. (see Chapter 3 for information on logistic regression and Support Vector Machines).*
