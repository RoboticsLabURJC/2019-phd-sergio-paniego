---
title: "Applying data augmentations with Albumentations on Tensorflow"
excerpt: "Applying data augmentations with Albumentations on Tensorflow"


sidebar:
  nav: "docs"

categories:
- Behavior Studio
tags:
- data augmentation
- detection brain
- preprocessing 



author: Sergio Paniego
pinned: false

gallery:
  - url: /assets/images/logbook/20210707/montmelo-completed.png
    image_path: /assets/images/logbook/20210707/montmelo-completed.png
    alt: "Montmelo circuit"

---

Data preprocessing is one of the most important parts on a machine learning pipeline. In this case, we are exploring
state of the art approaches on data augmentation using [Albumentations](https://albumentations.ai/). 

The workflow takes the images and makes some transformations over them during the training part, transforming the images on a probabilistic 
basis for each batch of images. This generates lots of different images to train with. 

With this workflow, some networks are trained with the PilotNet architecture previously studied. 

The transformations are: 

```
AUGMENTATIONS_TRAIN = Compose([
    RandomBrightnessContrast(),
    HueSaturationValue(),
    FancyPCA(),
    RandomGamma(),
    GaussianBlur(),
    GaussNoise(),
    Normalize()
])
```


Experiments:
* [Results for Pilotnet with train and validation data](#experiment-1)
* [Results for Pilotnet with extreme cases](#experiment-2)
* [Results for Pilotnet with extreme cases repeated more](#experiment-3)
* [Results for Pilotnet with complete-many_curves dataset and extreme cases](#experiment-4)
* [Results for Pilotnet with complete-many_curves dataset and extreme cases x 2 ](#experiment-5)

<a name="experiment-1"></a>
# 1. Results for Pilotnet with train and validation data

The simple case, with just the training and validation dataset with the transformations doesn't generate good results.
This brains doesn't even complete the simple circuit.  

<a name="experiment-2"></a>
# 2. Results for Pilotnet with extreme cases

Adding repeated extreme cases to the dataset when reading it, generates a brain that can complete the circuit but Montmelo.
It fails on the final turns.

<a name="experiment-3"></a>
# 3. Results for Pilotnet with extreme cases repeated more

Finally, this brain can complete Montmeló! 

The dataset is both Train and Test folders with extreme cases repeated even more. 

<a name="experiment-4"></a>
# 4. Results for Pilotnet with complete-many_curves dataset and extreme cases

In this case, instead of using the train and val folders, we trying using the complete dataset and many curves dataset folders. 
The information should be almost the same as in the previous scenario. We read both folders and separate train-val parts. After that, 
we add extreme cases and transform the images with the same workflow. 

This new scenario generates a Pilotnet brain that can complete all the circuits, even Montmeló.

## Montmeló completed

{% include gallery id="gallery" caption="" %} 

<a name="experiment-5"></a>
# 5. Results for Pilotnet with complete-many_curves dataset and extreme cases x 2 

Following the same idea developed on Experiment 3, for this experiment complete and many curves datasets are used but adding even more times
the extreme casees. This new brain is also able to complete Montmeló

