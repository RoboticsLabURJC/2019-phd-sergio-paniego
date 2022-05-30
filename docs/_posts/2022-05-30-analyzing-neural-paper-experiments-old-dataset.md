---
title: "Analyzing Neural paper experiment with old dataset"
excerpt: "First experimental results analysis"


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
  - url: /assets/images/logbook/20220530/success_ratio_circuits_combined.png
    image_path: /assets/images/logbook/20220530/success_ratio_circuits_combined.png
    alt: ""
gallery1:
  - url: /assets/images/logbook/20220530/success_ratio_models_combined.png
    image_path: /assets/images/logbook/20220530/success_ratio_models_combined.png
    alt: ""
gallery2:
  - url: /assets/images/logbook/20220530/success_ratio_simple_circuit.png
    image_path: /assets/images/logbook/20220530/success_ratio_simple_circuit.png
    alt: ""
gallery3:
  - url: /assets/images/logbook/20220530/success_ratio_many_curves.png
    image_path: /assets/images/logbook/20220530/success_ratio_many_curves.png
    alt: ""
gallery4:
  - url: /assets/images/logbook/20220530/success_ratio_montmelo.png
    image_path: /assets/images/logbook/20220530/success_ratio_montmelo.png
    alt: ""
gallery5:
  - url: /assets/images/logbook/20220530/success_ratio_nurburgring.png
    image_path: /assets/images/logbook/20220530/success_ratio_nurburgring.png
    alt: ""
gallery6:
  - url: /assets/images/logbook/20220530/classification.png
    image_path: /assets/images/logbook/20220530/classification.png
    alt: ""
gallery7:
  - url: /assets/images/logbook/20220530/regression.png
    image_path: /assets/images/logbook/20220530/regression.png
    alt: ""
gallery8:
  - url: /assets/images/logbook/20220530/simple_circuit_lap_seconds.png
    image_path: /assets/images/logbook/20220530/simple_circuit_lap_seconds.png
    alt: ""
gallery9:
  - url: /assets/images/logbook/20220530/many_curves_lap_seconds.png
    image_path: /assets/images/logbook/20220530/many_curves_lap_seconds.png
    alt: ""
gallery10:
  - url: /assets/images/logbook/20220530/montmelo_line_lap_seconds.png
    image_path: /assets/images/logbook/20220530/montmelo_line_lap_seconds.png
    alt: ""
gallery11:
  - url: /assets/images/logbook/20220530/nurburgring_line_lap_seconds.png
    image_path: /assets/images/logbook/20220530/nurburgring_line_lap_seconds.png
    alt: ""
gallery12:
  - url: /assets/images/logbook/20220530/simple_circuit_lap_seconds_filter.png
    image_path: /assets/images/logbook/20220530/simple_circuit_lap_seconds_filter.png
    alt: ""
gallery13:
  - url: /assets/images/logbook/20220530/many_curves_lap_seconds_filter.png
    image_path: /assets/images/logbook/20220530/many_curves_lap_seconds_filter.png
    alt: ""
gallery14:
  - url: /assets/images/logbook/20220530/montmelo_line_lap_seconds_filter.png
    image_path: /assets/images/logbook/20220530/montmelo_line_lap_seconds_filter.png
    alt: ""
gallery15:
  - url: /assets/images/logbook/20220530/nurburgring_line_lap_seconds_filter.png
    image_path: /assets/images/logbook/20220530/nurburgring_line_lap_seconds_filter.png
    alt: ""
gallery16:
  - url: /assets/images/logbook/20220530/simple_circuit_lap_seconds_filter_100.png
    image_path: /assets/images/logbook/20220530/simple_circuit_lap_seconds_filter_100.png
    alt: ""
gallery17:
  - url: /assets/images/logbook/20220530/many_curves_lap_seconds_filter_100.png
    image_path: /assets/images/logbook/20220530/many_curves_lap_seconds_filter_100.png
    alt: ""
gallery18:
  - url: /assets/images/logbook/20220530/montmelo_line_lap_seconds_filter_100.png
    image_path: /assets/images/logbook/20220530/montmelo_line_lap_seconds_filter_100.png
    alt: ""
gallery19:
  - url: /assets/images/logbook/20220530/nurburgring_line_lap_seconds_filter_100.png
    image_path: /assets/images/logbook/20220530/nurburgring_line_lap_seconds_filter_100.png
    alt: ""
gallery20:
  - url: /assets/images/logbook/20220530/circuits_success_100.png
    image_path: /assets/images/logbook/20220530/circuits_success_100.png
    alt: ""

---

# All circuit and all models success ratio

## Results for models in all circuits
{% include gallery id="gallery" caption="" %}

## Results for each circuit combining all models
{% include gallery id="gallery1" caption="" %}

# Success ratio for each circuit
## Results in simple circuit
{% include gallery id="gallery2" caption="" %}

## Results in many curves
{% include gallery id="gallery3" caption="" %}

## Results in montmeló
{% include gallery id="gallery4" caption="" %}

## Results in nurburgring
{% include gallery id="gallery5" caption="" %}

# Success ratio for type of annotations (classification vs regression)
## Results for classification models
{% include gallery id="gallery6" caption="" %}

## Results for regression models
{% include gallery id="gallery7" caption="" %}

## Lap seconds in simple circuit
{% include gallery id="gallery8" caption="" %}

# Lap seconds for each circuit
## Lap seconds in many curves
{% include gallery id="gallery9" caption="" %}

## Lap seconds in montmeló
{% include gallery id="gallery10" caption="" %}

## Lap seconds in nurburgring
{% include gallery id="gallery11" caption="" %}

# Combined lap seconds and success ratio > 80
## Lap seconds in simple circuit for success ratio > 80
{% include gallery id="gallery12" caption="" %}

## Lap seconds in many curves for success ratio > 80
{% include gallery id="gallery13" caption="" %}

## Lap seconds in montmeló for success ratio > 80
{% include gallery id="gallery14" caption="" %}

## Lap seconds in nurburgring for success ratio > 80
{% include gallery id="gallery15" caption="" %}

# Combined lap seconds and success ratio > 100
## Lap seconds in simple circuit for success ratio > 100
{% include gallery id="gallery16" caption="" %}

## Lap seconds in many curves for success ratio > 100
{% include gallery id="gallery17" caption="" %}

## Lap seconds in montmeló for success ratio > 100
{% include gallery id="gallery18" caption="" %}

## Lap seconds in nurburgring for success ratio > 100
{% include gallery id="gallery19" caption="" %}

# Number of circuits in which model has success ratio of 100
{% include gallery id="gallery20" caption="" %}



