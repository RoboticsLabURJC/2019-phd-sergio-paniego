---
title: "Imitation learning based on Bird-eye view for follow lane autonomous driving in CARLA simulator"
excerpt: "We explore learning a policy for end-to-end driving in CARLA"


sidebar:
  nav: "docs"

categories:
- Behavior Metrics
tags:
- CARLA
- End-to-end

author: Sergio Paniego
pinned: false


---
  

We are currently exploring end-to-end imitation learning in CARLA using bird-eye view for a follow lane autonomous driving agent.
The idea of using bird-eye-view is inspired by [Learning by Cheating by Dian Chen et al.](https://arxiv.org/abs/1912.12294).

Trying to learn a policy for driving using bird-eye view could be easier since the perception part of the problem is already partly solved. 
Providing the agent with bird-eye view images, it doesn't need to fully understand the complexity of the world as compared to a frontal camera view.

In the following videos, the current state of the solution can be studied. 

## Follow lane with a maximum speed of 20 km/h

In this case, the maximum speed of the car is set to 20km/h. Once this speed is reached, we apply a brake command. The learned policy is able to complete
different circuits, curves and directions.


<iframe width="560" height="315" src="https://www.youtube.com/embed/AIOJeMJdBFM" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Follow lane with maximum speed of 30km/h

In the scenario, the maximum speed is set to 30km/h. We don't manually apply the brake command, but the cases extracted from the expert agent don't go over 30km/h at any time.
The previous speed is used as input for the model.
We are able to learn a policy that is able to drive in some situations but there is still room for improvements.

<iframe width="560" height="315" src="https://www.youtube.com/embed/9vaMMYanyUE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


