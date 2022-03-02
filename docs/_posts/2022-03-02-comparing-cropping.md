---
title: "Comparing cropping strategies"
excerpt: "Experiments on cropping"


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
  - url: /assets/images/logbook/20220302/montmelo_normal.png
    image_path: /assets/images/logbook/20220302/montmelo_normal.png
    alt: "Montmelo normal"
gallery1:
  - url: /assets/images/logbook/20220302/simple_no_line_normal.png
    image_path: /assets/images/logbook/20220302/simple_no_line_normal.png
    alt: "Simple no line normal"
gallery2:
  - url: /assets/images/logbook/20220302/simple_no_line_no_wall_normal.png
    image_path: /assets/images/logbook/20220302/simple_no_line_no_wall_normal.png
    alt: "Simple no line no wall normal"
gallery3:
  - url: /assets/images/logbook/20220302/simple_white_normal.png
    image_path: /assets/images/logbook/20220302/simple_white_normal.png
    alt: "Simple white normal"
gallery4:
  - url: /assets/images/logbook/20220302/simple_white_no_line_normal.png
    image_path: /assets/images/logbook/20220302/simple_white_no_line_normal.png
    alt: "Simple white no line normal"

gallery5:
  - url: /assets/images/logbook/20220302/montmelo_new.png
    image_path: /assets/images/logbook/20220302/montmelo_new.png
    alt: "Montmelo new"
gallery6:
  - url: /assets/images/logbook/20220302/simple_no_line_new.png
    image_path: /assets/images/logbook/20220302/simple_no_line_new.png
    alt: "Simple no line new"
gallery7:
  - url: /assets/images/logbook/20220302/simple_no_line_no_wall_new.png
    image_path: /assets/images/logbook/20220302/simple_no_line_no_wall_new.png
    alt: "Simple no line no wall new"
gallery8:
  - url: /assets/images/logbook/20220302/simple_white_new.png
    image_path: /assets/images/logbook/20220302/simple_white_new.png
    alt: "Simple white new"
gallery9:
  - url: /assets/images/logbook/20220302/simple_white_no_line_new.png
    image_path: /assets/images/logbook/20220302/simple_white_no_line_new.png
    alt: "Simple white no line new"
---

<style>
    .page {
      padding-right: 0px;
    }
    .heatMap {
        width: 70%;
        text-align: center;
    }
    .heatMap th {
        background: grey;
        word-wrap: break-word;
        text-align: center;
    }
    .heatMap tr:nth-child(2) { background: #E5E3C9; }
    .heatMap tr:nth-child(3) { background: #E5E3C9; }
    .heatMap tr:nth-child(4) { background: #B4CFB0; }
    .heatMap tr:nth-child(5) { background: #B4CFB0; }
    .heatMap tr:nth-child(6) { background: #94B49F; }
    .heatMap tr:nth-child(7) { background: #94B49F; }
    .heatMap tr:nth-child(8) { background: #74959A; }
    .heatMap tr:nth-child(9) { background: #74959A; }
    .heatMap tr:nth-child(10) { background: #789395; }
    .heatMap tr:nth-child(11) { background: #789395; }
    .heatMap tr:nth-child(12) { background: #E5E3C9; }
    .heatMap tr:nth-child(13) { background: #E5E3C9; }
</style>

<table class="heatMap">
<thead>
<tr>
  <th>Model</th>
  <th>Cropping</th>
  <th>Montmeló</th>
  <th>Simple circuit no red line</th>
  <th>Simple circuit no line no wall</th>
  <th>Simple circuit white road</th>
  <th>Simple circuit white road no line</th>
</tr>
</thead>
<tbody>
<tr>
  <td>Explicit</td>
  <td>-</td>
  <td>✅</td>
  <td>❌</td>
  <td>❌</td>
  <td>✅</td>
  <td>❌</td>
</tr>
<tr>
  <td>PilotNet</td>
  <td>Normal</td>
  <td>✅</td>
  <td>❌</td>
  <td>✅</td>
  <td>✅</td>
  <td>❌</td>
</tr>
<tr>
  <td>PilotNet</td>
  <td>NEW</td>
  <td>✅✅</td>
  <td>❌</td>
  <td>✅(over the grass)</td>
  <td>✅</td>
  <td>❌</td>
</tr>
<tr>
  <td>Deepest LSTM</td>
  <td>Normal</td>
  <td>✅</td>
  <td>❌</td>
  <td>✅</td>
  <td>❌</td>
  <td>❌</td>
</tr>
<tr>
  <td>Deepest LSTM</td>
  <td>NEW</td>
  <td>✅✅</td>
  <td>❌</td>
  <td>✅</td>
  <td>❌</td>
  <td>❌</td>
</tr>
<tr>
  <td>Best PilotNet 3D</td>
  <td>Normal</td>
  <td>✅(lowering rate)</td>
  <td>❌</td>
  <td>❌</td>
  <td>✅</td>
  <td>❌</td>
</tr>
<tr>
  <td>Best PilotNet 3D</td>
  <td>NEW</td>
  <td>✅</td>
  <td>❌</td>
  <td>❌</td>
  <td>✅</td>
  <td>❌</td>
</tr>
<tr>
  <td>Best Deepest LSTM 3D</td>
  <td>Normal</td>
  <td>✅(lowering rate)</td>
  <td>✅</td>
  <td>❌</td>
  <td>❌</td>
  <td>❌</td>
</tr>
<tr>
  <td>Best Deepest LSTM 3D</td>
  <td>NEW</td>
  <td>✅</td>
  <td>❌</td>
  <td>❌</td>
  <td>❌</td>
  <td>❌</td>
</tr>
<tr>
  <td>Frankenstein (x3)</td>
  <td>Normal</td>
  <td>✅(lowering rate)</td>
  <td>✅</td>
  <td>✅(over the grass)</td>
  <td>✅</td>
  <td>❌(last turns)</td>
</tr>
<tr>
  <td>Frankenstein (x3)</td>
  <td>NEW</td>
  <td>✅</td>
  <td>❌</td>
  <td>✅(over the grass)</td>
  <td>✅</td>
  <td>✅</td>
</tr>
<tr>
  <td>Example image</td>
  <td>Normal</td>
  <td>{% include gallery id="gallery" caption="" %}</td>
  <td>{% include gallery id="gallery1" caption="" %}</td>
  <td>{% include gallery id="gallery2" caption="" %}</td>
  <td>{% include gallery id="gallery3" caption="" %}</td>
  <td>{% include gallery id="gallery4" caption="" %}</td>
</tr>
<tr>
  <td>Example image</td>
  <td>NEW</td>
  <td>{% include gallery id="gallery5" caption="" %}</td>
  <td>{% include gallery id="gallery6" caption="" %}</td>
  <td>{% include gallery id="gallery7" caption="" %}</td>
  <td>{% include gallery id="gallery8" caption="" %}</td>
  <td>{% include gallery id="gallery9" caption="" %}</td>
</tr>
</tbody>
</table>


### Conclusions

Modifying the cropping of the input image in test time seems to help on the normal circuits (those close to the training images), 
whereas it doesn't help when the circuit is modified.
