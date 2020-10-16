---
title: "Behavior Studio current state [oct 2020]"
excerpt: "Current state of the project and experiments made during last weeks."

sidebar:
  nav: "docs"

categories:
- Behavior Studio
tags:
- detection brain
- regression brain

author: Sergio Paniego
pinned: false
---

[Behavior Studio](https://jderobot.github.io/BehaviorStudio/) is the project I have started helping developed during the 
last couple of months. The code is available [here](https://github.com/JdeRobot/BehaviorStudio).

We are studying different approaches to the follow-the-line exercise based on deep learning to create a comparison of techniques
and understand deeply their performance and which solution is better. 

The project is available for both ROS noetic and melodic, but I have dedicated my efforts to the noetic branch. 

The lasts few weeks, I have replicated some brains that were previous working in an old version of the project while updating some other
sections. We had a dataset based on the circuit called simple circuit and I have trained the new brains with that dataset to prove that
it is still usable. The brains are based on classification and regression.


# Classification brain

The classification brain is divided in two networks, one that manages the lineal speed (V) and the other that manages the 
angular speed (W). This implies training two different networks. The architecture chosen is a **SmallerVGGNet**. 

The V has 5 different classes: *slow*, *moderate*, *fast*, *very_fast* and *negative*. The W has 7 different classes: *radically_left*, 
*moderately_left*, *slightly_left*, *slight*, *slightly_right*, *moderately_right* and *radically_right*. 

The images from the dataset are cropped to make it easier to the network to focus on the part that is relevant. With 65 epochs and accuracy of 
0.96 is achieved and the two networks are able to complete the simple circuit. 

Some aspects to improve here are that the car something make fast changes in its direction, because of the classes specified and the image that is used
as input and this scenario sometimes causes the car to crash against the wall.

# Regression brain

The regression brain is also divided in two networks, one for the V and other for W. The architecture is Pilot Net, which is simple but enough for this problem.
300 epochs are used to train these two networks. In this case, the network completed the scenario easily, performing better than
the classification brain. The car doesn't make those fast movements previously stated and here the movement is smoother.

Here is a video with the performance of the regression brain in the simple circuit.

## Regression brain video

<iframe width="420" height="315" src="http://www.youtube.com/embed/LcSnuJ99VIg" frameborder="0" allowfullscreen></iframe>
