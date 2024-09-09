# Training ML Models

## Learning Objectives

This section will help you understand:

- What it means to train an AI model
- Hyperparameters
- Issues with training like over- and under-fitting
- Transfer learning and fine tuning


## Model Training

Model training is at the heart of an AI project. It’s the process of feeding data examples to your model so that it can learn the patterns that are present. In supervised learning and generative AI, the model learns from data examples and their labels. In unsupervised learning, the model learns just from the data examples with no labels. In reinforcement learning, the model learns through interaction with the real world, or a simulation of it.

Models themselves consist of _parameters_, or _weights_, and training is the process of learning the values of those parameters. A linear regression model trained on one dataset might have the same number of parameters as that trained on another, but the learned parameter values are different because they've been learned from the different training datasets.

The number of parameters varies wildly between models. A small linear regression model might have in the order of 10 parameters, while a state-of-the-art generative AI model might have 10 billion or more parameters. Larger models require more time & computational power to train - often needing multiple GPUs for the largest models - while small models can be trained locally in minutes on just a CPU. Complex tasks typically need larger models for acceptable performance.

The training algorithm itself to learn these parameter values is also an iterative process. You feed training data into the model, then the algorithm figures out how wrong the model is for these data points and makes small adjustments to the parameters to perform a little better. The question of whether the model fits the data points is judged by a _loss function_ or an _objective function_ that can compute how well the model matches the data as training progresses. Over time, with lots of iterations passing over the training dataset, the parameters converge to a place where they model the training data well. Each pass over the entire training data set is known as an _epoch_.

As a researcher using AI, you can often get started exploring AI without needing to know the details of the training, as there are powerful software libraries that handle the implementation.


## Hyperparameters


The purpose of model training is to find optimal values for the model parameters. However, there are other parameters in machine learning that aren't part of the model. These are called _hyperparameters_, and they affect the outcome of the model training. These might be, for example, the number of layers in your neural network, the number of training epochs, or the learning rate of your training algorithm.

Many implementations of AI model training have good default settings for the hyperparameters. However, one purpose of a development set is to have data available for tuning the hyperparameters. There are several strategies for hyperparameter tuning. The simplest is known as _grid search_, and involves testing hyperparameter values across a range of values. So, in practice, tuning the hyperparameters means building models with several different hyperparameter values, testing the performance of those models on the development data, and choosing the model with best performance. By tuning hyperparameters on a development set, the test set can remain held out, and avoid overfitting.



## Randomness in Training



There are many places in ML training where randomness is used. Examples include the random initialisation of weights (parameters) at the beginning of training, the hardware that you’re building on, or the random shuffling of the data that you’re using for training. Randomness is essential to the performance of ML models, but can also prevent reproducibility of your work. 

Two ways to account for randomness are:

- Use a fixed ‘random seed’ to get the same results each time your code is run, and enable reproducibility
- Train multiple models with multiple random settings, and average the results

Randomness can be very difficult to eliminate entirely in more complex experimental setups. 


## Issues with training

Two ways that training can be derailed are over- and under-fitting.

**Over-fitting** is where the model learns the training data too well, capturing noise and details that do not generalise to the test data. This results in poor performance on development or test data, despite excellent performance on the training data. Over-fitting can be a risk if you don’t have enough data, or your model is complex.

**Under-fitting** is the opposite, where a model is too simplistic to capture details of the training data. You might have a lot of data and a simple model, so the model isn't able to approximate the data well. In this case the model will perform poorly on both your training and test set.

## Training vs Finetuning

You do not always need to train a model from scratch. Often, there can be a model out there which you can use as a starting point. Then, you would finetune that model to your data, or use transfer learning.

**Finetuning** is where you keep the model architecture as it is, and just train the model a bit more on your data.

**Transfer learning** is similar to finetuning, but with the understanding that you're training the model for a different task than the one it was originally trained to do. With neural networks, this typically means replacing the last layer with one which is designed for your task.

The advantage of starting from an existing pretrained model is that you typically don't need as large a dataset as you would if training a model entirely from scratch. 

## Contact

If you can't find what you need

[CONTACT US :fontawesome-solid-paper-plane:](mailto:accelerate-mle@cst.cam.ac.uk){ .md-button }



