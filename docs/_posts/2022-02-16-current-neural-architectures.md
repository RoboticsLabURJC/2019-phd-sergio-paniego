---
title: "Review of current neural architectures used"
excerpt: "Reviewing current neural architectures to set the base fot following steps."


sidebar:
  nav: "docs"

categories:
- Neural networks
tags:
- Neural network
- Architectures

author: Sergio Paniego
pinned: false



gallery:
  - url: /assets/images/logbook/20220216/pilotnet.png
    image_path: /assets/images/logbook/20220216/pilotnet.png
    alt: "Pilotnet architecture"
gallery1:
  - url: /assets/images/logbook/20220216/deepest-lstm-tinypilotnet.png
    image_path: /assets/images/logbook/20220216/deepest-lstm-tinypilotnet.png
    alt: "Deepest LSTM TinyPilotnet architecture"
gallery2:
  - url: /assets/images/logbook/20220216/pilotnet3d.png
    image_path: /assets/images/logbook/20220216/pilotnet3d.png
    alt: "Pilotnet3D architecture"
gallery3:
  - url: /assets/images/logbook/20220216/deepest-lstm-tinypilotnet-3d.png
    image_path: /assets/images/logbook/20220216/deepest-lstm-tinypilotnet-3d.png
    alt: "Deepest LSTM TinyPilotnet 3D architecture"

---

These are the current 4 neural approaches explored for controlling the robot.

# Pilotnet

{% include gallery id="gallery" caption="Pilotnet rachitecture" %}

* BatchNorm
* Conv2D x 5
* Flatten
* Dense x 5

# Deepest LSTM TinyPilotnet

{% include gallery id="gallery1" caption="Deepest LSTM TinyPilotnet" %}

* Conv2D * 3
* Dropout
* Reshape
* ConvLSTM * 3
* Flatten
* Dense * 3


# Pilotnet 3D (with memory)

{% include gallery id="gallery2" caption="Pilotnet rachitecture 3D (with memory)" %}

* BatchNorm
* Conv3D x 5
* Flatten
* Dense x 5

# Deepest LSTM TinyPilotnet 3D (with memory)

{% include gallery id="gallery3" caption="Deepest LSTM TinyPilotnet 3D (with memory)" %}

* TimeDistributed(Conv2D) * 3
* Dropout
* Reshape
* ConvLSTM * 3
* Flatten
* Dense * 3
