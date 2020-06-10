---
title: "OpenCV-Yolov3 inferencer included"
excerpt: "OpenCV-Yolov3 support is included in Detection Studio, getting rid of darknet framework dependency."

sidebar:
  nav: "docs"

toc: true
toc_label: "TOC installation"
toc_icon: "cog"


categories:
- Detection Studio
tags:
- YOLO
- OpenCV
- darknet
- object detection

author: Sergio Paniego
pinned: false
---

During this week, we finally came with a solution to a problem that had been long wih us. In [Detection Studio](https://github.com/JdeRobot/DetectionStudio)
we provide support to different deep learning frameworks. One of them is [darknet](https://pjreddie.com/darknet/). We only had support to YOLO versions v1 and v2, but YOLOv3 
was already available. So we wanted to give it also support. In this post, we will be exploring YOLO & darknet, the problem that we had in project
and the solution we finally developed.

## YOLO and darknet

[YOLO](https://arxiv.org/abs/1506.02640) is one of the most famous object detection approaches that has appeared in recent years. It's a one-step approach, 
based on regression/classification, as for example SSD. From the input of the image to the result of the different bonding boxes with class probabilities, there is only one step. 


![YOL_architecture](https://miro.medium.com/max/1148/1*15uBgdR3_rNZzx665Leang.jpeg)

The image is divided in to a grid of SxS. For each cell, bounding boxes are proposed. After this bounding boxes are generated, 
they are classified and regressed, until the final bounding boxes are generated. A single loss function is use to minimize the
classification and location error. The idea of having just one-step increased the FPS without lossing too much accuracy. This has also
been one of the most interesting points about YOLO.

This approach has been improved including different novel ideas and ideas from other papers generating YOLOv2, [YOLOv3](https://pjreddie.com/media/files/papers/YOLOv3.pdf)
 and finally [YOLOv4](https://arxiv.org/abs/2004.10934), which came out early this year.
 
 With this approach, a novel deep learning framework was also proposed, darknet, written in C. Using this framework, YOLO was developed


## Problem

We had support in Detection Studio for a previous darknet version which supported YOLOv2, but we needed an update.
We tried for some time to add support for official darknet YOLOv3 in Detection Studio, but after some time we decided to get rid of 
this dependency, because a we found that this support could be given by OpenCV

## Solution

[OpenCV-darnet](https://www.pyimagesearch.com/2020/02/03/how-to-use-opencvs-dnn-module-with-nvidia-gpus-cuda-and-cudnn/), gives support to darknet 
with [GPU](https://www.pyimagesearch.com/2020/02/03/how-to-use-opencvs-dnn-module-with-nvidia-gpus-cuda-and-cudnn/), even supporting CUDA. We added this support to 
Detection Studio, removing the official darknet but still giving support to this framework. We removed one dependency, since we already used OpenCV. The inference
time of this implementation were great thanks to the CUDA support so we implemented this solution!