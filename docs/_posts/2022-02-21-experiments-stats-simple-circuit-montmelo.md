---
title: "Experiments analysis for simple circuit and Montmeló"
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


gallery10:
  - url: /assets/images/logbook/20220221/completed_distance_montmelo.png
    image_path: /assets/images/logbook/20220221/completed_distance_montmelo.png
    alt: "Completed distance"
gallery11:
  - url: /assets/images/logbook/20220221/completed_percentage_montmelo.png
    image_path: /assets/images/logbook/20220221/completed_percentage_montmelo.png
    alt: "Completed percentage"
gallery12:
  - url: /assets/images/logbook/20220221/lap_seconds_montmelo.png
    image_path: /assets/images/logbook/20220221/lap_seconds_montmelo.png
    alt: "Lap seconds"
gallery13:
  - url: /assets/images/logbook/20220221/average_speed_montmelo.png
    image_path: /assets/images/logbook/20220221/average_speed_montmelo.png
    alt: "Average speed simple"
gallery14:
  - url: /assets/images/logbook/20220221/position_deviation_mean_montmelo.png
    image_path: /assets/images/logbook/20220221/position_deviation_mean_montmelo.png
    alt: "Position deviation mean"
gallery15:
  - url: /assets/images/logbook/20220221/frame_rate_montmelo.png
    image_path: /assets/images/logbook/20220221/frame_rate_montmelo.png
    alt: "Frame rate"
gallery16:
  - url: /assets/images/logbook/20220221/mean_inference_time_montmelo.png
    image_path: /assets/images/logbook/20220221/mean_inference_time_montmelo.png
    alt: "Mean inference time"
gallery17:
  - url: /assets/images/logbook/20220221/real_time_factor_montmelo.png
    image_path: /assets/images/logbook/20220221/real_time_factor_montmelo.png
    alt: "Real time factor"
gallery18:
  - url: /assets/images/logbook/20220221/mean_brain_iterations_real_montmelo.png
    image_path: /assets/images/logbook/20220221/mean_brain_iterations_real_montmelo.png
    alt: "Mean brain iterations real"
gallery19:
  - url: /assets/images/logbook/20220221/brain_iterations_freq_simulated_montmelo.png
    image_path: /assets/images/logbook/20220221/brain_iterations_freq_simulated_montmelo.png
    alt: "Brain iterations frequency simulated"

gallery20:
  - url: /assets/images/logbook/20220221/brain_iterations_freq_real_montmelo.png
    image_path: /assets/images/logbook/20220221/brain_iterations_freq_real_montmelo.png
    alt: "Mean inference time"
gallery21:
  - url: /assets/images/logbook/20220221/target_brain_iterations_simulated_montmelo.png
    image_path: /assets/images/logbook/20220221/target_brain_iterations_simulated_montmelo.png
    alt: "Real time factor"
gallery22:
  - url: /assets/images/logbook/20220221/target_brain_iterations_real_montmelo.png
    image_path: /assets/images/logbook/20220221/target_brain_iterations_real_montmelo.png
    alt: "Mean brain iterations real"
gallery23:
  - url: /assets/images/logbook/20220221/mean_brain_iterations_simulated_montmelo.png
    image_path: /assets/images/logbook/20220221/mean_brain_iterations_simulated_montmelo.png
    alt: "Brain iterations frequency simulated"

---

This is the second iteration of the analysis of experiments. 
In this case the experiments are conducted on the **Simple circuit and Montmeló**, and with a special consideration. We only consider the 
experiments where the simulated time is above 120 seconds for Simple Circuit and 50 secs for Montmeló, so we only consider successful experiments.

We compare 4 different brains modifying the brain cycle time, to set the maximum amount of iterations per second.

Analyzing the experiments, we can see that **for evey brain, adding more possible brain iterations per second increases the performance**.


* [Simple circuit results](#simple-circuit)
* [Montmeló results](#montmelo)

# Simple circuit

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

# Montmelo

{% include gallery id="gallery10" caption="" %}

{% include gallery id="gallery11" caption="" %}

{% include gallery id="gallery12" caption="" %}

{% include gallery id="gallery13" caption="" %}

{% include gallery id="gallery14" caption="" %}

{% include gallery id="gallery15" caption="" %}

{% include gallery id="gallery16" caption="" %}

{% include gallery id="gallery17" caption="" %}

{% include gallery id="gallery18" caption="" %}

{% include gallery id="gallery19" caption="" %}

{% include gallery id="gallery20" caption="" %}

{% include gallery id="gallery21" caption="" %}

{% include gallery id="gallery22" caption="" %}

{% include gallery id="gallery23" caption="" %}