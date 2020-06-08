---
title: "PyTorch inferencer included"
excerpt: "This is an example of my first post"

sidebar:
  nav: "docs"

toc: true
toc_label: "TOC installation"
toc_icon: "cog"


categories:
- your category
tags:
- tag 1
- tag 2
- tag 3
- tag 4

author: Sergio Paniego
pinned: false
---

During this week, additional support for PyTorch in Detection Studio was given.

## PyTorch

[PyTorch](https://arxiv.org/abs/1912.01703) is a deep learning [framework](https://pytorch.org/)

[COMPLETE THIS PART]


## Support in Detection Studio

We gave support for PyTorch implementing a [python module](https://github.com/JdeRobot/DetectionStudio/blob/master/DetectionStudio/DetectionStudioLib/python_modules/pytorch_detect.py) 
that is connected to C++. Detection Studio is mainly implemented in C++, so it calls a python module.

A configuration file is needed for giving support to PyTorch. This file is read by Detection Studio to understand 
where the model is and which model is. 