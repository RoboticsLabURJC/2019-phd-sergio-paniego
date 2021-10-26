---
title: "New position deviation calculation"
excerpt: "New position deviation calculation"


sidebar:
  nav: "docs"

categories:
- Behavior Studio
tags:
- Deepest LSTM TinyPilotNet
- Pilotnet
- comparison
- Metrics



author: Sergio Paniego
pinned: false

gallery:
  - url: /assets/images/logbook/20211026/completed_distance.png
    image_path: /assets/images/logbook/20211026/completed_distance.png
    alt: "Completed distance"
gallery1:
  - url: /assets/images/logbook/20211026/completed_percentage.png
    image_path: /assets/images/logbook/20211026/completed_percentage.png
    alt: "Completed percentage"
gallery2:
  - url: /assets/images/logbook/20211026/lap_seconds.png
    image_path: /assets/images/logbook/20211026/lap_seconds.png
    alt: "Lap seconds"
gallery3:
  - url: /assets/images/logbook/20211026/position_deviation.png
    image_path: /assets/images/logbook/20211026/position_deviation.png
    alt: "Position deviation"
gallery4:
  - url: /assets/images/logbook/20211026/average_speed.png
    image_path: /assets/images/logbook/20211026/average_speed.png
    alt: "Average speed"


---

This blog is for sharing results retrieved using the new position deviation calculation. For this, we have generated
new perfect lap bags for each circuit, this time considering exactly the red line positions to be the perfect points, 
so our target points for each brain.

Below, we have run the same experiments with the 3 brains that we had working and the new metric, which outputs different 
result if we compare them to the previous obtained ones.

# Results 

{% include gallery id="gallery" caption="" %}

{% include gallery id="gallery1" caption="" %}

{% include gallery id="gallery2" caption="" %}

{% include gallery id="gallery3" caption="" %}

{% include gallery id="gallery4" caption="" %}

{% include gallery id="gallery5" caption="" %}
