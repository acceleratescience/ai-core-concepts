# Evaluating AI Models


## Learning Objectives
This section will help you understand:

- Using test data to robustly evaluate models
- Quantative vs qualitative evaluation
- Evaluation metrics
- Error analysis tools including stratification, confusion matrices & ROC

## Overview

All machine learning models make mistakes. Consider a binary classification supervised model that's used to identify spam emails, and has been trained on a training dataset (circles). As the model weights have been trained using the training data, we can't use that data to see how well the classifier performs. That's a bit like seeing the exam questions ahead of time! To judge how well the classifier performs, we test its performance on a separate test set (triangles). 

![Evaluation](imgs/eval1.png){ align=center }

## Data
It's important when training to separate your data into training, development, and test sets.

- **Training** data is used for adjusting the model parameters during the model training phase
- **Development** data is used to judge the model performance at intermediate stages, and may be used for tuning hyperparameters
- **Test** data is used at the end of development to estimate how well your model performs on unseen data

It is important to ensure that there's no leakage or cross-over between training and testing data.

One really common way that leakage happens is during data pre-processing. It's common to estimate some transformations of the data. For example, normalising it so that the mean and standard deviation are 0 and 1. Estimating the transformations should be done only on the training set, and then should be applied to the development and test data. 

If you have a small set, and carving out separate test and development sets leaves you with only a very small amount of training data, then a technique like _k-fold cross validation_ may be appropriate. 

## Qualitative vs Quantative Evaluation
There are two main categories of way to evaluate how well your model is working

1. *Quantative* evaluations devise an automated metric which you can automatically compute on your test set to give a score
2. *Qualitative* evaluations ask people to interact with your model and judge it

For some tasks, like spam email detection, we can automatically compute an accuracy metric. For other tasks, like machine translation, there are many possible correct answers and it's hard to find a good automated metric. Hence, the way to judge performance is by having people evaluate the translations.

Qualitative evaluations are expensive to perform, and so in practice it's often helpful to have a mix of quantitative and qualitative metrics. 


## Metrics

There are a wide range of metrics in use for different tasks, so the best thing to do is to look at the literature and see what people are using. However, some common metrics exist. For classification:

- **Accuracy** is simply how often the classifier is right. This is computed by comparing the classifier's prediction against the ground truth human labels in a test set. 
- **Precision** is a measure of how many of your positive classifications were correct. For the spam email case, it's the proportion of emails the model identified as spam that actually were spam. 
- **Recall** tells you what proportion of your positives were correct. For the spam email case, it's the proportion of actual spam emails the model identified as spam.

[Precision and recall](https://developers.google.com/machine-learning/crash-course/classification/precision-and-recall) are used together. An increase in one usually means a decrease in the other. 

For regression tasks,

- **RMSE** root mean squared error, is a measure of how far on average your predictions are from the ground truth label. 

You'll need to use your judgement to interpret a particular metric. An accuracy or 5% may be great for one task, but terrible for another. 

## Error Analysis

Usually, you 'll want to look deeper at the kind of errors that a model is making, in order to identify places where you can improve. Some useful ways to view errors are:

- **Confusion matrix**: a plot showing which categories were confused with each other.
- **ROC** a graph that shows classification error as you change the classifier's threshold.
- **Stratification** of your test data into different subgroups, to compute the error on those. This can help identfy sub-populations with different performance. 

## Contact

If you can't find what you need

[CONTACT US :fontawesome-solid-paper-plane:](mailto:accelerate-mle@cst.cam.ac.uk){ .md-button }





