---
title: "Improving previous experiments"
excerpt: "Taking last week's experiments and improving the results"

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
  - url: /assets/images/logbook/20210302/completed-distance-1.png
    image_path: /assets/images/logbook/20210302/completed-distance-1.png
    alt: "Completed distance"
gallery1:
  - url: /assets/images/logbook/20210302/completed-percentage-1.png
    image_path: /assets/images/logbook/20210302/completed-percentage-1.png
    alt: "Completed percentage"
gallery2:
  - url: /assets/images/logbook/20210302/circuit-diameter-1.png
    image_path: /assets/images/logbook/20210302/circuit-diameter-1.png
    alt: "Circuit diameter"
gallery3:
  - url: /assets/images/logbook/20210302/average-speed-1.png
    image_path: /assets/images/logbook/20210302/average-speed-1.png
    alt: "Average speed"
gallery4:
  - url: /assets/images/logbook/20210302/lap-seconds-1.png
    image_path: /assets/images/logbook/20210302/lap-seconds-1.png
    alt: "Lap seconds"

---

This week, the previous experiment results are improved using new approaches. 


# Results for non-LSTM networks with extreme data

In the previous blog, we saw that PilotNet and TinyPilotNet performance was ok and we improved their results with some small tricks. 
This week, we have tried to get rid of those tricks and instead go a step backward and focus on the dataset. We have decided
to train the non-LSTM networks with the full dataset instead of separating it as sequences, shuffling the images on the preprocess part and 
adding twice to the dataset some extreme cases. These extreme cases are examples where the W is high, looking for the network to focus more on 
curves.


Below are the results for these experiments, comparing them with last's weeks results for PilotNet and TinyPilotNet. On the right side, the new
experiments are located. In the middle, last's weeks experiments and on the left hand side the explicit brain results. 

As we can see, the improvements is clearly visible both for PilotNet and TinyPilotnet. They can now manage to complete the lap 
several times.

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

