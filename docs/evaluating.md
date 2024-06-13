# Evaluating AI Models


## Learning Objectives
This section will help you understand:

- Using test data to robustly evaluate models
- Quantative vs qualitative evaluation
- Evaluation metrics
- Error analysis tools including confusion matrices & ROC

## Data split
Split your data into train/test/dev splits
If you have a small set, something like k-fold cross validation is the best bet. 

## Qualitative vs Quantative
There are two main categories of way to evaluate how well your model is working

1. Devise an automated metric which you can run to find a score
2. Ask people to interact with your model and judge it




## Metrics

All AI models make mistakes. Metrics depend on what it is you're trying to do.

Automated metrics are run over a test dataset. For classification, some common ways to judge performance are:

- **Accuracy** is simply how often the classifier is right
- **Precision** tells you for a category, how many things predicted to be in that category actually belong to that category. 
- **Recall** tells you for a category, how many things of that category are predicted as being in that category. 

Precision and recall are used together. An increase in one usually means a decrease in the other. 

For regression tasks,

- **RMSE** root mean squared error, is a measure of how far on average your predictions are from the ground truth. 

You need to use your judgement to interpret a particular metric. An accuracy or 5% may be great for one task, but terrible for another. 

## Error Analysis

Usually, you will want to look deeper at the kind of errors that a model is making, in order to identify places where you can improve. Some useful ways to view are:

- **Confusion matrix**
- **ROC** 

## Contact

If you can't find what you need

[CONTACT US :fontawesome-solid-paper-plane:](mailto:accelerate-mle@cst.cam.ac.uk){ .md-button }





