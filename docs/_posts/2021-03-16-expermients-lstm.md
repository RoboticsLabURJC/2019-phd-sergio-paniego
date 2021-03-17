---
title: "Exploring data augmentation for LSTMs"
excerpt: "Exploring data augmentation for LSTMs"


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
  - url: /assets/images/logbook/20210316/completed-distance-1.png
    image_path: /assets/images/logbook/20210316/completed-distance-1.png
    alt: "Completed distance"
gallery1:
  - url: /assets/images/logbook/20210316/completed-percentage-1.png
    image_path: /assets/images/logbook/20210316/completed-percentage-1.png
    alt: "Completed percentage"
gallery2:
  - url: /assets/images/logbook/20210316/circuit-diameter-1.png
    image_path: /assets/images/logbook/20210316/circuit-diameter-1.png
    alt: "Circuit diameter"
gallery3:
  - url: /assets/images/logbook/20210316/average-speed-1.png
    image_path: /assets/images/logbook/20210316/average-speed-1.png
    alt: "Average speed"
gallery4:
  - url: /assets/images/logbook/20210316/lap-seconds-1.png
    image_path: /assets/images/logbook/20210316/lap-seconds-1.png
    alt: "Lap seconds"
gallery5:
  - url: /assets/images/logbook/20210316/completed-distance-2.png
    image_path: /assets/images/logbook/20210316/completed-distance-2.png
    alt: "Completed distance"
gallery6:
  - url: /assets/images/logbook/20210316/completed-percentage-2.png
    image_path: /assets/images/logbook/20210316/completed-percentage-2.png
    alt: "Completed percentage"
gallery7:
  - url: /assets/images/logbook/20210316/circuit-diameter-2.png
    image_path: /assets/images/logbook/20210316/circuit-diameter-2.png
    alt: "Circuit diameter"
gallery8:
  - url: /assets/images/logbook/20210316/average-speed-2.png
    image_path: /assets/images/logbook/20210316/average-speed-2.png
    alt: "Average speed"
gallery9:
  - url: /assets/images/logbook/20210316/lap-seconds-2.png
    image_path: /assets/images/logbook/20210316/lap-seconds-2.png
    alt: "Lap seconds"
gallery10:
  - url: /assets/images/logbook/20210316/completed-distance-3.png
    image_path: /assets/images/logbook/20210316/completed-distance-3.png
    alt: "Completed distance"
gallery11:
  - url: /assets/images/logbook/20210316/completed-percentage-3.png
    image_path: /assets/images/logbook/20210316/completed-percentage-3.png
    alt: "Completed percentage"
gallery12:
  - url: /assets/images/logbook/20210316/circuit-diameter-3.png
    image_path: /assets/images/logbook/20210316/circuit-diameter-3.png
    alt: "Circuit diameter"
gallery13:
  - url: /assets/images/logbook/20210316/average-speed-3.png
    image_path: /assets/images/logbook/20210316/average-speed-3.png
    alt: "Average speed"
gallery14:
  - url: /assets/images/logbook/20210316/lap-seconds-3.png
    image_path: /assets/images/logbook/20210316/lap-seconds-3.png
    alt: "Lap seconds"


---

New experiments this week.

Experiments:
* [Results for different data augmentation strategies](#experiment-1)
* [Results for different data augmentation strategies only in Montmeló](#experiment-2)
* [Results for LeNet classification](#experiment-3)

<a name="experiment-1"></a>
# 1. Results for different data augmentation strategies

In the experiment, different data augmentation strategies are explored only using Deepest LSTM Pilotnet architecture. This experiment 
started in the last section of last week's blog and here are the results of all the different strategies. 
These experiments are:

* Remove moderate data from the dataset. Data sequences with a majority of low turn values are removed.
* Add extreme sequences twice to the dataset. 
* Add extreme sequences twice and remove moderate sequences. 
* Add patched images to the dataset. The image red line is removed and added to the dataset.
* Add gaussian noise to the dataset. 

In this case, the results show that they still can't complete the Montmeló circuit but most of then can complete the rest of the scenarios.

*Click on the images to expand them.*

## Completed distance

{% include gallery id="gallery" caption="" %}

## Completed percentage
{% include gallery id="gallery1" caption="" %}

## Circuit diameter
{% include gallery id="gallery2" caption="" %}

## Average speed
{% include gallery id="gallery3" caption="" %}

## Lap seconds
{% include gallery id="gallery4" caption="" %}


<a name="experiment-2"></a>
# 2. Results for different data augmentation strategies only in Montmeló

More experiments for the same nets in Montmeló. In this case, we can see that the network trained with gaussian noise data augmentation is the 
best one even completing the circuit once. It is the only regression based network that has completed the circuit so far. It's also important
to consider that the experiments start on a random position and rotation in the circuit.

## Completed distance

{% include gallery id="gallery5" caption="" %}

## Completed percentage
{% include gallery id="gallery6" caption="" %}

## Circuit diameter
{% include gallery id="gallery7" caption="" %}

## Average speed
{% include gallery id="gallery8" caption="" %}

## Lap seconds
{% include gallery id="gallery9" caption="" %}


<a name="experiment-3"></a>
# 3. Results for LeNet classification

For this experiment, we have considered the famous [LeNet](http://yann.lecun.com/exdb/publis/pdf/lecun-98.pdf) architecture from Yann Lecun et al.
This architecture accepted 32x32 B/W images as input and has 90000 parameters in it's LeNet-5 structure. The number of parameters in the case of B/W images is
comparable to the Deepest LSTM one, so we tested it's performance to have a *fair* comparison. We have 2 new networks in this case, one accepting B/W images (we transform the 
dataset to make it suitable for this scenario) and other accepting color images (RGB). The experiments show that even this classification networks can complete the different 
circuits (even Montmeló).


## Completed distance

{% include gallery id="gallery10" caption="" %}

## Completed percentage
{% include gallery id="gallery11" caption="" %}

## Circuit diameter
{% include gallery id="gallery12" caption="" %}

## Average speed
{% include gallery id="gallery13" caption="" %}

## Lap seconds
{% include gallery id="gallery14" caption="" %}

