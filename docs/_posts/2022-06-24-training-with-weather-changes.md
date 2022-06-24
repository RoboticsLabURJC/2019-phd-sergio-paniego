---
title: "Training models with weather changes"
excerpt: "Comparing performance with new training procedure"


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

# MAE & MSE metrics comparison between models trained without and with weather changes.

| Model        | Weather changes training | MAE train | MAE val | MAE test | MSE train | MSE val | MSE test |
|--------------|--------------------------|-----------|---------|----------|-----------|---------|----------|
| PilotNet     | -                        | 0.0044    | 0.00546 | 0.0851   | 0.00016   | 0.00064 | 0.0576   | 
| PilotNet     | YES                      | 0.0083    | 0.0067  | -        | 0.00100   | 0.00060 | -        | 
| Deepest      | -                        | 0.018     | 0.0016  | 0.1202   | 0.00416   | 0.00382 | 0.0508   | 
| Deepest      | YES                      | -         | -       | -        | -         | -       | -        | 
| PilotNetx3   | -                        | 0.0044    | 0.0048  | 0.0738   | 0.00018   | 0.00032 | 0.044    | 
| PilotNetx3   | YES                      | 0.0126    | 0.0075  | -        | 0.00209   | 0.00058 | -        | 
| Frankenstein | -                        | 0.019     | 0.018   | 0.0694   | 0.0039    | 0.0035  | 0.0436   | 
| Frankenstein | YES                      | 0.025     | 0.016   | -        | 0.0051    | 0.0027  | -        | 