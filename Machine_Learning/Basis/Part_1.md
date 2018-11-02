Part_1
===

Index
---
<!-- TOC -->
* [Bias and Variance](#bias-and-variance)
  * [Reason causes Bias & Variance](#reason-causes-bias-&-variance)
  * [Bias & Vairance in Deep Learning](#bias-variance-in-deep-learning)
  * [Bias/Variance with Boosting/Bagging](#Bias/Variance-with-Boosting/Bagging)
  * [How to calculate Bias & Variance](#How-to-calculate-Bias-&-Variance)
  * [Tradeoff between Bias & Variance](#Tradeoff-between-Bias-&-Variance)

<!-- TOC -->
 
## Bias and Variance
* **Bias** and **Variance** are used to evaluate two aspectss of model generalization error
  * The **Bias** of model refers to the difference between the expected value predicted by the model and true value;
  *  The **Variance** of model refers to the sum of the square difference between the expected value and predicted value predicted by the model
* In **Supervise Learning**, model generalization error comes from the sum of **Bias**, **Vairance** and **Noise**
* **Bias** is used to describe **model fitting ability**</br>
* **Variance** is used to describe **model stability**
  
### Reason causes Bias & Variance
* Generally **Bias** is caused by we do **wrong assumption** on the learning model, or the complexity of modle is not enough
  * Supposing one real model is nonlinear model, but we apply a linear model on it which will increase **Bias** which we call **underfitting**
  * We can easily find **Bias** from training data, we can also say that **Bias** comes from training data
* Generally **Vairance** is usually due to the compexity of model relative to the training data being too high
  * Supposing the real model is a quadratic function, and we assume that the model is higher order function, which leads to an increase on the **Variance**(**over fitting**)
  * The error caused by the **variance** is usually reflected in the increment of the test error relative to the training error

## Bias & Variance in Deep Learning
* The fitting ability of Neural Network is very powerful, normally the **training error**(Bias) is small
* However good fitting ability will cause big Variance, which will bring increment of testing error(**Generalization Error**)
* The core work of Deep Learning is to do research about how to decrease the generalization error of the model, we call it regularization method

## Bias/Variance with Boosting/Bagging

## How to calculate Bias & Variance
* Model on **Training Data Set**:
* The expect value of Model
* **Bias**
* **Variance**
* The **Noise** expresses the lower bound of the expected generalization error that any learning algorithm can achieve on the current task, that is, the difficulty of learning the problem itself
* **Bias-Variance decomposition** indicates that the generalization ability of the model is determined by the ability of the algorithm, the adequacy of the data, and the difficulty of the task itself

## Tradeoff between Bias & Variance
* Given Task
 * Unsufficient training, the model has weak fitting ability(**underfitting**), at this time **Bias** is the main reason of **Generalization Error** on the model
 * With having more training, the model's fitting ability will improve, at this time **Variance** will gradually be the main reason of **Generalization Error** on the model
 * After Sufficient Training, the model's fitting ability will be overqualified, which we call it **overfitting**，it means that the model has learned **training data self and non-global features** 
   <div align="center"><img src="../Basis/Image/20181102.png" height="" /></div>

 
