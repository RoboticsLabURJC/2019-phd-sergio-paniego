---
title: "Analyzing experiments classification vs regression"
excerpt: "Different classification and regressions brains used."


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


# Increasing inference time causes the brain to perform worse.

As we can see on the following table, the more time the brain spends on inferencing, the lower the success ratio.

| Mean inference time | brain_iterations_frequency_simulated_time | Success ratio | 
|--|---|---|
| 0.1102177578 | 8.489471774 | 0 | 
| 0.1097273208 | 9.087081608 | 0 | 
| 0.1089397428 | 8.826833574 | 0 | 
| 0.108384775 | 8.611706416 | 0 | 
| 0.08469425758 | 10.39180166 | 0 | 
| 0.08176505948 | 11.83541062 | 0 | 
| 0.06180069967 | 18.54519817 | 0 | 
| 0.05832424202 | 16.10134917 | 40 | 
| 0.05663843244 | 16.91381077 | 10 | 
| 0.05654587854 | 16.74553374 | 10 | 
| 0.05617845177 | 17.19212514 | 30 | 
| 0.05601816702 | 17.0677267 | 40 | 
| 0.05587896598 | 16.54422074 | 100 | 
| 0.05159521093 | 17.27328385 | 90 | 
| 0.05100311045 | 17.98406404 | 40 | 
| 0.04423760964 | 18.3121465 | 80 | 
| 0.04390220998 | 18.23390419 | 100 | 
| 0.03166032962 | 18.57335699 | 70 | 
| 0.03142367519 | 18.17389982 | 80 | 
| 0.02815542527 | 17.7724807 | 30 | 
| 0.02796182987 | 18.45898923 | 30 | 
| 0.02129336391 | 19.6270721 |90 |


# Classification vs regression

* Brains with the highest success ratio are based on classification.
* Classification brains are much slower!
* Regression brains achieve a mean position deviation error close or even better than classification ones
* Regression is actually better than classification!

| Mode | net | net| Lap seconds | Mean Position deviation |  Success ratio | 
|--|---|---|---|---|
| classification | mobilenet_v3_small |	mobilenet_v3_large | 106.2 | 3.58 | 100 |
| classification | mobilenet_v3_small |	mobilenet_v3_large | 108.7 | 3.50 | 100 |
| regression | mobilenet_v3_large | mobilenet_v3_large | 91.11 | 3.18 | 90 |
| regression | pilotnet | pilotnet  | 96.11| 3.81 | 90 |
| regression | mobilenet_v3_small | mobilenet_v3_large | 88.5 | 2.24 | 80 |
| regression | mobilenet_v3_small | mobilenet_v3_large | 97.875 | 3.17 | 80 |








