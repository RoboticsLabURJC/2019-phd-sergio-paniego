---
title: "Brain iterations comparison extended"
excerpt: "Comparing how changing the brain iterations affects the output"


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
  - url: /assets/images/logbook/20220201/completed_distance_comparison.png
    image_path: /assets/images/logbook/20220201/completed_distance_comparison.png
    alt: "Completed distance comparison"
gallery1:
  - url: /assets/images/logbook/20220201/completed_percentage_comparison.png
    image_path: /assets/images/logbook/20220201/completed_percentage_comparison.png
    alt: "Completed percentage comparison"
gallery2:
  - url: /assets/images/logbook/20220201/position_deviation_comparison.png
    image_path: /assets/images/logbook/20220201/position_deviation_comparison.png
    alt: "Position deviation comparison"
gallery3:
  - url: /assets/images/logbook/20220201/lap_seconds_comparison.png
    image_path: /assets/images/logbook/20220201/lap_seconds_comparison.png
    alt: "Lap seconds comparison"
gallery4:
  - url: /assets/images/logbook/20220201/average_speed_comparison.png
    image_path: /assets/images/logbook/20220201/average_speed_comparison.png
    alt: "Average speed comparison"    
gallery5:
  - url: /assets/images/logbook/20220201/frame_rate_comparison.png
    image_path: /assets/images/logbook/20220201/frame_rate_comparison.png
    alt: "Frame rate comparison"
gallery6:
  - url: /assets/images/logbook/20220201/mean_iteration_time_comparison.png
    image_path: /assets/images/logbook/20220201/mean_iteration_time_comparison.png
    alt: "Mean iteration comparison"
gallery7:
  - url: /assets/images/logbook/20220201/mean_inference_time_comparison.png
    image_path: /assets/images/logbook/20220201/mean_inference_time_comparison.png
    alt: "Mean inference comparison"
gallery8:
  - url: /assets/images/logbook/20220201/mean_ros_iteration_time_comparison.png
    image_path: /assets/images/logbook/20220201/mean_ros_iteration_time_comparison.png
    alt: "ROS iteration comparison"
  


---

This post is an extension of the [previous post](../brain-iterations-comparison/) comparing the performance of the robot with different max brain iteration thresholds. 

We have added a broader range of low values to the comparison. The results are pretty similar to the ones on the previous post. We can see that the performance for both
brains starts decreasing from 1Hz to lower values, although the actual results vary for the actual execution.

The conclusion could be that the brain speed is not as high as it could be. We should explore how increasing the speed of the brain affects these results shown here to verify this hypothesis.

{% include gallery id="gallery" caption="Completed distance comparison" %}

{% include gallery id="gallery1" caption="Completed percentage comparison" %}

{% include gallery id="gallery2" caption="Position deviation comparison" %}

{% include gallery id="gallery3" caption="Lap seconds comparison" %}

{% include gallery id="gallery4" caption="Average speed comparison" %}

{% include gallery id="gallery5" caption="Frame rate comparison" %}

{% include gallery id="gallery6" caption="Mean iteration time comparison" %}

{% include gallery id="gallery7" caption="Mean inference time comparison" %}

{% include gallery id="gallery8" caption="Mean ROS iteration time comparison" %}