---
title: "Paper writing, documentation update and RetinaNet reading"
excerpt: "The paper is completed and RetinaNet paper is read."

sidebar:
  nav: "docs"


categories:
- Detection Studio
tags:
- paper
- RetinaNet

author: Sergio Paniego
pinned: false
---

Week dedicated to finish writing the paper and reading more papers. The paper in general was updated, reviewing each section
and updating figures. The documentation was also reviewed. 

## RetinaNet
RetinaNet [[1]](https://arxiv.org/abs/1708.02002) paper is a new approach in object detection. It discusses the problems of one-step 
approaches and proposes improvements that are reflected in RetinaNet. A new loss function is proposed and class imbalance during training
is identified as one of the main problems of one-stage detectors. This means that they evaluate 10^4-10^5 candidate locations but
the amount of objects is low. The new loss function pays less importance to *easy objects*, those that are not difficult to be found and classify correctly.

## References

[[1] Tsung-Yi Lin, Priya Goyal, Ross Girshick, Kaiming He, Piotr Dollár, Focal Loss for Dense Object Detection, 2018](https://arxiv.org/abs/1708.02002)

