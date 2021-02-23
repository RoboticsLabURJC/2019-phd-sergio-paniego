---
title: "Learning to drive with deep learning. Experiments with 4 types of nets and comparison"
excerpt: "Current state of the project and experiments made"

sidebar:
  nav: "docs"

categories:
- Behavior Studio
tags:
- detection brain
- LSTM
- PilotNet
- TinyPilotNet


author: Sergio Paniego
pinned: false

gallery:
  - url: /assets/images/logbook/20210223/pilotnet-architecture.png
    image_path: /assets/images/logbook/20210223/pilotnet-architecture.png
    alt: "PilotNet architecture"
gallery2:
  - url: /assets/images/logbook/20210223/train-set.png
    image_path: /assets/images/logbook/20210223/train-set.png
    alt: "Train set"
gallery3:
  - url: /assets/images/logbook/20210223/val-set.png
    image_path: /assets/images/logbook/20210223/val-set.png
    alt: "Val set"
gallery4:
  - url: /assets/images/logbook/20210223/deepest-stats.png
    image_path: /assets/images/logbook/20210223/deepest-stats.png
    alt: "Deepest stats"
gallery5:
  - url: /assets/images/logbook/20210223/tiny-lstm-stats.png
    image_path: /assets/images/logbook/20210223/tiny-lstm-stats.png
    alt: "TinyLSTM stats"
gallery6:
  - url: /assets/images/logbook/20210223/tiny-stats.png
    image_path: /assets/images/logbook/20210223/tiny-stats.png
    alt: "Tiny stats"
gallery7:
  - url: /assets/images/logbook/20210223/pilotnet-stats.png
    image_path: /assets/images/logbook/20210223/pilotnet-stats.png
    alt: "PilotNet stats"
    
---

In this blogpost, I will sum up the last weeks (months) of work in this project. Many improvements have been made and my 
general knowledge of this huge area is now broader but still quite small. 

# Introduction

For this problem, we would like to generate a brain that learns to drive the circuits that we have autonomously. The brain
will need to learn to generate two outputs, the speed V and the rotation W. For this purpose, we have a dataset consisting of images
with annotations V, W generated from an explicit brain.

# Brains

4 approaches are explored, all of them from the literature. We select previous brains used in the literature because in this phase we
are only learning concepts and we are not trying to outperform the state of the art (probably that will be covered some time soon :)). 

## PilotNet

The first brain comes from two papers [1](https://arxiv.org/abs/1604.07316) [2](https://arxiv.org/abs/1704.07911) proposed by Nvidia. In these papers
they present a deep learning architecture called PilotNet based on a CNN that learns to drive using data from a real environment. Our case is much simpler, 
so this network could be a good start point to learn the concepts.

This model has 12000000 params. 

{% include gallery id="gallery" caption="" %}



## TinyPilotNet

This network and teh following ones come from the paper *Self-driving a Car in Simulation Through a CNN*. They present different approaches to improve the PilotNet
architecture for autonomous driving using a smaller network (this case) or more advance concepts like LSTMs nodes (the following brains).

This architecture takes the same ideas from PilotNet but making the network simpler and smaller.
This model has 220000 params. 

## TinyPilonetNet LSTM

In this architecture, the ideas from the previous architecture are used combined with an LSTM node to learn temporal dependencies. This could make sense for the problem
of autonomously driving because previous steps in time are sometime useful for current predictions (imagine taking a curve).
This model has 920000 params. 

## Deepest TinypilotNet LSTM

Finally, the most complex network is also based on the previous one, but adding more LSTM layers to make ir deeper and learn more temporal dependencies. 
This model has 86000 params. 

# Dataset

Considering the problem that we are trying to solve, we elaborated a dataset consisting of images and V-W pais predictions. This dataset comes from a variate set of 
circuits in both directions with an explicit brain. Since we have several sequences and we would like to learn temporal dependencies, we have to take this into account 
when preprocessing the data that is fed into the networks. If we want the LSTMs to learn temporal dependencies, the images should come as a sequence. 

For this purpose, the data is divided into sequences that are then mixed and separated into train-val sets. Below are the distributions of 
data for the W value for the train and val sets.

{% include gallery id="gallery2" caption="" %}
{% include gallery id="gallery3" caption="" %}

# Training

We train all of the networks with the same criteria in order to make the comparison as fair as possible. Each architecture
is trained 300 epochs with batches of 50 examples. The 300 epochs are more than enough to over fit the data. On this stage that is not a problem
since we are only learning concepts and the goal is to generate brains that learn to drive. 

{% include gallery id="gallery4" caption="" %}
{% include gallery id="gallery5" caption="" %}
{% include gallery id="gallery6" caption="" %}
{% include gallery id="gallery7" caption="" %}

# Results in test circuit



