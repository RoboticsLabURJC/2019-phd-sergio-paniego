---
title: "Real time factor comparison"
excerpt: "Comparing how changing Gazebo simulation real time factor affects the results"


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
  - url: /assets/images/logbook/20220118/completed_distance_comparison.png
    image_path: /assets/images/logbook/20220118/completed_distance_comparison.png
    alt: "Completed distance comparison"
gallery1:
  - url: /assets/images/logbook/20220118/completed_percentage_comparison.png
    image_path: /assets/images/logbook/20220118/completed_percentage_comparison.png
    alt: "Completed percentage completed"
gallery2:
  - url: /assets/images/logbook/20220118/position_deviation_comparison.png
    image_path: /assets/images/logbook/20220118/position_deviation_comparison.png
    alt: "Position deviation comparison"
gallery3:
  - url: /assets/images/logbook/20220118/lap_seconds_comparison.png
    image_path: /assets/images/logbook/20220118/lap_seconds_comparison.png
    alt: "Lap seconds comparison"
gallery4:
  - url: /assets/images/logbook/20220118/average_speed_comparison.png
    image_path: /assets/images/logbook/20220118/average_speed_comparison.png
    alt: "Average speed comparison"
gallery5:
  - url: /assets/images/logbook/20220118/frame_rate_comparison.png
    image_path: /assets/images/logbook/20220118/frame_rate_comparison.png
    alt: "Frame rate"
gallery6:
  - url: /assets/images/logbook/20220118/mean_iteration_time_comparison.png
    image_path: /assets/images/logbook/20220118/mean_iteration_time_comparison.png
    alt: "Mean iteration time"
gallery7:
  - url: /assets/images/logbook/20220118/mean_inference_time_comparison.png
    image_path: /assets/images/logbook/20220118/mean_inference_time_comparison.png
    alt: "Mean inference time comparison"
gallery8:
  - url: /assets/images/logbook/20220118/mean_ros_iteration_comparison.png
    image_path: /assets/images/logbook/20220118/mean_ros_iteration_comparison.png
    alt: "Mean ROS iteration time comparison"
gallery9:
  - url: /assets/images/logbook/20220118/real_time_factor_comparison.png
    image_path: /assets/images/logbook/20220118/real_time_factor_comparison.png
    alt: "Real time factor comparison"
gallery10:
  - url: /assets/images/logbook/20220118/position_deviation_comparison_detail.png
    image_path: /assets/images/logbook/20220118/position_deviation_comparison_detail.png
    alt: "Position deviation comparisondetail"


---

Happy 2022 everyone!

In this new blog post, I explore the importance of Gazebo simulator real time factor and the computational load of the machine in the 
performance of the brains developed until today.

We have started training brains that accept several images as input at the same time and so we started wondering how this new 
computation was affecting the overall performance of the simulation and robot control. 

In the following plots, the comparison of the different metrics can be observerd. We compare 3 brains in several scenarios. 
The first brain is a Deepest LSTM Tinypilotnet brain, the second one a PilotNet with 3dconv layers that accepts 3 images and the third
brain is a common PID controller. The interesting comparison here is on the `Real time update rate` factor that modifies the real time factor
of the Gazebo simulation. The modification of this parameter makes the Gazebo simulation faster or slower, varying the computational load depending
on the value used. In this case, we compare 4 values for the parameter: 1000, 500, 100 and 50 (different bar colors). 1000 is the default parameter value on the simulation.

Additionally, we compare the cases where the GPU is used for inference against those where the inference is done using CPU computation.

Browsing the plots, we can have some ideas:
* The best `Real time update rate` for our machine is 100.
* The GPU vs. CPU battle is won by the CPU. This could be related to the fact that the inference is done 1 image at a time, so we are not using the 
GPU capabilities.
* The neural brains already complete Montmeló when the `Real time update rate` is 100. This fact means that our machine computation load is too high to handle
the simulation and execution of the brain on the default settings. Since we are using simulation, we can do this trick but if we want to use the brains
  on a real robot we should consider this issues.
* When the `Real time update rate` is lower, the brain is able to complete Montmeló faster and with better position deviation error.
* The more iterations of the brain the better it performs. When the `Real time update rate` is 100 or lower, the neural brains are able to achieve 10 iterations
of the brain per second, enough for this control task.



{% include gallery id="gallery" caption="Completed distance comparison" %}

{% include gallery id="gallery1" caption="Completed percentage comparison" %}

{% include gallery id="gallery2" caption="Position deviation comparison" %}

{% include gallery id="gallery3" caption="Laps seconds comparison" %}

{% include gallery id="gallery4" caption="Average speed comparison" %}

{% include gallery id="gallery5" caption="Frame rate comparison" %}

{% include gallery id="gallery6" caption="Mean iteration time comparison" %}

{% include gallery id="gallery7" caption="Mean inference time comparison" %}

{% include gallery id="gallery8" caption="Mean ROS iteration time comparison" %}

{% include gallery id="gallery9" caption="Real time factor comparison" %}

# Detail of position deviation

In this plot, a detail of the position deviation values is shown, removing one value that was different. 
The plot shows that the `Real time update rate` plays an important role in the simulations, when it's 100 or lower, the
performance of the different brains is close to the same.

{% include gallery id="gallery10" caption="Position deviation detailed comparison" %}