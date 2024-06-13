# Training ML Models

## Learning Objectives

This section will help you understand:

- Know what it means to train an AI model
- How to use data for robust training, development and testing
- Over and under fitting
- Tuning hyperparameters
- Transfer learning and fine tuning
- Know about the iterative approach to building a model

## Training supervised models

Training a supervised learning algorithm involves:

![AI Lifecycle](imgs/ailifecycle.png){ align=center }

1. decide on the task and collect data; label that data
2. train a model on a 'training' set of your data
3. evaluate the model on a separate test set, to see how well it does
4. investigate the errors to see where you can improve

This tends to be an iterative process, not a linear one, so you may need to loop through these steps several times to get a model that works. 

## What is training?
Model training is the process of feeding data examples to your model so that it can learn. Usually, models are generic and have a lot of numbers (parameters). Training is the process of learning those parameters. The number of parameters varies wildly between models. A small linear regression model might have in the order of 10 parameters, while a state-of-the-art generative AI model might have 10 billion parameters. 

A linear regression model trained on one dataset might have the same number of parameters as that trained on another, but the parameter values are different.

Training is an interative process where you feed data into the model, it figures out how wrong the model is for those values, and then makes small adjustments to the parameters to be a little better. Over time, with lots of iterations, the parameters get to model the data well. 




## Data
The first thing to do when training a model is to separate your data into testing and training. 
Split your data into train, test, dev splits.
Really important to ensure no leakage between training and testing.
Shuffling your data


## Over and under fitting

Two ways that training can do badly are over and under fitting.

**Overfitting** is where you have a small amount of data and a complex model, so the model learns to model the training set really well. In this case, the model will perform really well on the training set, but poorly on your test set. 

**Underfitting** is the opposite, where you might have a lot of data and a simple model, so the model doesn't do well at approximating the data. In this case the model will perform poorly on both your training and test set. 

## Hyperparameters

When training, we mentioned the model parameters above, that get modified by the training process. There are other parameters too, called hyperparameters, that you might need to tune. These might be, for example, the number of layers in your neural network, or the learning rate of your training algorithm.

We usually keep a separate development set for use with tuning hyperparameters. This lets us keep the test set held out, and avoid overfitting. 



## Top Tips for getting started


1. Prototype - start with a small model and a simple baseline; Start with a small dataset, before increasing the amount of data
2. Ensure there's no leakage between your test and training data
3. Make use of open source libraries, models and data

## Inspiration

Find more examples of research that's using supervised learning on Accelerate's blog:

- link
- link
- link


## Contact

If you can't find what you need

[CONTACT US :fontawesome-solid-paper-plane:](mailto:accelerate-mle@cst.cam.ac.uk){ .md-button }



