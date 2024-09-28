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

**"Random upsampling"** is a technique used to balance imbalanced datasets by randomly increasing the number of samples in the minority class. In this process, samples from the minority class are randomly selected and duplicated, which helps to equalize the representation of classes in the dataset and improve the performance of predictive models in situations of extreme imbalance.

**"Random downsampling"** is a technique used to reduce the number of samples in the majority class of an imbalanced dataset. This is achieved by randomly selecting samples from the majority class and removing them from the dataset, which helps to balance the representation of the classes and improve the performance of predictive models in situations of extreme imbalance.

**SMOTE (Synthetic Minority Over-sampling Technique)** is a supervised resampling method used to balance imbalanced datasets by synthetically generating new samples of the minority class. The algorithm works as follows:

1. For each sample in the minority class, find its k nearest neighbors from the same class.

2. Randomly select one of the k neighbors.

3. Calculate the difference between the feature vector of the current minority sample and the feature vector of the selected neighbor.

4. Multiply this difference by a random number between 0 and 1.

5. Add the result to the features of the current minority sample to generate a new synthetic sample.

This process is repeated until the desired number of synthetic samples of the minority class is reached. This allows for an increase in the representation of the minority class in the dataset, which helps to improve the performance of predictive models in situations of extreme imbalance.

**ADASYN (Adaptive Synthetic Sampling)** is a resampling method used to balance imbalanced datasets in machine learning. This method generates synthetic samples for the minority classes based on the density distribution of the original samples. Unlike techniques such as SMOTE, ADASYN focuses on generating synthetic samples for the minority samples that are harder to learn, which can significantly improve the performance of predictive models in situations of extreme imbalance.

ADASYN works as follows:

1. **Density Distribution**: The density distribution of each sample in the minority class is calculated.

2. **Synthetic Sample Generation**: Synthetic samples are generated based on the calculated density distribution.

3. **Adaptation**: The number of synthetic samples generated is adjusted according to the learning difficulty of each minority sample, allowing the focus to be on the harder samples.

This adaptive approach helps to improve the representation of the minority classes and to reduce the bias towards the majority class, enhancing the accuracy of predictive models in applications such as intrusion detection, medical research, and fraud detection.
