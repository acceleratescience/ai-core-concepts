# Training ML Models

## Learning Objectives

This section will help you understand:

- What it means to train an AI model
- How to use data for robust training, development and testing
- Over and under fitting
- Tuning hyperparameters
- Transfer learning and fine tuning

## Building Machine Learning Models

Building a machine learning model involves:

1. Deciding on the task and collecting data; labelling that data
2. Training a model on a '_training set_' of your data
3. Evaluating the model on a separate '_development set_', to see how well it does
4. Investigating the errors to see where you can improve

This tends to be an iterative process, not a linear one, so you may need to loop through these steps several times to get a model that works. Once you have a model that works well, you can evaluate its final performance on a '_test set_'.

![AI Lifecycle](imgs/ailifecycle.png){ align=center }

## Supervised Model Training
In a supervised learning scenario, model training is the process of feeding data examples to your model so that it can learn the patterns that are present. Models themselves consist of _parameters_, and training is the process of learning the values of those parameters. The number of parameters varies wildly between models. A small linear regression model might have in the order of 10 parameters, while a state-of-the-art generative AI model might have 10 billion parameters. 

A linear regression model trained on one dataset might have the same number of parameters as that trained on another, but the parameter values, or _weights_, are different because they've been learned from the data.


The training algorithm itself is also an iterative process. You feed training data into the model, then the algorithm figures out how wrong the model is for these data points and makes small adjustments to the parameters to perform a little better. Over time, with lots of iterations passing over the training dataset, the parameters converge to a place where they model the training data well. You often don't need to know the details of the training, as there are powerful software libraries that handle the implementation. 




## Data
It's important when training to separate your data into training, development, and test sets.

- **Training** data is used for adjusting the model parameters during the model training phase
- **Development** data is used to judge the model performance at intermediate stages, and may be used for tuning hyperparameters
- **Test** data is used at the end of development to estimate how well your model performs on unseen data

It is important to ensure that there's no leakage or cross-over between training and testing data.


## Over and under fitting

Two ways that training can be derailed are over- and under-fitting.

**Overfitting** is where you have a small amount of data and a complex model, so the model learns to model the training set really well. In this case, the model will perform really well on the training set, but poorly on your test set. 

**Underfitting** is the opposite, where you might have a lot of data and a simple model, so the model isn't able to approximate the data well. In this case the model will perform poorly on both your training and test set. 

## Hyperparameters

The purpose of model training is to find optimal values for the model parameters. However, there are other parameters in machine learning that aren't part of the model. These are called _hyperparameters_.

These might be, for example, the number of layers in your neural network, or the learning rate of your training algorithm. The purpose of a development set is to have data for tuning the hyperparameters. This lets us keep the test set held out, and avoid overfitting.

## Transfer Learning and Fine Tuning
You do not always need to train a model from scratch. Often, there can be a model out there which you can use as a starting point. Then, you would finetune that model to your data, or use transfer learning.

**Finetuning** is where you keep the model architecture as it is, and just train the model a bit more on your data.

**Transfer learning** is similar to finetuning, but with the understanding that you're training the model for a different task than the one it was originally trained to do. With neural networks, this typically means replacing the last layer with one which is designed for your task. 


## Top Tips for getting started

1. Look at what ML models exist. Hugging Face, for example, has a large repository of models available to use. Or in your field, perhaps a relevant group has released a model onto GitHub.
2. Consider whether you can build a baseline system without ML/AI. This will be a simple first step, and likely give you some insight into your problem. 
3. Prototype - start with a small model and a simple baseline; Start with a small dataset to get your setup working, before increasing the amount of data
4. Ensure there's no leakage between your test and training data
5. Make use of open source libraries, models and data

## Inspiration


## Contact

If you can't find what you need

[CONTACT US :fontawesome-solid-paper-plane:](mailto:accelerate-mle@cst.cam.ac.uk){ .md-button }



