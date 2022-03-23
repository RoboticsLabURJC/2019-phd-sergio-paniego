---
title: "Extending new dataset and training Pilotnet model"
excerpt: "The new dataset has been expanded for a broader support."


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
  - url: /assets/images/logbook/20220323/monaco_circuit.png
    image_path: /assets/images/logbook/20220323/monaco_circuit.png
    alt: "Monaco circuit"
gallery1:
  - url: /assets/images/logbook/20220323/extended_simple_circuit.png
    image_path: /assets/images/logbook/20220323/extended_simple_circuit.png
    alt: "Extended simple circuit"
gallery2:
  - url: /assets/images/logbook/20220323/cases_distribution_new_dataset.png
    image_path: /assets/images/logbook/20220323/cases_distribution_new_dataset.png
    alt: "Cases distribution"

---

# Key Ideas of this week progress

During this week:

* New circuits supported
* The new dataset has been expanded for a broader support of cases.
* Pilotnet has been trained with the new dataset with different approximations.

## New circuits supported

New circuits have been added to [CustomRobots](https://github.com/JdeRobot/CustomRobots/) repository, so they can be used on the experiments.

These circuits are:

* Monaco

{% include gallery id="gallery" caption="" %}

* Extended simple circuit

{% include gallery id="gallery1" caption="" %}

## Extended new dataset

[Last week](../generating-new-dataset-experiments-with-cropping), we started developing a new dataset with the following structure:

* 2 clockwise turns of the simple circuit
* 2 anticlockwise turns of the simple circuit
* 2 clockwise turns of the many curves circuit
* 2 anticlockwise turns of the many curves circuit
* 2 clockwise turns of the Nurburgring circuit
* 2 anticlockwise turns of the Nurburgring circuit

In addition to this configuration, new images and annotations have been added.

The new cases are:

* 2 clockwise turns of the extended simple circuit.
* 2 anticlockwise turns of the extended simple circuit.
* 2 clockwise turns of the Monaco circuit.
* 2 anticlockwise turns of the Monaco circuit.
* Curves only dataset from many curves, Monaco and Nurburgring circuits.
* Difficult cases from the same circuits. A difficult case is when the car is facing directly to the wall, so it has to find again the line.

On the last point, since the previous dataset lacked difficult cases or cases that where no ideally executed by the agent (just following the line always), 
if the car landed on a wall, it wouldn't know what to do based on the cases learned.


## Some trainings with PilotNet


Some trainings have been developed for Pilotnet and the new dataset. These are:


* Full dataset (from previous week) training 
* Full dataset + more extreme
* Full dataset without simple circuit + monaco + extended simple + curves only
* Full dataset without simple circuit + monaco + extended simple + curves only + difficult cases (**the best model**)
* Full dataset without simple circuit + monaco + curves only + difficult cases
* Full dataset without simple circuit + monaco + curves only
* Full dataset without simple circuit + monaco + extended simple + curves only + difficult cases + broader support on extreme cases.


The *broader support on extreme cases* means that extreme cases addition has been changed so the distribution of cases looks like this:

{% include gallery id="gallery2" caption="" %}

With the previous approach used, there was a big gap between the extreme parts of the below plot and the middle top part.
