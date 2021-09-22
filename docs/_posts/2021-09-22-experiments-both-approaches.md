---
title: "Experiments with DeepestLSTMTinyPilonet and Pilotnet on more circuits"
excerpt: "Experiments with DeepestLSTMTinyPilonet  and Pilotneton more circuits"


sidebar:
  nav: "docs"

categories:
- Behavior Studio
tags:
- Deepest LSTM TinyPilotNet
- Pilotnet
- comparison
- Nurburgring
- Montreal



author: Sergio Paniego
pinned: false

gallery:
  - url: /assets/images/logbook/20210922/completed_distance.png
    image_path: /assets/images/logbook/20210922/completed_distance.png
    alt: "Completed distance"
gallery1:
  - url: /assets/images/logbook/20210922/completed_percentage.png
    image_path: /assets/images/logbook/20210922/completed_percentage.png
    alt: "Completed percentage"
gallery2:
  - url: /assets/images/logbook/20210922/lap_seconds.png
    image_path: /assets/images/logbook/20210922/lap_seconds.png
    alt: "Lap seconds"
gallery3:
  - url: /assets/images/logbook/20210922/orientation_mae.png
    image_path: /assets/images/logbook/20210922/orientation_mae.png
    alt: "Orientations mAE"
gallery4:
  - url: /assets/images/logbook/20210922/orientation_total_error.png
    image_path: /assets/images/logbook/20210922/orientation_total_error.png
    alt: "Orientation total error"
gallery5:
  - url: /assets/images/logbook/20210922/average_speed.png
    image_path: /assets/images/logbook/20210922/average_speed.png
    alt: "Average speed"


---


More experiments conducted using Deepest LSTM TinyPilotNet and PilotNet on even more circuits.

The lines that cross lap seconds and orientation mae reflect the mean for each metric using the explicit brain.

On the lap seconds metrics, we can see thah both PilotNet and Deepest are faster than the explicit brain for all the circuits. 
From the lap seconds metrics we can also learn that PilotNet seems to be faster than Deepest LSTM.

Comparing the Orientation MAE, the conclusions are different. The explicit brain is better for all the circuits. For Montmeló the error
is much higher for every approach than on any other circuit, which means that this circuit is more difficult. For the rest of the circuits, 
the explicit brain behaves quite better than the rest of the brains. 
Considering Deepest and PilotNet, Deepest results are slightly better for all the circuits, even completing Montmeló more times than PilotNet.


# Results 

{% include gallery id="gallery" caption="" %}

{% include gallery id="gallery1" caption="" %}

{% include gallery id="gallery2" caption="" %}

{% include gallery id="gallery3" caption="" %}

{% include gallery id="gallery4" caption="" %}

{% include gallery id="gallery5" caption="" %}

