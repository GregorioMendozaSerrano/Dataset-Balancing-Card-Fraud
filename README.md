# **Dataset Balancing - Practical Exercise**

## *Gregorio Mendoza Serrano*

During this exercise, we will analyze what needs to be done in highly imbalanced environments, such as credit card fraud. In this environment, the fraud detection rate can be as low as 1 in 1000. Therefore, the initial challenge is always to have a properly balanced dataset.
Fraud detection systems rely on a set of parameters or attributes from each credit card transaction to predict whether a particular transaction is fraudulent or not.
The goal of this exercise is to explore various techniques for oversampling or subsampling.

As a source for this exercise, we will work with a credit card data dataset where transactions are already categorized as fraudulent or not:
https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud?resource=download

---
**Note:** This notebook will use the proposed dataset (*credit card fraud*) to compare four different balancing techniques:
- Random Upsampling
- Random Downsampling
- SMOTE Resampling
- ADASYN Resampling
---
**Note2:** This notebook is designed to be executed locally. 
---
# 2. Balancing Methods (Functions)
