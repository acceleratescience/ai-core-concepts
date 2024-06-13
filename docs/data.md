# Data for AI


## Learning Objectives

This section will help you understand:

- What data is and how it's stored
- How much data you need and how dataset size impacts your options
- Data issues
- Where researchers look for data



## Dealing with data
To build an AI model, you'll be working closely with data. Data can make or break your project, and so it's crucial to think carefully about the data you're using and how it'll impact your task. 

The data you use for your AI work is tightly connected with what you are trying to achieve. If you are building a system that translates between languages, then your data will be text in the languages you're interested in. If you're diagnosing medical conditions, then your data will likely be medical test results or biomarkers. 

Data can be stored in several formats, whether it's in a spreadsheet, as files on your local machine, or in the cloud.

It is transformed into something computer readable by _feature extraction_, which is the step to convert your data into a numerical format for AI models to use. 

To use your data, you'll need to split it into several parts. One part will be for training your model, one part for development work, and one for the testing of your model at the end of your work.

If you have a dataset, then a common rule of thumb is to use 80% of data for training, 10% for development, and 10% for testing. However, you do need that 10% for testing to be enough data that you can see statistically significant results.

If you don't have enough data for this split, you can use an N-fold cross validation setup.

If you have more data, and from different sources, you might need to carefully think about how to split your data. It's important, for example, that your test set reflects the task you're trying to do. If you use synthetic data in your training, you might keep that out of your test set. 



## How much data do you need?
This is a commonly asked question, but there's no hard and fast answer.

**Task** some tasks are inherently easier than others, and require less data. 

**Model** the larger your model, the more data you need

**Diversity** you also need diversity in your data as well as quantity. More data that has the same information in won't really improve your model

**Starting point** starting from scratch usually requires more data than if you're finetuning an already existing model.


## Data issues

Data drift refers to data where the distribution changes over time.

Related is the shift between training and test data distribution. If you collect training data in one way, and test data in another, there may be a difference between the two sets. 

Skewed data is where there is an imbalance between classes. 

Data is often the source of many problems with building AI models. husky/wolf example. 

Depending on what you're doing, your data may contain personal and sensitive information about people. Keeping it safe and secure is crucial. 


## Where to get data from

- Collection: can you collect the data you need from volunteers, or by some other way?
- Open source: there are many open source datasets available, which might work for your task. Many open source sets are ready split into test & training sets for you to use
- Experimental results: it's common to use AI methods on experimental data from your work or your lab's results. 
- Synthetic: Generating synthetic data is an increasingly common way to create training data. 
- Partnerships: partnering with other labs or organisations to share data can be an effective way to boost the amount of data you're working with

## Contact

If you can't find what you need

[CONTACT US :fontawesome-solid-paper-plane:](mailto:accelerate-mle@cst.cam.ac.uk){ .md-button }





