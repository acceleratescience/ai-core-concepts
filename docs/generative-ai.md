# Generative AI


## Learning Objectives

This section will help you understand:

- What generative AI is
- What foundation models are and the pros & cons of using them
- Some real-world examples of generative AI in research


## What is Generative AI?

Broadly speaking, generative AI refers to models that generate content, often in the form of images, text, video or audio, but increasingly combining several content types. In the sciences, there’s interest in generative AI in the design of new molecules and genetics studies.

![Generative AI](imgs/gen1.png){ align=center }

In many ways, generative AI is similar to supervised learning. The predictions that the models make are predictions about the content itself. You might hear the term _self-supervised_ to describe these models. This is because a person isn’t needed to label the data as the supervision signal is present within the data itself.

## Generative AI and Text


In the field of natural language processing (NLP), _transformer_ models have had a large impact. Generative AI in NLP uses the task of _language modelling_ - the task of predicting the next word in a sentence. This is a supervised learning task. Given a sequence of words, the model's goal is to predict the next word. It doesn’t require large amounts of effort to label the text data for training because “next word” is inherently there in the data. A language model is essentially a very powerful autocomplete model. Additional types of training are used to turn a basic language model from an autocomplete into an interactive chat model like ChatGPT.

What’s interesting about Generative AI models for NLP is that when trained on large amounts of data, they are able to do several tasks that they weren’t explicitly trained to do. For example, as their training data includes a large amount of multilingual training data, they are able to translate between languages. This is described as _zero shot learning_.

Text-based generative AI models typically are based on _transformer_ models (a kind of neural network) that was proposed in 2017. Transformer-based Large Language Models (LLMs) like ChatGPT are widely available and offer researchers varied capability such as literature search, writing, summarisation and other tasks related to science reporting. They are often used for assistance with writing code, a key part of many scientists’ workflows, and can potentially be used for assisting with data analysis and other research tasks. 




## Generative AI and Images

Generative AI models involving image generation tend to make use of _generative adversarial networks_ (GANs) or _diffusion models_. These are models that work by starting with images that consist of random noise, and iteratively denoising them to generate an image that matches a text description. These models find applications in scientific domains that deal with images, such as medical imaging. 

## Generative AI and Scientific Domains

While there’s been a lot of research into generative AI models for text and image, researchers are looking too at how generative AI can be used in other fields:

- In genetics, generative AI models have been used to generate new gene editors
- In Materials Science, diffusion models have been used to accelerate the discovery of new materials that can go on to be tested, e.g. in photovoltaics to find better materials for use in solar panels.
- In Medicine, generative AI is applied to identify novel drug candidates for specific diseases.
- In Climate Science, diffusion models are applied to weather forecasting, for more accurate forecasts


## Foundation Models

One driver of generative AI in the text and image domain is that there’s a large amount of training data for these content types widely available online, and it doesn’t need to be labelled. This means that organisations are able to build larger and larger models with massive training data sets.

Generative AI models are expensive to train, due to their large size and the large amount of training data. That means that only a handful of organisations can afford to build their own models from scratch. A typical way of working now is that these large ‘_foundation models_’, trained once by an organisation with the money and resources to do so, are then released publicly. Researchers can use the models directly, or _fine-tune_ them for their own projects with a small amount of data - far smaller than the amount of data that’s needed to build their own large model from scratch.

There are some considerations to take into account when using foundation models that have been trained by an outside organisation:

- For many public models, there are varying levels of openness. Often the model weights might be available, but details about the training set may not be public. This lack of transparency can make it difficult, as a researcher, to fully know how your AI model has been trained.
- If a model is hosted by an organisation behind an API, we cannot be sure what changes they are making, and that can affect reproducibility
- These models are typically trained on large amounts of data from the internet, which brings with it societal biases that become embedded in the model.
- There's a large environmental cost to using these models.



## Inspiration

Here are two papers that look at applications of some of these models:

- [An Interdisciplinary Outlook on Large Language Models for Scientific Research](https://arxiv.org/abs/2311.04929)
- [An Overview of Diffusion Models: Applications, Guided Generation, Statistical Rates and Optimization](https://arxiv.org/abs/2404.07771)

## More Resources

Generative AI is a fast moving field, and details such as how to evaluate these models are open research questions. Accelerate Science has two workshops related to generative AI, each with online material that you can work through at your own pace: 


- LLMs
- Diffusion Models


## Contact

If you can't find what you need

[CONTACT US :fontawesome-solid-paper-plane:](mailto:accelerate-mle@cst.cam.ac.uk){ .md-button }





