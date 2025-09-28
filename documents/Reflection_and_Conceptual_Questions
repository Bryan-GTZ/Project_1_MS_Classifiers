# Reflection and Conceptual Questions

## 1. Why is feature scaling important for gradient-based algorithms?
In the Dataset we worked with, certain features, like age, would range from 17 years all the way to 90 years. We also had another feature, education number, which would only go from 1 to 16. Gradient algorithms, such as Adaline and Logistic Regression, have a habit of treating features as more important just because the numbers are larger. Since the features have been standardized, this allows the algorithm to converge faster, and the decision boundaries will not be influenced negatively by the units.

---

## 2. Difference between batch gradient descent and stochastic gradient descent
- **Batch Gradient Descent (BGD)**  
  Uses the whole dataset for each update.  
  - Pros: Stable convergence.  
  - Cons: Works very slowly on large datasets.  

- **Stochastic Gradient Descent (SGD)**  
  Updates its weights after every sample.  
  - Pros: Works well on big data because it is fast and scalable.  
  - Cons: Noisy path because it jumps around until it gets up to the optimum.  

---

## 3. Why does scikit-learn Perceptron and Adaline outperform book code?
In the *Machine Learning with PyTorch and Scikit-Learn* (Raschka et al.), it talks about how it made the Perceptron and Adaline simple on purpose; they both use batch gradient descent, fixed learning rate, and barely any stopping logic. As a result, this makes these implementations more of an example.  

As we can see, the scikit-learn Perceptron and SGDRegressor/SGDClassifier are tailored to fit the situation. We added stochastic or mini-batch gradient descent, shuffling, and regularization. Since we implemented all of these features, this has improved generalization and convergence speed, as mentioned in the textbook. They are also being fed through pipelines and are being cross-validated.

📖 **Reference**  
> Raschka, S., Liu, Y., & Mirjalili, V. (2022). *Machine Learning with PyTorch and Scikit-Learn*. Packt Publishing.  
> (See Chapter 2 on Adaline and gradient descent, and Chapter 3 on scikit-learn’s Perceptron).

