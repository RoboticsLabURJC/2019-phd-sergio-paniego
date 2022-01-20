---
title: "Max speed comparison"
excerpt: "Comparing how changing the speed of the robot affects the output"


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
  - url: /assets/images/logbook/20220120/lap_seconds_comparison.png
    image_path: /assets/images/logbook/20220120/lap_seconds_comparison.png
    alt: "Lap seconds comparison"
gallery1:
  - url: /assets/images/logbook/20220120/average_speed_comparison.png
    image_path: /assets/images/logbook/20220120/average_speed_comparison.png
    alt: "Average speed comparison"
gallery2:
  - url: /assets/images/logbook/20220120/position_deviation_comparison.png
    image_path: /assets/images/logbook/20220120/position_deviation_comparison.png
    alt: "Position deviation comparison"


---

After the previous post where we discussed the importance of the real time factor of the simulation
on the performance of the robot, here we discuss how fast can the car go. For this experiment, we select the previous
best `Real time update rate` which was 100 and start multiplying the speed for both linear and angular factors. 

In the following plots, the results are displayed. Two brains are used, the PID one (explicit-right-hand side of the table) and 
the deepest LSTM Tinypilotnet (left-hand side bars). As we can see, we are able to complete the circuit even multiplying the speeds 4 times.
The position deviation start growing when we multiply the speeds, which is the expected behavior. It's interesting to point that the 
seconds spend on completing a lap when the speed is the normal one are 80 whereas when the speed is multiplied the time factor is reduced heavily (around 25 secs on completing the lap on the best cases).


When multiplied 5 times, the brains are not able to complete the lap.

{% include gallery id="gallery" caption="Completed distance comparison" %}

{% include gallery id="gallery1" caption="Completed percentage comparison" %}

{% include gallery id="gallery2" caption="Position deviation comparison" %}
