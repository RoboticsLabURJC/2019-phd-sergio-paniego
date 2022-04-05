---
title: "New dataset vs old dataset comparison"
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
  <td>NEW</td>
  <td>✅</td>
  <td>❌(last turns)</td>
  <td>❌(some turns ok)</td>
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
  <td>NEW</td>
  <td>✅</td>
  <td>❌</td>
  <td>❌</td>
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
  <td>NEW</td>
  <td>❌</td>
  <td>❌</td>
  <td>❌</td>
  <td>❌</td>
  <td>❌</td>
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
  <td>NEW</td>
  <td>❌</td>
  <td>❌</td>
  <td>❌</td>
  <td>❌</td>
  <td>❌</td>
</tr>
</tbody>
</table>