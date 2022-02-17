---
title: "Brain iterations comparison"
excerpt: "Comparing how changing the brain iterations affects the output"


sidebar:
  nav: "docs"

categories:
- Behavior Metrics
tags:
- comparison
- Metrics



author: Sergio Paniego
pinned: false

gallery:
  - url: /assets/images/logbook/20220124/completed_distance_comparison.png
    image_path: /assets/images/logbook/20220124/completed_distance_comparison.png
    alt: "Completed distance comparison"
gallery1:
  - url: /assets/images/logbook/20220124/completed_percentage_comparison.png
    image_path: /assets/images/logbook/20220124/completed_percentage_comparison.png
    alt: "Completed percentage comparison"
gallery2:
  - url: /assets/images/logbook/20220124/position_deviation_comparison.png
    image_path: /assets/images/logbook/20220124/position_deviation_comparison.png
    alt: "Position deviation comparison"
gallery3:
  - url: /assets/images/logbook/20220124/lap_seconds_comparison.png
    image_path: /assets/images/logbook/20220124/lap_seconds_comparison.png
    alt: "Lap seconds comparison"
gallery4:
  - url: /assets/images/logbook/20220124/average_speed_comparison.png
    image_path: /assets/images/logbook/20220124/average_speed_comparison.png
    alt: "Average speed comparison"    
gallery5:
  - url: /assets/images/logbook/20220124/frame_rate_comparison.png
    image_path: /assets/images/logbook/20220124/frame_rate_comparison.png
    alt: "Frame rate comparison"
gallery6:
  - url: /assets/images/logbook/20220124/mean_iteration_time_comparison.png
    image_path: /assets/images/logbook/20220124/mean_iteration_time_comparison.png
    alt: "Mean iteration comparison"
gallery7:
  - url: /assets/images/logbook/20220124/mean_inference_time_comparison.png
    image_path: /assets/images/logbook/20220124/mean_inference_time_comparison.png
    alt: "Mean inference comparison"
gallery8:
  - url: /assets/images/logbook/20220124/mean_ROS_iteration_comparison.png
    image_path: /assets/images/logbook/20220124/mean_ROS_iteration_comparison.png
    alt: "ROS iteration comparison"
gallery9:
  - url: /assets/images/logbook/20220124/real_time_comparison.png
    image_path: /assets/images/logbook/20220124/real_time_comparison.png
    alt: "Real time comparison"    


---

After the last 2 posts, we continue with the comparisons of performance in brains to find out the best combination of factors.

In this comparison, we run the brains with different maximum brain iterations per seconds. With this comparison, we can understant
which is the minimum iterations per seconds that the brain needs in order to perform correctly on the experiments. 


The compared values are: 20 iterations per second, 10, 8, 6, 4, 2, 1, 0.5 and 0.1. All the experiments are run with a `Real time update factor` of 100

Looking at the bar charts, the brains are capable of finishing the lap even with 1 iteration of the brain per second. 


{% include gallery id="gallery" caption="Completed distance comparison" %}

{% include gallery id="gallery1" caption="Completed percentage comparison" %}

{% include gallery id="gallery2" caption="Position deviation comparison" %}

{% include gallery id="gallery3" caption="Completed distance comparison" %}

{% include gallery id="gallery4" caption="Completed percentage comparison" %}

{% include gallery id="gallery5" caption="Position deviation comparison" %}

{% include gallery id="gallery6" caption="Completed distance comparison" %}

{% include gallery id="gallery7" caption="Completed percentage comparison" %}

{% include gallery id="gallery8" caption="Position deviation comparison" %}




