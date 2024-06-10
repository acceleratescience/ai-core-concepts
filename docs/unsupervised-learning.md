# Unsupervised Learning


## Learning Objectives

This section will help you understand:

- What unsupervised learning is, and where you can use it
- Unsupervised learning tasks including clustering, outlier detection and dimensionality reduction
- Some real-world examples of unsupervised learning in research

## Overview

Supervised learning is the most popular form of AI. However, supervised learning requires labelled data, which can be difficult or expensive to obtain. Most of the data in the world is unlabelled. Unsupervised learning helps us make sense of unstructured and unlabelled data.

Three common unsupervised algorithms are _clustering_, _dimensionality reduction_ and _anomaly detection_. 

**Clustering**

Clustering is the process of taking your data and arranging it into sub-groups, or clusters, that are sufficiently similar to each other. Unlike classification, where we know the groups ahead of time, clustering uncovers the structure of the groups in a larger population.

Suppose you have a library of photos of people. A clustering algorithm might group them into clusters that you hope would correspond to specific individuals. This is not unlike the processing that your phone's library might do. You cannot guarantee that this is the case, your phone might for example group two people together if they look similar, or split one person into two clusters based on something like their haircut. 

Other applications of clustering include: xxx

K-means is a popular clustering algorithm. You might have to give the number of clusters, or you might use a method to try and find the best fitting number of clusters.  


**Dimensionality reduction**

High dimensional data is hard to work with. It's hard to see, and also has an impact on the number of parameters your AI model might need to model the data. The more parameters you have, the larger model and more data you need. This is the _curse of dimensionality_.

Reducing the dimensionality of your data can be one way to work with this.

Can also help with visualisation, because we can project to 2- and 3-dimensions which we can view on a graph. 

**Anomaly Detection**

Tries to figure out if an example is an anomaly, and doesn't fit with the rest of the set. 

For example, identifying a fraudulent bank transaction because it doesn't fit with your other transactions. 



## Inspiration

Find more examples of research using unsupervised learning on Accelerate's blog:

- [Ema Bauzyte discusses using unsupervised learning to cluster sites in archeology, get more insight about which might be related](https://acceleratescience.github.io/accelerate-spark%20data%20science%20residency/2021/06/10/EmBauztye-ML-for-archeology.html)
- [Jesse Allardice uses dimensionality reduction in Physics, to reduce the complexity of high dimensional data for solar panels](https://acceleratescience.github.io/accelerate-spark%20data%20science%20residency/2021/07/08/JesseAllardice-ML-for-solar-tech.html)
- [Dr Romit Samanta groups patients to better identify subgroups of patients and understand how their biology relates to disease progression](https://acceleratescience.github.io/2022/05/17/how-can-we-use-ai-to-understand-acute-respiratory-distress-syndrome.html)

## Contact

If you can't find what you need

[CONTACT US :fontawesome-solid-paper-plane:](mailto:accelerate-mle@cst.cam.ac.uk){ .md-button }





