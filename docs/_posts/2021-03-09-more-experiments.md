---
title: "More experiments adding classification and extreme sequence data for LSTM models"
excerpt: "More experiments with a new classification model and extreme data for the LSTM based models"


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
  - url: /assets/images/logbook/20210309/completed-distance-1.png
    image_path: /assets/images/logbook/20210309/completed-distance-1.png
    alt: "Completed distance"
gallery1:
  - url: /assets/images/logbook/20210309/completed-percentage-1.png
    image_path: /assets/images/logbook/20210309/completed-percentage-1.png
    alt: "Completed percentage"
gallery2:
  - url: /assets/images/logbook/20210309/circuit-diameter-1.png
    image_path: /assets/images/logbook/20210309/circuit-diameter-1.png
    alt: "Circuit diameter"
gallery3:
  - url: /assets/images/logbook/20210309/average-speed-1.png
    image_path: /assets/images/logbook/20210309/average-speed-1.png
    alt: "Average speed"
gallery4:
  - url: /assets/images/logbook/20210309/lap-seconds-1.png
    image_path: /assets/images/logbook/20210309/lap-seconds-1.png
    alt: "Lap seconds"
gallery5:
  - url: /assets/images/logbook/20210309/completed-distance-2.png
    image_path: /assets/images/logbook/20210309/completed-distance-2.png
    alt: "Completed distance"
gallery6:
  - url: /assets/images/logbook/20210309/completed-percentage-2.png
    image_path: /assets/images/logbook/20210309/completed-percentage-2.png
    alt: "Completed percentage"
gallery7:
  - url: /assets/images/logbook/20210309/circuit-diameter-2.png
    image_path: /assets/images/logbook/20210309/circuit-diameter-2.png
    alt: "Circuit diameter"
gallery8:
  - url: /assets/images/logbook/20210309/average-speed-2.png
    image_path: /assets/images/logbook/20210309/average-speed-2.png
    alt: "Average speed"
gallery9:
  - url: /assets/images/logbook/20210309/lap-seconds-2.png
    image_path: /assets/images/logbook/20210309/lap-seconds-2.png
    alt: "Lap seconds"

---

New experiments this week.

Experiments:
* [Results for classification brain with extreme data](#experiment-1)
* [Comparison of best brains for each architecture](#experiment-2)


<a name="experiment-1"></a>
# 1. Results for classification brain with extreme data

Adding more diversity to the brains that we have used, we add a classification brain. Its architecture is based on a Smaller 
VGG network that is trained with the same dataset as the rest of the regression based architectures. For this new scenario, the different 
values in the dataset are classified in different categories. 4 categories for the V and 7 for the W. Additionally, extreme data is added taking 
into consideration for this purpose the extreme cases of W, radically_left turns of radically_right turns, replicating them in the dataset generating 
a bias towards those values which are scarce. The results show that this brain is able to complete the different circuits in more or less the same
time and interpreting the differences in time to the classification schema chosen. 



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
# 2. Comparison of best brains for each architecture

Complete comparison until now of the best trained models for each architecture. The brains generally can complete the 
different circuits except for the Montmelo one. The only one that manages to complete a full lap in Montmelo is the classification
brain. 

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



