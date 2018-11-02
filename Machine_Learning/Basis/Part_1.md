Part_1
===

Index
---
<!-- TOC -->
* [Bias and Variance](#Bias-and-Variance)
  * [Reason causes Bias & Variance](#Reason-causes-Bias-&-Variance)
  * [Bias & Vairance in Deep Learning](#Bias-&-Variance-in-Deep-Learning)
  * Bias/Variance with Boosting/Bagging
  * How to calculate Bias & Variance
  * Tradeoff in Bias & Variance

<!-- TOC -->
 
## Bias and Variance
* **Bias** and **Variance** are used to evaluate two aspectss of model generalization error
  * The **Bias** of model refers to the difference between the expected value predicted by the model and true value;
  *  The **Variance** of model refers to the sum of the square difference between the expected value and predicted value predicted by the model
* In **Supervise Learning**, model generalization error comes from the sum of **Bias**, **Vairance** and **Noise**
* **Bias** is used to describe **model fitting ability**</br>
* **Variance** is used to describe **model stability**
  
### Reason causes Bias & Variance
* Generally **Bias** is caused by we do **warong assumption** on the learning model, or the complexity of modle is not enough
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
* 
