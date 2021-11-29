---
title: "Where are the extreme cases located on the circuits?"
excerpt: "I look for the extreme cases considering the angular speed and derivative value on the PID controller."


sidebar:
  nav: "docs"

categories:
- Behavior Studio
tags:
- Deepest LSTM TinyPilotNet
- Pilotnet
- PID brain
- comparison
- Metrics



author: Sergio Paniego
pinned: false

gallery:
  - url: /assets/images/logbook/20211129/simple_circuit_speed_v.png
    image_path: /assets/images/logbook/20211129/simple_circuit_speed_v.png
    alt: "Simple circuit speed"
gallery1:
  - url: /assets/images/logbook/20211129/simple_circuit_speed_w.png
    image_path: /assets/images/logbook/20211129/simple_circuit_speed_w.png
    alt: "Simple circuit speed"
gallery2:
  - url: /assets/images/logbook/20211129/simple_circuit_derivative.png
    image_path: /assets/images/logbook/20211129/simple_circuit_derivative.png
    alt: "Simple circuit derivative"
gallery3:
  - url: /assets/images/logbook/20211129/many_curves_speed_v.png
    image_path: /assets/images/logbook/20211129/many_curves_speed_v.png
    alt: "Many curves speed"
gallery4:
  - url: /assets/images/logbook/20211129/many_curves_speed_w.png
    image_path: /assets/images/logbook/20211129/many_curves_speed_w.png
    alt: "Many curves speed"
gallery5:
  - url: /assets/images/logbook/20211129/many_curves_derivative.png
    image_path: /assets/images/logbook/20211129/many_curves_derivative.png
    alt: "Many curves derivative"
gallery6:
  - url: /assets/images/logbook/20211129/montmelo_line_speed_v.png
    image_path: /assets/images/logbook/20211129/montmelo_line_speed_v.png
    alt: "Montmelo line speed"    
gallery7:
  - url: /assets/images/logbook/20211129/montmelo_line_speed_w.png
    image_path: /assets/images/logbook/20211129/montmelo_line_speed_w.png
    alt: "Montmelo line speed"
gallery8:
  - url: /assets/images/logbook/20211129/montmelo_line_derivative.png
    image_path: /assets/images/logbook/20211129/montmelo_line_derivative.png
    alt: "Montmelo line derivative"
gallery9:
  - url: /assets/images/logbook/20211129/montreal_speed_v.png
    image_path: /assets/images/logbook/20211129/montreal_speed_v.png
    alt: "Montreal speed"
gallery10:
  - url: /assets/images/logbook/20211129/montreal_speed_w.png
    image_path: /assets/images/logbook/20211129/montreal_speed_w.png
    alt: "Montreal speed"
gallery11:
  - url: /assets/images/logbook/20211129/montreal_derivative.png
    image_path: /assets/images/logbook/20211129/montreal_derivative.png
    alt: "Montreal derivative"
gallery12:
  - url: /assets/images/logbook/20211129/nurburgring_speed_v.png
    image_path: /assets/images/logbook/20211129/nurburgring_speed_v.png
    alt: "Nurburgring speed"
gallery13:
  - url: /assets/images/logbook/20211129/nurburgring_speed_w.png
    image_path: /assets/images/logbook/20211129/nurburgring_speed_w.png
    alt: "Nurburgring speed"
gallery14:
  - url: /assets/images/logbook/20211129/nurburgring_derivative.png
    image_path: /assets/images/logbook/20211129/nurburgring_derivative.png
    alt: "Nurburgring derivative"

---

Analyzing where the extreme cases are located on the different circuits for the three considered metrics: linear velocity (V speed), 
angular velocity (W speed), and derivative part from the PID controller driver on the different circuits.

This visualization allows us to understand where the extreme cases are located across the circuits.


# Results 

# Simple circuit


{% include gallery id="gallery" caption="Simple circuit V speed" %}

{% include gallery id="gallery1" caption="Simple circuit W speed" %}

{% include gallery id="gallery2" caption="Simple circuit derivative value" %}

# Many curves circuit

{% include gallery id="gallery3" caption="Many curves circuit V speed" %}

{% include gallery id="gallery4" caption="Many curves circuit W speed" %}

{% include gallery id="gallery5" caption="Many curves circuit derivative value" %}

# Montmeló circuit

{% include gallery id="gallery6" caption="Montmeló circuit V speed" %}

{% include gallery id="gallery7" caption="Montmeló circuit W speed" %}

{% include gallery id="gallery8" caption="Montmeló circuit derivative value" %}

# Montreal circuit

{% include gallery id="gallery9" caption="Montreal circuit V speed" %}

{% include gallery id="gallery10" caption="Montreal circuit W speed" %}

{% include gallery id="gallery11" caption="Montreal circuit derivative value" %}

# Nurburgring circuit

{% include gallery id="gallery12" caption="Nurburgring circuit V speed" %}

{% include gallery id="gallery13" caption="Nurburgring circuit W speed" %}

{% include gallery id="gallery14" caption="Nurburgring circuit derivative value" %}

