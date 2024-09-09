# Data for AI


## Learning Objectives

This section will help you understand:

- What data is and how it's stored
- How much data you need and how dataset size impacts your options
- Data pre-processing
- Data issues
- How researchers acquire data



## Working with data
To build an AI model, you'll be working closely with data. In particular, you will need a dataset consisting of many examples of the data you’re working with. Data can make or break your project, and so it's crucial to think carefully about the data you're using and how it'll impact your task. It is always worth spending time early in a project to thoroughly understand your data, to visualise it, and to understand its limitations.

The data you use for your AI work is tightly connected with what you're trying to achieve. If you're building a system that translates between languages, then your data will be text in the languages you're interested in. If you're diagnosing medical conditions in clinical settings, then your data could be medical test results, biomarkers, or medical images.

Data can be stored in several formats. Structured data - that’s data that you could list out in a table - could be stored in spreadsheets or specific file formats, like csv or json. Unstructured data like images, audio or text files are more often stored as files on your local machine, or in the cloud.

The input of machine learning models must be numbers, not text, images or other non-numerical data type. Data is transformed into a numerical format by _feature extraction_, which is the step to convert your raw data into a numerical format that AI models can ingest. 

## Data Splits

Typically, when building machine learning models you will acquire a large amount of data, called a dataset. It's important to separate your large dataset into training, development, and test splits. These each have a different purpose during the building process:

- **Training** data is used for adjusting the model parameters during the model training phase
- **Development** data is used to judge the model performance at intermediate stages, and may be used for tuning hyperparameters
- **Test** data is used at the end of development to estimate how well your model performs on unseen data


It is important to ensure that these sets are completely separate from each other, and there's no leakage or cross-over between training and testing data. That’s to ensure the model is tested on data that it hasn’t been trained on.

If you have a dataset, then a common rule of thumb is to use 80% of data for training, 10% for development, and 10% for testing. However, you do need to be sure that 10% of data you have left for testing is enough data that you can see statistically significant differences in performance. If you have very large amounts of data, then you might choose to use more than 80% of it for training. If you have a small set, and carving out separate test and development sets leaves you with only a very small amount of training data, then a technique like _k-fold cross validation_ may be appropriate.

Usually, you'd create these data splits by randomly sampling your entire set. There may be cases though where you want to do something different. One example is stratified sampling, where you split your data into segments and sample from each segment to be sure you have full representation in your test set. Another example is where you have data from multiple sources and not all are appropriate test data. For example, you might choose to use synthetic data in your training set, but only real-world data in your test set. Some datasets also contain multiple examples for each subject, e.g. audio recordings taken as part of a longitudinal study, and it is usually important to ensure that those examples are kept together during the split so that data from one subject is not split across the subsets.

Typically, data is _shuffled_ before its used - i.e. the order is randomised. That’s to ensure that any ordering that may come from the way you collected and named your data files doesn’t impact the training algorithm.


## How much data do you need?

This is a commonly asked question, but unfortunately there's no hard and fast answer! More data is usually better, but sometimes the only way to know if you have enough data is to build a model and test its performance. Some of the factors that influence data needs are:

**Task**: some tasks are inherently easier than others, and require less data to model.

**Model**: the larger and more complex your model, the more data you need.

**Diversity**: you also need diversity in your data as well as quantity. Simply adding more data that has the same information won't improve your model.

**Starting point**: starting from scratch usually requires more data than if you're finetuning an already existing model.

**Data dimension**: the higher the dimensionality of your data, the more of it you need to model effectively.

You can often get a good sense of the size of datasets you need for your task by looking at related work in the literature. In general, more data tends to lead to better performing models, but more data comes with the price of an increased computational cost and longer model training times.

## Data Preprocessing
A large amount of time in any AI project is spent on acquiring, cleaning and processing data. As a scientist, you can expect to spend more time than expected on data related tasks. Data pre-processing is the work needed to prepare raw data for use by AI models.

It's common to estimate transformations of the data, one example is data normalisation. Some features have very different ranges. For example, systolic blood pressure may be in the range 8–180, while the level of hormone TSH is likely in the range 0.4 to 4.0. Using both of these features in a model can be tricky to balance. Data normalisation is where you scale the range of each feature in your data to have a specific mean and variance, typically 0 and 1.

