---
title: "Network models testing"
excerpt: "Experiments with some of the most common object detection models are conducted."

sidebar:
  nav: "docs"

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

The Tensorflow models were downloaded from Tensorflow model zoo [[1]](https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/detection_model_zoo.md), where they offer a selections of models. 
The YOLOv3
weights and configuration were downloaded from the official documentation [[2]](https://pjreddie.com/darknet/yolo/) and the PyTorch model is included
in torchvision module [[3]](https://pytorch.org/docs/stable/torchvision/models.html). 

With this selection of models, some of the most common approaches in object detection were evaluated and even having 
different deep learning frameworks for some of them. This scenario shows that Detection Studio can help evaluating models 
from different approaches, different frameworks...

Additionally, the experiment was conducted on the same computer environment, to make things fair.

## References

[[1] Tensorflow model zoo](https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/detection_model_zoo.md)

[[2] YOLO website](https://pjreddie.com/darknet/yolo/)

[[3] Torchvision module](https://pytorch.org/docs/stable/torchvision/models.html)

