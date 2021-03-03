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
gallery5:
  - url: /assets/images/logbook/20210302/completed-distance-2.png
    image_path: /assets/images/logbook/20210302/completed-distance-2.png
    alt: "Completed distance"
gallery6:
  - url: /assets/images/logbook/20210302/completed-percentage-2.png
    image_path: /assets/images/logbook/20210302/completed-percentage-2.png
    alt: "Completed percentage"
gallery7:
  - url: /assets/images/logbook/20210302/circuit-diameter-2.png
    image_path: /assets/images/logbook/20210302/circuit-diameter-2.png
    alt: "Circuit diameter"
gallery8:
  - url: /assets/images/logbook/20210302/average-speed-2.png
    image_path: /assets/images/logbook/20210302/average-speed-2.png
    alt: "Average speed"
gallery9:
  - url: /assets/images/logbook/20210302/lap-seconds-2.png
    image_path: /assets/images/logbook/20210302/lap-seconds-2.png
    alt: "Lap seconds"
gallery10:
  - url: /assets/images/logbook/20210302/dataset-1.png
    image_path: /assets/images/logbook/20210302/dataset-1.png
    alt: "Dataset 1"
gallery11:
  - url: /assets/images/logbook/20210302/dataset-2.png
    image_path: /assets/images/logbook/20210302/dataset-2.png
    alt: "Dataset 1"
gallery12:
  - url: /assets/images/logbook/20210302/dataset-3.png
    image_path: /assets/images/logbook/20210302/dataset-3.png
    alt: "Dataset 1"
gallery13:
  - url: /assets/images/logbook/20210302/dataset-4.png
    image_path: /assets/images/logbook/20210302/dataset-4.png
    alt: "Dataset 1"
gallery14:
  - url: /assets/images/logbook/20210302/dataset-5.png
    image_path: /assets/images/logbook/20210302/dataset-5.png
    alt: "Dataset 1"
gallery15:
  - url: /assets/images/logbook/20210302/dataset-6.png
    image_path: /assets/images/logbook/20210302/dataset-6.png
    alt: "Dataset 1"

---

This week, the previous experiment results are improved using new approaches. 

Experiments:
* [Results for non-LSTM networks with extreme data](#experiment-1)
* [Results for LSTM networks with patched dataset](#experiment-2)
* [Results for best networks in new Montmelo circuit](#experiment-3)
* [Best networks results so far](#experiment-4)


<a name="experiment-1"></a>
# 1. Results for non-LSTM networks with extreme data

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

<a name="experiment-2"></a>
# 2. Results for LSTM networks with patched dataset

In new experiment the LSTM networks are trained with images without the red line, changing the color of those pixels to match
the rest of the floor. Below we can check some examples. 

{% include gallery id="gallery10" caption="" %}
{% include gallery id="gallery11" caption="" %}
{% include gallery id="gallery12" caption="" %}
{% include gallery id="gallery13" caption="" %}
{% include gallery id="gallery14" caption="" %}
{% include gallery id="gallery15" caption="" %}

If we look at the result of this experiment, we can say that the deepest still manages to learn how to drive but the Tinypilonet does not
perform well enough. The right part of the results is again the new experiment, the middle the previous one and the left is the explicit brain results.

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
# Results for best networks in new Montmeló circuit

A new circuit is added for the experiments, a simulation of the real F1 circuit Montmeló. 

**CIRCUIT IMAGE**

This is a circuit that is not present in the dataset so it can be used for real test. The many_curves circuit is part of the dataset
and the simple circuit is not directly part but a more complex design based on it is, so they both can be biased.

Montmeló circuit has some particularities, having some very difficult turns. Below are the results for all the best networks in this 
new circuit. 

**RESULTS**


<a name="experiment-4"></a>
# Best networks results so far

In this case, we saw a comparison of the best trained networks so far for each architecture. As we have studied, for LSTM, the networks trained
with a sequence dataset are so far the best ones. In the case of the non-LSTM networks, the ones trained on the dataset with extreme cases outperforms
the rest, so here we compare those side by side.

**RESULTS**

