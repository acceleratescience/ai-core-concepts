# What is AI?

## Learning Objectives
This section will help you understand:

- What AI is and where it is used
- Some different definitions of AI and related terms

## Overview
**Artificial Intelligence (AI)** is an umbrella term. Usually it’s thought of as something like imitating human intelligence. AI systems are used to automate decision making in tasks that typically need some level of intelligence to perform.

**Machine Learning (ML)** is a set of algorithms that learn their behaviour from data. This is in contrast to more traditional computer programming that spells out the rules that a computer must follow. When people talk about AI today, they're almost always talking about machine learning. All of the recent progress in the field of AI has been in machine learning, and particularly in a specific type of machine learning called deep learning.

There are 4 broad categories of ML that this course will explore:

* Supervised Learning: The model is trained on labelled data to make predictions or classify new data, such as predicting disease from medical images.
* Unsupervised Learning: Uncovers structure, patterns and relationships in unstructured and unlabelled data, such as identifying clusters of cells based on their gene expression in genomics.
* Reinforcement Learning: Builds agents that learn to take actions in uncertain and changing environments, such as controlling robot automation in the lab.
* Generative AI: The model creates new content, such as identifying new molecular structures in drug discovery. 

The course will explore each of these areas and how they are being applied in AI for science projects.


## What is AI?
AI models are built to tackle specific **tasks**. A task is something specific that a model might do such as:

* Make a decision about whether an email is spam or not
* Identify people in images
* Translate text from one language into another
* Automatically transcribe speech
* Identify supernovae in Astrophysics data
* Predict whether an X-ray shows a cancerous mass
* Predict the toxicity of a chemical compound
* Classify the type of cell from gene expression data
* Identify scientific papers that are close in topic to each other

Tasks usually have **datasets** associated with them. A dataset is essentially lots of examples of that task. For example, a spam email detection dataset would consist of many emails. A speech recognition dataset would consist of audio of people speaking. A medical image dataset would consist of many examples of medical images.

A dataset might have **labels** (or annotations), which are the correct answer, for each item in the dataset. The emails in your spam email dataset would have labels marking each email as spam or not. The audio files in your speech recognition dataset would have accurate transcriptions of the words spoken. The medical images dataset might contain information about suspicious masses in the images. These labels are often created by people who manually go through the dataset and annotate each example.

Many popular AI tasks have open source datasets that are available to use. Though, depending on the existing research in your field, you might need to acquire your own dataset.

An ML **model** is trained to perform a task, using one or more datasets. The training process updates the model’s **parameters**. These are the set of numbers inside the model which are learnt from data. The model is usually the artefact that's the result of your experimentation, and it can be used again and again on new data.

Under the umbrella of ML, there are many different algorithms. Deep Learning, or **Deep Neural Networks**, are popular today because they’ve been successful at a range of different tasks. There are many other algorithms though, some of which may be more suitable for your data.

You need to **evaluate** the performance of your model based on a subset of your data, to judge how well your model achieves the task. 

## AI for Scientific Research

Researchers across disciplines are exploring the application of AI to data and tasks in their own domains. AI is being used across the entire scientific research lifecycle:

* Speeding up literature review, by using text processing techniques to sift through large amounts of scientific text.
* Hypothesis generation, by uncovering relationships and patterns that may not be immediately apparent to human researchers.
* Data analysis, by identifying patterns in data
* Simulation and modelling, by simulating complex processes & providing insights into phenomena that are difficult or impossible to study experimentally.
*Writing assistant, by helping suggest ways to write scientific findings.

The following sections dive into different types of AI algorithms and highlight how they work in scientific research, along with some of their limitations.
