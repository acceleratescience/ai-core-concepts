# Unsupervised Learning


## Learning Objectives

This section will help you understand:

- What unsupervised learning is, and where you can use it
- Unsupervised learning tasks including clustering, outlier detection and dimensionality reduction
- Some real-world examples of unsupervised learning in research

## Overview

Supervised learning is the most popular form of AI. However, supervised learning requires labelled data, which can be difficult or expensive to obtain. Most of the data in the world is unlabelled. Unsupervised learning helps us make sense of unstructured and unlabelled data.

Three common unsupervised algorithms are _clustering_, _dimensionality reduction_ and _anomaly detection_.

## Unsupervised Learning Algorithms

**Clustering**

Clustering is the process of taking your data and discovering sub-groups, or clusters, that are sufficiently similar to each other. Unlike classification in supervised learning, where we know the groups ahead of time, clustering uncovers the structure of the groups in a larger population.

Suppose you're working with medical data. You know that some groups of people respond differently to treatment than others, but you don't know the factors that lead here. A clustering algorithm might group your participants into different clusters that allow you to explain what's going on. 

Other places that people have used clustering include uncovering structure in archeological data, clustering sounds and speakers together, identifying sub-groups of study participants etc. 

K-means and DBSCAN are popular clustering algorithms. You may need to give the number of clusters before running the clustering algorithm, or you might use an automated method to try and find which number of clusters best fits the data. 


**Dimensionality reduction**

High dimensional data is hard to work with. The first thing we usually notice is that it's hard to visualise well, so that you can explore what the data looks like. A high number of dimensions also imacts the number of parameters your AI model needs to model the data. The more parameters a model has, the larger model and more data you need. This is the _curse of dimensionality_.

Reducing the dimensionality of your data can be one way to work with it effectively. Projecting down to 2- or 3-dimensions means that you can plot it on a graph to view. 


Principal Component Analysis (PCA), [t-SNE](https://distill.pub/2016/misread-tsne/), and [UMAP](https://pair-code.github.io/understanding-umap/) are popular dimensionality reduction algorithms that you might see used. 

**Anomaly Detection**

Anomoly detection is identifying anomolous or rare examples in a dataset, that are inconsistent with the rest of the dataset.

Examples of this might be in identifying fraudulent and unusual bank transactions, or identifying unusual behaviour that might be a cybersecurity threat. 


## Inspiration

Find more examples of research using unsupervised learning on Accelerate's blog:

- [Ema Bauzyte discusses using unsupervised learning to cluster sites in archeology, get more insight about which might be related](https://acceleratescience.github.io/accelerate-spark%20data%20science%20residency/2021/06/10/EmBauztye-ML-for-archeology.html)
- [Jesse Allardice uses dimensionality reduction in Physics, to reduce the complexity of high dimensional data for solar panels](https://acceleratescience.github.io/accelerate-spark%20data%20science%20residency/2021/07/08/JesseAllardice-ML-for-solar-tech.html)
- [Dr Romit Samanta groups patients to better identify subgroups of patients and understand how their biology relates to disease progression](https://acceleratescience.github.io/2022/05/17/how-can-we-use-ai-to-understand-acute-respiratory-distress-syndrome.html)

## Contact

If you can't find what you need

[CONTACT US :fontawesome-solid-paper-plane:](mailto:accelerate-mle@cst.cam.ac.uk){ .md-button }





