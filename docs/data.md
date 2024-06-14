# Data for AI


## Learning Objectives

This section will help you understand:

- What data is and how it's stored
- How much data you need and how dataset size impacts your options
- Data issues
- Where researchers look for data



## Working with data
To build an AI model, you'll be working closely with data. Data can make or break your project, and so it's crucial to think carefully about the data you're using and how it'll impact your task. 

The data you use for your AI work is tightly connected with what you're trying to achieve. If you're building a system that translates between languages, then your data will be text in the languages you're interested in. If you're diagnosing medical conditions, then your data will likely be medical test results or biomarkers. 

Data can be stored in several formats, whether it's in a spreadsheet, as files on your local machine, or in the cloud.

It is transformed into something computer readable by _feature extraction_, which is the step to convert your data into a numerical format that AI models can ingest.

## Data Splits
It's important when training to separate your data into training, development, and test sets.

- **Training** data is used for adjusting the model parameters during the model training phase
- **Development** data is used to judge the model performance at intermediate stages, and may be used for tuning hyperparameters
- **Test** data is used at the end of development to estimate how well your model performs on unseen data

It is important to ensure that there's no leakage or cross-over between training and testing data.

One really common way that leakage happens is during data pre-processing. It's common to estimate some transformations of the data. For example, normalising it so that the mean and standard deviation are 0 and 1. Estimating the transformations should be done only on the training set, and then should be applied to the development and test data. 

If you have a small set, and carving out separate test and development sets leaves you with only a very small amount of training data, then a technique like _k-fold cross validation_ may be appropriate. 

If you have a dataset, then a common rule of thumb is to use 80% of data for training, 10% for development, and 10% for testing. However, you do need to be sure that 10% of data you have left for testing is enough data that you can see statistically significant results.

Usually, you'd create these data splits by randomly sampling your entire set. There may be cases though where you want to do something different. One example is stratified sampling, where you split your data into segments and sample from each segment to be sure you have full representation in your test set. Another example is where you have multiple data points from multiple people, and you want t ensure that a single person's data doesn't span the sets. For example, suppose you are working with audio files and you would like to keep each speaker's data in a single split.

If you move to collecting data from multiple different sources, you might need to carefully think about how to split your data. If you use synthetic data in your training set, you might not split that synthetic data between your test sets. 



## How much data do you need?
This is a commonly asked question, but unfortunately there's no hard and fast answer! Sometimes the only way to know if you have enough data is to build a model and test its performance. Some of the factors that influence data needs are:

**Task**: some tasks are inherently easier than others, and require less data to model. 

**Model**: the larger and more complex your model, the more data you need.

**Diversity**: you also need diversity in your data as well as quantity. Simply adding more data that has the same information won't really improve your model.

**Starting point**: starting from scratch usually requires more data than if you're finetuning an already existing model.

**Data dimension**: the higher the dimensionality of your data, the more of it you need to model effectively. 



## Data issues

Data is often the source of many problems researchers encounter when building AI models.

A typical issue arises when there is a difference between the training and testing data that you're using. Perhaps training data was collected in one way, and test data in another. 

A similar issue arises when data distributions change over time, and is called _data drift_. This happens all the time in real-world scenarios! Consider the language that we use. Models trained on language from 200 years ago probably wouldn't do well on today's language! And even models trained 20 years ago might miss some crucial language changes. 

Problems with data can sometimes be very subtle. Consider this paper that deliberately trained a poor classifier to distinguish [wolves and huskies](https://arxiv.org/abs/1602.04938). In this setup, the images of wolves all had snow in the background, while images of huskies didn't have snow. Rather than distinguish the wolves and huskies based on their appearance, the classifier _actually_ learned to distinguish snowy from non-snowy scenes. 

Skewed data is where there is an imbalance in the amount of data between classes, because one class is far more common than another. This is common in, say, medical contexts where the number of people with a particular condition is far lower than those without. 

Finally, depending on what you're doing, your data may contain personal and sensitive information about people. Keeping it safe and secure is crucial.

Often, if you have trouble getting a machine learning model to perform well, the first place to start looking for issues is in the data that you're using to train your model. 


## Where to get data from

- Collection: can you collect the data you need from volunteers, or some other way?
- Open source: there are many open source datasets available, which might work for your task. Many open source sets are ready split into test & training sets for you to use.
- Experimental results: it's common to use AI methods on experimental data from your work or your lab's results. 
- Synthetic: Generating synthetic data is an increasingly common way to create training data. 
- Partnerships: partnering with other labs or organisations to share data can be an effective way to boost the amount of data you're working with.

## Contact

If you can't find what you need

[CONTACT US :fontawesome-solid-paper-plane:](mailto:accelerate-mle@cst.cam.ac.uk){ .md-button }





