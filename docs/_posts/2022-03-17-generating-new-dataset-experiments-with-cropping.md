---
title: "New dataset, experiments with new cropping"
excerpt: ""


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
  - url: /assets/images/logbook/20220317/simple_circuit_new_dataset.png
    image_path: /assets/images/logbook/20220317/simple_circuit_new_dataset.png
    alt: "Simple circuit new dataset"
gallery1:
  - url: /assets/images/logbook/20220317/simple_circuit_old_dataset.png
    image_path: /assets/images/logbook/20220317/simple_circuit_old_dataset.png
    alt: "Simple circuit old dataset"

---

# Key Ideas of this week progress

* New models trained for new cropping strategy don't work. Probably because the dataset for training is different on that part 
so they're able to generalize if they're shown just the road part but if the sky is present, the results are worse.
* Current dataset analysis for new cropping cases.
* New generated dataset for simple circuit, many curves and nurburgring for both clockwise and anticlockwise directions.


## Models trained with new cropping strategy

Considering [previous week](../comparing-cropping/) analysis on how some models improved its performance when the cropping of the images
was higher in testing time (without retraining the models), we have trained some current models with this new cropping 
strategy, expecting improvements on the performance. 

The results have been worse than the previous baselines for the models with memory (deepest x3, pilotnet 3d and frankenstein) when trained
with this approach. They struggle to complete all the circuits, even the simplest ones. 

We took a step back and trained again the Frankenstein model with the previous hyperparameters (previous cropping approach) to understand if the training
was the issue and found a similar performance for this trained model with previous hyperparameters to the baseline Frankenstein model that we already had. We discarded 
a possible issue on the training then, so the problem should be on the data.

## Dataset cropping analysis

The following images show, on the left, how the brain sees the world currently and, on the right, how the current 
dataset is constructed. Considering the new cropping strategies, adding some pixels of the sky could add information that is
not relevant for the model (blue vs grey sky).

The current used dataset was built on circuits that are different from the current ones, with different lights and turns.
Additionally, the PID brain developed to generate that dataset is different from the ones available now.

<table class="heatMap">
<thead>
    <tr>
        <th>New dataset</th>
        <th>Old dataset</th>
    </tr>
</thead>
<tbody>
    <tr>
        <td>{% include gallery id="gallery" caption="" %}</td>
        <td>{% include gallery id="gallery1" caption="" %}</td>
    </tr>
</tbody>
</table>

## Generating a new dataset.

After the previous consideration, a new dataset has been generated to compare the performance.

This dataset is generated using the explicit brain available with Behavior Metrics, as follows:

* 2 clockwise turns of the simple circuit
* 2 anticlockwise turns of the simple circuit
* 2 clockwise turns of the many curves circuit
* 2 anticlockwise turns of the many curves circuit
* 2 clockwise turns of the Nurburgring circuit
* 2 anticlockwise turns of the Nurburgring circuit


