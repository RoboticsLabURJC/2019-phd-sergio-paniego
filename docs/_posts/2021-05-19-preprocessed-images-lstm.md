---
title: "Preprocessed images with and without memory (LSTMs)"
excerpt: "Preprocessed images experiments using basic NNs and LSTMs"


sidebar:
  nav: "docs"

categories:
- Behavior Studio
tags:
- detection brain
- LSTM



author: Sergio Paniego
pinned: false



---

During these previous weeks. More experiments have been conducted and new strategies have been discussed. 
With previous lessons learned, we have decided to try learn to drive giving some preprocess to the images so the network only needs to learn
directly from the important features how to drive. 

From a given raw image, a color filter is applied to extract the red line and after that, 4, 5 or 13 central points are extracted from that processed image.
This means that after the process, we have an array of 4, 5, 13 values corresponding to the center point of the red line on the image dividing the image in 4, 5 or 13 parts from 
the upper part down to the bottom.

After that we have even generated sequences of preprocessed images containing 2 or even 5 images and tested this approach against an LSTMs.

Experiments:
* [Results for 4, 5 and 13 points](#experiment-1)
* [Results for 13 points images using LSTMs](#experiment-2)

<a name="experiment-1"></a>
# 1. Results for 4, 5 and 13 points

More experiments need to be conducted but the general idea is that for 4, 5 points the performance is quite similar but 
when 13 points are added it's better. It's capable of completing all th circuits with 13 points but the Montmeló last curves.

<a name="experiment-2"></a>
# 2. Results for 13 points images using LSTMs

After this few experiments, LSTMs are introduced for the preprocessed images. In addition to preprocess the images, we have divided them
based on sequences of 2 and 5 images for training and testing. This means that me have to store previous images on a data structure during testing.
This operation is a bit more expensive and we start to have to consider additionally the Hz that the robot achieves on test time as a parameter. 

In this case, the robot is capable of finishing the simple circuit but in many curves and Montmeló it start to have issues on some turns.

