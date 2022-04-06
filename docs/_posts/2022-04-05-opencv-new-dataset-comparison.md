---
title: "Opencv new dataset vs Explicit dataset vs old dataset comparison"
excerpt: "Comparing how the brains perform training with different datasets"


sidebar:
  nav: "docs"

categories:
- Behavior Metrics
tags:
- Experiments
- Analysis

author: Sergio Paniego
pinned: false



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
    .heatMap tr:nth-child(3) { background: #E5E3C9; }
    .heatMap tr:nth-child(4) { background: #E5E3C9; }
    .heatMap tr:nth-child(5) { background: #E5E3C9; }
    .heatMap tr:nth-child(6) { background: #B4CFB0; }
    .heatMap tr:nth-child(7) { background: #B4CFB0; }
    .heatMap tr:nth-child(8) { background: #B4CFB0; }
    .heatMap tr:nth-child(9) { background: #94B49F; }
    .heatMap tr:nth-child(10) { background: #94B49F; }
    .heatMap tr:nth-child(11) { background: #94B49F; }
    .heatMap tr:nth-child(12) { background: #74959A; }
    .heatMap tr:nth-child(13) { background: #74959A; }
    .heatMap tr:nth-child(14) { background: #74959A; }
    .heatMap tr:nth-child(15) { background: #789395; }
    .heatMap tr:nth-child(16) { background: #789395; }
    .heatMap tr:nth-child(17) { background: #789395; }
    .heatMap tr:nth-child(18) { background: #E5E3C9; }
    .heatMap tr:nth-child(19) { background: #E5E3C9; }
    .heatMap tr:nth-child(20) { background: #E5E3C9; }


    .heatMap-2 {
        width: 100%;
        text-align: center;
    }
    .heatMap-2 th {
        background: grey;
        word-wrap: break-word;
        text-align: center;
    }
    .heatMap-2 tr:nth-child(4) { background: #E5E3C9; }
    .heatMap-2 tr:nth-child(5) { background: #E5E3C9; }
    .heatMap-2 tr:nth-child(6) { background: #E5E3C9; }
    .heatMap-2 tr:nth-child(7) { background: #B4CFB0; }
    .heatMap-2 tr:nth-child(8) { background: #B4CFB0; }
    .heatMap-2 tr:nth-child(9) { background: #B4CFB0; }
</style>


## Comparing which circuits do the brains complete

<table class="heatMap">
<thead>
<tr>
  <th>Model</th>
  <th>Dataset</th>
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
  <td>OpenCV</td>
  <td>-</td>
  <td>✅</td>
  <td>❌</td>
  <td>❌</td>
  <td>✅</td>
  <td>❌</td>
</tr>
<tr>
  <td>PilotNet</td>
  <td>Old</td>
  <td>✅</td>
  <td>❌</td>
  <td>✅</td>
  <td>✅</td>
  <td>❌</td>
</tr>
<tr>
  <td>PilotNet</td>
  <td>Explicit</td>
  <td>✅</td>
  <td>❌(last turns)</td>
  <td>❌(some turns ok)</td>
  <td>✅</td>
  <td>❌</td>
</tr>
<tr>
  <td>PilotNet</td>
  <td>OpenCV(fastest)</td>
  <td>✅(lowering rate much)</td>
  <td>❌</td>
  <td>❌</td>
  <td>✅</td>
  <td>❌</td>
</tr>
<tr>
  <td>Deepest LSTM</td>
  <td>Old</td>
  <td>✅</td>
  <td>❌</td>
  <td>✅</td>
  <td>❌</td>
  <td>❌</td>
</tr>
<tr>
  <td>Deepest LSTM</td>
  <td>Explicit</td>
  <td>✅</td>
  <td>❌</td>
  <td>❌</td>
  <td>✅</td>
  <td>❌</td>
</tr>
<tr>
  <td>Deepest LSTM</td>
  <td>OpenCV(fastest)</td>
  <td>✅(lowering rate)</td>
  <td>❌</td>
  <td>✅(over the grass)</td>
  <td>✅</td>
  <td>❌</td>
</tr>
<tr>
  <td>Frankenstein</td>
  <td>Old</td>
  <td>✅(lowering rate)</td>
  <td>✅</td>
  <td>✅(over the grass</td>
  <td>✅</td>
  <td>❌</td>
</tr>
<tr>
  <td>Frankenstein</td>
  <td>Explicit</td>
  <td>✅</td>
  <td>❌</td>
  <td>❌</td>
  <td>✅</td>
  <td>❌</td>
</tr>
<tr>
  <td>Frankenstein</td>
  <td>OpenCV(fastest)</td>
  <td>-</td>
  <td>-</td>
  <td>-</td>
  <td>-</td>
  <td>-</td>
</tr>
<tr>
  <td>PilotNet 3D</td>
  <td>Old</td>
  <td>✅(lowering rate)</td>
  <td>❌</td>
  <td>❌</td>
  <td>✅</td>
  <td>❌</td>
</tr>
<tr>
  <td>PilotNet 3D</td>
  <td>Explicit</td>
  <td>❌</td>
  <td>❌</td>
  <td>❌</td>
  <td>❌</td>
  <td>❌</td>
</tr>
<tr>
  <td>PilotNet 3D</td>
  <td>OpenCV(fastest)</td>
  <td>-</td>
  <td>-</td>
  <td>-</td>
  <td>-</td>
  <td>-</td>
</tr>
</tbody>
</table>

## Comparing stats values


<table class="heatMap-2">
<thead>
<tr>
  <th>Model</th>
  <th>Dataset</th>
  <th>MAE train</th>
  <th>MAE val</th>
  <th>MSE train</th>
  <th>MSE val</th>
</tr>
</thead>
<tbody>
<tr>
  <td>PilotNet</td>
  <td>Old</td>
  <td>5.16e⁻3</td>
  <td>0.028</td>
  <td>2.6e⁻4</td>
  <td>5.63e⁻3</td>
</tr>
<tr>
  <td>PilotNet</td>
  <td>Explicit</td>
  <td>2.39e⁻3</td>
  <td style="color:red">3.03e⁻3</td>
  <td>5.39e⁻3</td>
  <td style="color:red">4.39e⁻3</td>
</tr>
<tr>
  <td>PilotNet</td>
  <td>OpenCV(fastest)</td>
  <td>4.40e⁻3</td>
  <td>5.46e⁻3</td>
  <td>1.67e⁻3</td>
  <td>6.45e⁻3</td>
</tr>
<tr>
  <td>Deepest LSTM</td>
  <td>Old</td>
  <td>-</td>
  <td>0.047</td>
  <td>-</td>
  <td>8.27e⁻3</td>
</tr>
<tr>
  <td>Deepest LSTM</td>
  <td>Explicit</td>
  <td>0.023</td>
  <td>0.02</td>
  <td>3.73e⁻3</td>
  <td style="color:red">3.39e⁻3</td>
</tr>
<tr>
  <td>Deepest LSTM</td>
  <td>OpenCV(fastest)</td>
  <td>0.018</td>
  <td style="color:red">0.016</td>
  <td>4.16e⁻3</td>
  <td>3.82e⁻3</td>
</tr>
<tr>
  <td>Frankenstein</td>
  <td>Old</td>
  <td>0.032</td>
  <td>0.044</td>
  <td>3.49e⁻3</td>
  <td>6.32e⁻3</td>
</tr>
<tr>
  <td>Frankenstein</td>
  <td>Explicit</td>
  <td>0.016</td>
  <td style="color:red">0.015</td>
  <td>2.05e⁻3</td>
  <td style="color:red">2.14e⁻3</td>
</tr>
<tr>
  <td>Frankenstein</td>
  <td>OpenCV(fastest)</td>
  <td>0.019</td>
  <td>0.018</td>
  <td>3.9e⁻3</td>
  <td>3.5e⁻3</td>
</tr>
</tbody>
</table>


## Comparing V and W of each brain


<table>
<thead>
<tr>
  <th>Dataset</th>
  <th>V min</th>
  <th>V max</th>
  <th>W min</th>
  <th>W max</th>
</tr>
</thead>
<tbody>
<tr>
  <td>Old</td>
  <td style="background: #E5E3C9">-0.6</td>
  <td style="background: #E5E3C9">13</td>
  <td style="background: #B4CFB0">-3</td>
  <td style="background: #B4CFB0">3</td>
</tr>
<tr>
  <td>Explicit</td>
  <td style="background: #E5E3C9">-0.6</td>
  <td style="background: #E5E3C9">13</td>
  <td style="background: #B4CFB0">-3</td>
  <td style="background: #B4CFB0">3</td>
</tr>
<tr>
  <td>OpenCV(fastest)</td>
  <td style="background: #E5E3C9">6.5</td>
  <td style="background: #E5E3C9">24</td>
  <td style="background: #B4CFB0">-7.1</td>
  <td style="background: #B4CFB0">7.1</td>
</tr>
</tbody>
</table>
