---
title: "Network models testing"
excerpt: "Experiments with some of the most common object detection models are conducted."

sidebar:
  nav: "docs"

toc: true
toc_label: "TOC installation"
toc_icon: "cog"


categories:
- Detection Studio
tags:
- object detection
- experiment
- paper
- framework

author: Sergio Paniego
pinned: false
---

This week was dedicated to complete the experiments part in Detection Studio paper.

## Experiment explanation

This experiment idea is to show how you can use Detection Studio to compare different object detection models
and understand which one has a better performance. To do so, several object detection models implementing common approaches
were used. The models are: 

* SSD Inception v2 implemented in TensorFlow.
* Faster RCNN Resnet 101 implemented in TensorFlow.
* YOLOv3 implemented in darknet.
* Faster RCNN Resnet 50 FPN implemented in PyTorch.

The Tensorflow models were downloaded from [Tensorflow model zoo](), where they offer a selections of models. The YOLOv3
weights and configuration were downloaded from the [official documentation]() and the PyTorch model is included
in torchvision module. 

With this selection of models, some of the most common approaches in object detection were evaluated and even having 
different deep learning frameworks for some of them. This scenario shows that Detection Studio can help evaluating models 
from different approaches, different frameworks...

Additionally, the experiment was conducted on the same computer environment, to make things fair.




