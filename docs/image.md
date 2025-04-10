# Image Processing / Computer Vision


## Learning Objectives
This section will help you understand:

- What falls under the umbrella of Computer Vision (CV) 
- Some common Computer Vision tasks
- Examples of Computer Vision applied to scientific research


## What is Computer Vision?

Computer Vision (CV) is the umbrella term for techniques that are concerned with processing images and video. CV is a large domain, and there are many opportunities to use CV across a wide range of scientific disciplines. The field of CV has a long history making use of AI and machine learning techniques. In fact, one of the most popular introductory ML datasets you might come across is [MNIST](https://en.wikipedia.org/wiki/MNIST_database), a set of images of handwritten digits. Supervised and unsupervised learning have been applied across a range of image and video processing tasks.

When thinking of images, we usually imagine a photo taken with a camera. However, across the sciences, there are many other sources of image data in use such as X-rays, ultrasound, CT scans, satellite images, and electron microscopy. The same techniques that are applied to photos are often used for these other image formats. Hence, if you anticipate processing any form of image or video in your research, it can be valuable to look to the CV literature to understand what has previously been done. 

Key models that you might encounter in the computer vision field include:

- Convolutional Neural Networks (CNNs) have been used successfully for many years in computer vision, and convolutional blocks form the basis of many more complex models
- Vision Transformer (ViT) is used for image classification
- Generative Adversarial Networks (GANs) are used for image generation
- Autoencoders are used for denoising
- Diffusion models, which are a pipeline consisting of multiple model types, are used to generate images


## CV Tasks

Computer vision is widespread, and many CV tasks exist including:

- **Image classification**: classifying an image into one of several categories, e.g. classifying the handwritten digit in the MNIST task.
- **Image segmentation**: segmenting an image into different parts. For example, identifying boundaries of objects within an image. In a medical image this could also be something like identifying the boundaries of a tumour.
- **Image generation**: creating images from text descriptions, as is done by Stable Diffusion and Dall-E.
- **Denoising and enhancement**: removing noise from images and enhancing them.
- **Pose detection**: identifying the pose of the person (or animal) in an image.


## Examples of Computer Vision in Scientific Research

Examples of computer vision techniques applied to scientific research include:

- In Paleontology, classifying microfossils (that’s fossils <1mm in size) by their type. Microfossils are more abundant than their larger macrofossil counterparts, and can tell a lot about ecosystems of the past. 
- In medical imaging, segmenting a malignant mass from the rest of the image in an X-ray, Ultrasound image or CT scan.
- In Materials Science, for denoising and improving the resolution of electron microscopy images, making them easier to work with.
- In Veterinary Science, identifying the pose of animals in photographs can help with behavioural analysis.

!!! abstract "Case Study: Computer Vision in Neuroscience"

    <iframe width="1413" height="375" src="https://www.youtube.com/embed/68fQ7ZGTxAQ?list=PLbbha-3_S4YWkM-FXjZp8f5fNdV5z5D6B" title="Computer Vision in Neuroscience - Dr Samia Mohinta" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

    **Samia Mohinta**

    Computer vision provides a set of tools and techniques for interrogating different kinds of image data, including electron microscopy images that are relied on in neuroscience.

    Electron microscopy images of fruit fly brains look nothing like natural images, like photographs, that we are used to. Many computer vision algorithms are built to work on natural images, and so aren't directly applicable to these kind of images.

     So, scientists need to develop vision models that are specialised for electron microscope images. These models can do all same tasks of classification & segmentation as models for natural images. By identifying and segmenting neurons in these images, it's possible to map the structure and connection - i.e. the connectome - of these small brains. What we learn about fruit fly brains can then give us insight into our own human brains. 


## Contact

If you can't find what you need

[CONTACT US :fontawesome-solid-paper-plane:](mailto:accelerate-mle@cst.cam.ac.uk){ .md-button }





