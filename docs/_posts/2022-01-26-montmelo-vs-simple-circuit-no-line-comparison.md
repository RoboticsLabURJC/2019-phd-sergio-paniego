---
title: "Montmeló vs simple circuit no red line comparison fot all the brains"
excerpt: "Comparing all the different brains developed on two circuits"


sidebar:
  nav: "docs"

categories:
- Behavior Studio
tags:
- comparison
- Metrics



author: Sergio Paniego
pinned: false

gallery:
  - url: /assets/images/logbook/20220126/completed_distance_comparison.png
    image_path: /assets/images/logbook/20220126/completed_distance_comparison.png
    alt: "Completed distance comparison"
gallery1:
  - url: /assets/images/logbook/20220126/completed_percentage_comparison.png
    image_path: /assets/images/logbook/20220126/completed_percentage_comparison.png
    alt: "Completed percentage comparison"
gallery2:
  - url: /assets/images/logbook/20220126/position_deviation_comparison.png
    image_path: /assets/images/logbook/20220126/position_deviation_comparison.png
    alt: "Position deviation comparison"
gallery3:
  - url: /assets/images/logbook/20220126/lap_seconds_comparison.png
    image_path: /assets/images/logbook/20220126/lap_seconds_comparison.png
    alt: "Lap seconds comparison"

---

In this case, the comparison is between the 5 different brain approaches that we have used during the past few months.

The different brains are:


* PID controller
* **NO MEMORY** Pilotnet brain (CNN based)
* **IMPLICIT MEMORY** Deepest LSTM Tinypilonet (CNN+LSTM with 1 image as input for each timestep)
* **EXPLICIT MEMORY** Pilotnet with 3DCNN (3 images as input for each timestep with 3DCNN)
* **EXPLICIT MEMORY** Deepest LSTM Tinypilotnet with 3 image-input (3 images as input for each timestep)

We compare these brain on 2 different circuits that should be enough to show differences: Montmeló with red line and the simple
circuit without the red line. The first one is the circuit with difficult turns and the second one has a special feature, we have removed the
red line from it. Since the dataset we have used for training has the red line, it's interesting to show if the brains generalise to worlds
without the red line. 


We expect the brains with memory to be better on some aspects to the rest of the brains. 

The results show that all the brains are capable of finishing Montmeló except for the Deepest LSTM Tinypilotnet with 3 image-input. This should be related with a
problem on the architecture of the brain or its capabilities. 

Considering the second circuit, we start to see the differences. The first brain is not able to even start driving, since it expects a red line that is missing. This 
is actually the worse brain, since it's only capable of running on a very specific scenario.

The second and third brains are not able to complete the circuit, but the third one is still able to complete some part of the circuit. This could be related to the memory 
capabilities that Pilotnet misses.

Pilotnet with 3dCNN is able to complete the simple circuit even without the red line that was not on the dataset. It receives 3 images as input. The seconds per lap are a bit higher 
but that's completely normal.

The fourth brain again shows a great struggle on this circuit and fails miserably.

{% include gallery id="gallery" caption="Completed distance comparison" %}

{% include gallery id="gallery1" caption="Completed percentage comparison" %}

{% include gallery id="gallery3" caption="Completed distance comparison" %}


With this post, we start to understand the differences of using a neural network based approach against a PID controller and a brain without memory against one that actually has some kind of memory.