In some fields, when using structured data, not all of the data points are present. Perhaps a particular test is only run for a certain subset of patients, there are data entry errors, or some participants have dropped out of your study. Machine learning models require complete datasets. _Missing value imputation_ is the task of estimating missing values in your data.

Other common pre-processing steps include removing duplicate entries, fixing incorrect entries, increasing dataset size with data augmentation, removing outliers, selecting a subset of features, and dimensionality reduction.

Every step in pre-processing the data is a choice, and it’s important to keep records so that you can reproduce your work, and later recall what choices were made. If you are using open source data from another source, knowing what processing choices they made are important for your own scientific rigour.

One really common way that leakage happens is during data pre-processing. For a robust setup, all of your data pre-processing should be done on the training set only. Taking the example of normalisation, estimating the transformations should be done only on the training set, and then those transformations should be applied to the development and test data. A common mistake is to estimate the transformations over the entire dataset, but this means that information from the test set will leak into your training set, via the transformations. Similar rules apply to other pre-processing operations.

A data pipeline is a series of steps in code that you apply to your data to transform it from raw data into the form that’s ready for use by your AI algorithm. 



## Data issues


Data is often the source of many problems researchers encounter when building AI models.

A typical issue arises when there is a difference between the training and testing data that you're using. Perhaps training data was collected in one way, and test data in another. That means that your model may not work as well on your test set. One example could be a medical imaging model that is trained on images collected at one hospital, but tested on images from another where slight protocol differences mean that the data is subtly different between the two hospitals. Subtle differences like this can be hard to spot, but also highly impactful for your work. 

A similar issue arises when data distributions change over time, and is called data _drift_. This happens all the time in real-world scenarios! Consider the language that we use. Models trained on language from 200 years ago wouldn't perform well on today's language. And even models trained 20 years ago might miss some crucial language changes.

Skewed data is where there is an imbalance in the amount of data between classes, because one class is far more common than another. This is common in, say, astrophysics contexts where the number of transient events of interest is low compared to the number of stable objects.

Finally, depending on what you're doing, your data may contain personal and sensitive information about people. Keeping it safe and secure is crucial. A data management plan is a key tool for describing how you plan to manage your data. It covers factors such as how and where you can process data, where it’s stored, and who can access with different levels of security, and whether it’s anonymised. Your [library](https://www.data.cam.ac.uk/DMPsupport) can offer support on writing a data management plan. Sharing data beyond your group may require a _data transfer agreement_ to be in place.

Problems with data can sometimes be very subtle. Consider this paper that deliberately trained a poor classifier to distinguish [wolves and huskies](https://arxiv.org/abs/1602.04938). In this setup, the images of wolves all had snow in the background, while images of huskies didn't have snow. Rather than distinguish the wolves and huskies based on their appearance, the classifier _actually_ learned to distinguish snowy from non-snowy scenes. Tracking down these subtle data issues can take significant time and effort.

Often, problems with machine learning models - whether they’re not performing well, or are suspiciously good - come down to data. The first place to start looking for issues is in the datasets that you’re using.



## How to acquire data

While many researchers begin with a dataset that they would like to apply AI to, others begin with the idea of a task they believe AI could be applied to and are then faced with the initial goal of acquiring data. There are several places to begin looking for relevant data:

- Experimental results: it's common to use AI methods on experimental data from your work or your lab's results.
- Web scraping: text, images and other forms of data may be available online
- Partnerships: partnering with other labs or organisations to share data can be an effective way to boost the amount of data you're working with.
- Data collection: volunteers or paid participants may be able to create the data that you require, e.g. asking for volunteers to participate in a study.
- Open source: there are many open source datasets available, which might work for your task. Many open source sets are ready split into test & training sets for you to use. You need to be careful of the licence and provenance with any open source dataset. 
- Synthetic: Generating synthetic data is an increasingly common way to create data.
- Data augmentation: creating noisy versions of your training data can be an effective way to boost the robustness of your models

For supervised learning, there’s also the challenge of obtaining accurate labels for the dataset. Sometimes the labels are inherently a part of the data, but other times it needs someone (researcher, volunteer, or paid participant) to spend time on labelling. Be prepared to spend significant time on labelling data if you are building up a new dataset for supervised learning. 




## Contact

If you can't find what you need

[CONTACT US :fontawesome-solid-paper-plane:](mailto:accelerate-mle@cst.cam.ac.uk){ .md-button }





