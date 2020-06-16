---
title: "Object detection models review"
excerpt: "General review of object detection papers to improve the paper and the experiments."

sidebar:
  nav: "docs"

toc: true
toc_label: "TOC installation"
toc_icon: "cog"


categories:
- Detection Studio
tags:
- object detection model review
- yolo
- ssd
- faster r-cnn

author: Tony Stark
pinned: false
---

This week was dedicated to read papers and complete the state of the art part of the paper.
Papers were related to a general review of object detection models and the most important
model's papers

## Object detection model review

Object detection generic goal is finding objects in images and locating them. A general idea is that having an image, the algorithm
retrieves located bounding boxes with the object class for each object found in the image. A detailed explanation can be found in [[1]](https://arxiv.org/abs/1807.05511).
The broad variety of models based on deep learning can be divided in two main groups. The models which are based on a two-step approach and the one-step models. 

The two step approach generates region proposals in the first step and then in the second one classifies them.In this group, we can highlight Faster R-CNN [[2]](https://arxiv.org/abs/1506.01497).
It is divided in three stages: anchor generation, region proposal network and classifier and bounding box regressor.

he one step approach is based on regression and directly outputs the categories and locations for the objects in one step. Two important approaches in this group
are Single Shot MultiBox Detector[[3]](https://arxiv.org/abs/1512.02325) and You Only Look Once(YOLO) [[4]](https://arxiv.org/abs/1506.02640).
 YOLO gained popularity because it obtained a great time performance with good performance metrics, something that was previously difficult to achieve.
 This architecture has evolved to this days with YOLOv3[[5]](https://arxiv.org/abs/1804.02767) and YOLOv4[[6]](https://arxiv.org/abs/2004.10934) including several improvements over the first release.










