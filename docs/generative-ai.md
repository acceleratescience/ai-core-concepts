# Generative AI


## Learning Objectives

This section will help you understand:

- What generative AI is, and where you can use it
- What frontier or foundation models are and the pros & cons of using them
- Some real-world examples of generative AI in research


## Overview
Since 2017, there has been a lot of work in the area of generative AI. Broadly speaking, generative AI refers to models that generate content, usually in the form of images, text, video or audio.

![Generative AI](imgs/gen1.png){ align=center }

In many ways, generative AI is similar to supervised learning. The predictions that the models make are actually predictions about the content itself. You might hear the term _self-supervised_ to describe these models. This is because we don't need a person to label the data as the supervision signal is present within the data itself. 

One big difference between generative AI and more classic supervised learning is that the kind of content (image, text, audio etc.) that's popular for generative AI models is widely available online. This means that organisations can build larger and larger models with massive training data sets. 

Generative AI was spurred on recently by the introduction of the transformer model (a kind of neural network) in 2017, and more recent work in building large models. In the field of natural language processing (NLP), transformer models have had a huge impact. Generative AI in NLP uses the task of _language modelling_ - the task of predicting the next word in a sentence. This is a supervised learning task. Given a sequence of words, the model's goal is to predict the next word. It doesn’t require large amounts of effort to label the text data for training because “next word” is inherently there in the data. A language model is essentially a very powerful autocomplete model, but additional types of training is used to turn a basic language model into a chat model like ChatGPT. 

What’s interesting about Generative AI models for NLP is that when trained on large amounts of data, they are able to do several tasks that they weren’t explicitly trained to do. For example, with a large amount of multilingual training data, they are able to translate between languages. This is described as _zero shot learning_.

Tasks involving image and audio processing tend to make use of _diffusion models_ rather than transformers. 

## Frontier/Foundation Models

Generative AI models are expensive to train, due to their large size and the large amount of training data. There's a current trend of building larger and larger models. That means that only a handful of organisations can afford to build their own models from scratch. A typical way of working now is that these large ‘_foundation models_’ trained once by an organisation with the money and resources to do so, are then released publicly. Others can then use the models directly, or _fine-tune_ them for their own projects with a small amount of data - far smaller than the amount of data that’s needed to build their own large model from scratch.

There are some considerations to take into account when using foundation models:

- For many public models, there are varying levels of openness. Often the model weights might be available, but we might not know about the training data that was used. 
- If a model is hosted by an organisation behind an API, we cannot be sure what changes they are making, and that can affect reproducibility
- These models are typically trained on large amounts of data from the internet, which brings with it societal biases that become embedded in the model.
- There's a large environmental cost to using these models.


## Inspiration

Here are two papers that look at applications of some of these models:

- [An Interdisciplinary Outlook on Large Language Models for Scientific Research](https://arxiv.org/abs/2311.04929)
- [An Overview of Diffusion Models: Applications, Guided Generation, Statistical Rates and Optimization](https://arxiv.org/abs/2404.07771)

## More Resources

Accelerate Science has two workshops related to generative AI, each with online material that you can work through at your own pace:

- LLMs
- Diffusion Models


## Contact

If you can't find what you need

[CONTACT US :fontawesome-solid-paper-plane:](mailto:accelerate-mle@cst.cam.ac.uk){ .md-button }





