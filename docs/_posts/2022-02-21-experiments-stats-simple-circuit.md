---
title: "Experiments analysis for simple circuit"
excerpt: "Looking at some experiments"


sidebar:
  nav: "docs"

categories:
- Behavior Metrics
tags:
- Experiments
- Analysis

author: Sergio Paniego
pinned: false


gallery:
  - url: /assets/images/logbook/20220221/completed_distance.png
    image_path: /assets/images/logbook/20220221/completed_distance.png
    alt: "Completed distance"
gallery1:
  - url: /assets/images/logbook/20220221/completed_percentage.png
    image_path: /assets/images/logbook/20220221/completed_percentage.png
    alt: "Completed percentage"
gallery2:
  - url: /assets/images/logbook/20220221/lap_seconds.png
    image_path: /assets/images/logbook/20220221/lap_seconds.png
    alt: "Lap seconds"
gallery3:
  - url: /assets/images/logbook/20220221/average_speed.png
    image_path: /assets/images/logbook/20220221/average_speed.png
    alt: "Average speed simple"
gallery4:
  - url: /assets/images/logbook/20220221/position_deviation_mean.png
    image_path: /assets/images/logbook/20220221/position_deviation_mean.png
    alt: "Position deviation mean"
gallery5:
  - url: /assets/images/logbook/20220221/frame_rate.png
    image_path: /assets/images/logbook/20220221/frame_rate.png
    alt: "Frame rate"
gallery6:
  - url: /assets/images/logbook/20220221/mean_inference_time.png
    image_path: /assets/images/logbook/20220221/mean_inference_time.png
    alt: "Mean inference time"
gallery7:
  - url: /assets/images/logbook/20220221/real_time_factor.png
    image_path: /assets/images/logbook/20220221/real_time_factor.png
    alt: "Real time factor"
gallery8:
  - url: /assets/images/logbook/20220221/mean_brain_iterations_real_time.png
    image_path: /assets/images/logbook/20220221/mean_brain_iterations_real_time.png
    alt: "Mean brain iterations real"
gallery9:
  - url: /assets/images/logbook/20220221/brain_iterations_freq_simulated.png
    image_path: /assets/images/logbook/20220221/brain_iterations_freq_simulated.png
    alt: "Brain iterations frequency simulated"

---

This is the second iteration of the analysis of experiments. 
In this case the experiments are conducted on the **simple circuit**, and with a special consideration. We only consider the 
experiments where the simulated time is above 120 seconds, so we only consider successful experiments.

We compare 4 different brains modifying the brain cycle time, to set the maximum amount of iterations per second.

Analyzing the experiments, we can see that **for evey brain, adding more possible brain iterations per second increases the performance**.


{% include gallery id="gallery" caption="" %}

{% include gallery id="gallery1" caption="" %}

{% include gallery id="gallery2" caption="" %}

{% include gallery id="gallery3" caption="" %}

{% include gallery id="gallery4" caption="" %}

{% include gallery id="gallery5" caption="" %}

{% include gallery id="gallery6" caption="" %}

{% include gallery id="gallery7" caption="" %}

{% include gallery id="gallery8" caption="" %}

{% include gallery id="gallery9" caption="" %}

