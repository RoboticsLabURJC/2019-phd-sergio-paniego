---
title: "PyTorch inferencer included"
excerpt: "PyTorch framework support is included in Detection Studio."

sidebar:
  nav: "docs"

toc: true
toc_label: "TOC installation"
toc_icon: "cog"


categories:
- Detection Studio
tags:
- PyTorch
- object detection

author: Sergio Paniego
pinned: false
---

During this week, additional support for PyTorch in Detection Studio was given.

## PyTorch

[PyTorch](https://arxiv.org/abs/1912.01703) is one of the most used deep learning [frameworks](https://pytorch.org/) nowadays.

Some interesting parts extracted from PyTorch's paper that sum up the idea of the project:

> Deep learning frameworks have often focused on either usability or speed, but not both. PyTorch is a machine
learning library that shows that these two goals are in fact compatible: it provides an imperative and Pythonic
programming style that supports code as a model, makes debugging easy and is consistent with other popular scientific
computing libraries, while remaining efficient and supporting hardware accelerators such as GPUs.

> Many popular frameworks such as Caffe, CNTK, TensorFlow and Theano, construct a static dataflow
graph that represents the computation and which can then be applied repeatedly to batches of data.
This approach provides visibility into the whole computation ahead of time, and can theoretically
be leveraged to improve performance and scalability. However, it comes at the cost of ease of use,
ease of debugging, and flexibility of the types of computation that can be represented.


The core of the project is written in C++ but accessible from Python and closely integrated with it, to improve the overall performance.


## Support in Detection Studio

We gave support for PyTorch implementing a [python module](https://github.com/JdeRobot/DetectionStudio/blob/master/DetectionStudio/DetectionStudioLib/python_modules/pytorch_detect.py) 
that is connected to C++. Detection Studio is mainly implemented in C++, so it calls a python module.

A configuration file is needed for giving support to PyTorch. This file is read by Detection Studio to understand 
where the model is and which model is. 