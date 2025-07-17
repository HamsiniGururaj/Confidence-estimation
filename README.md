# Confidence Estimation
This codebase is an implementation of the paper: Confidence Estimation Using Unlabeled Data  
https://arxiv.org/abs/2307.10440

- We estimate the prediction certainty or confidence of an image classification model in semi-supervised learning setting which uses ResNet
- **Consistency implies confidence**: If the model gives the same output for a particular input in a large percentage of the epochs, it means that the model is sure of that particular prediction 

## Dataset
- The dataset used is CIFAR10
- To simulate semi supervised learning, the train set consists of 70% unlabeled data and 30% labeled data while the test set has 100% labeled data

## Loss functions
- We track the consistency and correctness of the model across all the training epochs
- These values are used to calcuate the consistency ranking loss and correctness ranking loss
- These losses along with the Cross Entropy Loss are used to measure the estimated confidence of the model
