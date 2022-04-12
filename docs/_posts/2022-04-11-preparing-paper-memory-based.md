---
title: "Wrapping up ideas"
excerpt: "Wrapping up ideas"


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


# Current networks status updated


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
  <td>✅(increasing it/s much)</td>
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
  <td>✅(increasing it/s)</td>
  <td>❌</td>
  <td>✅(over the grass)</td>
  <td>✅</td>
  <td>❌</td>
</tr>
<tr>
  <td>Frankenstein</td>
  <td>Old</td>
  <td>✅(increasing it/s)</td>
  <td>✅</td>
  <td>✅(over the grass)</td>
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
  <td>✅(increasing it/s)</td>
  <td>✅(increasing it/s)</td>
  <td>✅(over the grass and increasing it/s)</td>
  <td>✅(increasing it/s)</td>
  <td>✅(increasing it/s)</td>
</tr>
<tr>
  <td>PilotNet 3D</td>
  <td>Old</td>
  <td>✅(increasing it/s)</td>
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


## Conclusions

* The brain "matches" the PID controller performance learning from the examples in the different circuits
* The neural brains need more it/s due to the inference time (this depends on the hardware). The conclusion is that the more it/s the better.
* Generalization. The neural brains are able to complete a broad variety of circuits. The memory based brain even more.
* We present a new neural architecture based on memory and some datasets.
* All open source and reproducible.


----





## Ideas


### Generalization

* Generalization: the neural brain trained on the fastest dataset is still able to complete circuits modifying the red line to a white line (simple circuit) modifying the 
number of iterations per seconds. The number of iterations per second is key in this case due to inference time.

### Importance of number of iterations 


* Importance of number of iterations per seconds: when the number of iterations per second on the brain is low, the performance degrades a lot due to this fact and its combination with the 
inference time needed. 


* Adding more iterations per second improves the performance of the PID controller? Yes, lowering for example the time to complete a circuit. Time to complete a lap with more it/s -> 50s
* Same question for neural brains? Same answer. For PilotNet, the time to complete a lap in simple with more it/s is 51s

--- 

#### Simple circuit
* Lap seconds PID -> 52s \|\|  with improved it/s: 50 s
* Lap seconds PilotNet -> \|\|  with improved it/s: 51 s
* Lap seconds TinyPilotNet -> 52 s \|\|  with improved it/s: 46 s
* Lap seconds Frankenstein with dataset with more extreme cases -> 65 s \|\| with improved it/s: 56 s


#### Montmeló line

* Lap seconds PID -> 71 s (56 it/s simulated) | 78 s (11 it/s simulated)
* Lap seconds TinyPilotNet -> 83 s (14 it/s simulated)


--- 

* Lap seconds PID -> 12it/s -> 5.23 8it/s -> 5.35 \|\|  with improved it/s: 
* Lap seconds PilotNet -> \|\|  with improved it/s: 
* Position deviation  MAE Frankenstein with dataset with more extreme cases -> 8 it/s ->19.03 \|\| with improved it/s:



* What happens when the number of iterations is the same?
* Comparing memory vs memory-less approaches. Differences?

#### Frankenstein is not fully trained.

[Image of training error curves]

The training curves show that the training hasn't finished, so a longer training could help in this scenario.


#### What happens if images are modified?

If the line is white instead of red, the PID based brain can't drive. PilotNet and Frankenstein are still able to complete 
part of the circuit.


#### Possible training strategy

Train a memory based model with several outputs, for example the same amount of outputs as inputs. 
With this training, the model should be able to output t, t+1 and t+2 speeds given as input t, t-1, t-2. 

