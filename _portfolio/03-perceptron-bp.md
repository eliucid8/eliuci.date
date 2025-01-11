---
title: "Perceptron Branch Predictor"
excerpt: "Research, implementation, and simulation of a machine learning-inspired branch predictor in microarchitecture."
header:
    overlay_image: /assets/images/perceptron-bp-diagram.png
    overlay_filter: "0.7"
    teaser: /assets/images/perceptron-bp-diagram.png
order: 3
---
### October 2024 - November 2024

This was a research project for ECE 552 - Advanced Computer Architecture I, in collaboration with [Han Zhang](https://linkedin.com/in/han-zhang-2sk34).

Han and I elected to research/reproduce the perceptron branch predictor, a design inspired by machine learning techniques. This concept was first described by Jiminez and Lin in [*Dynamic Branch Prediction with Perceptrons*](https://ieeexplore.ieee.org/document/903263).

The general design of this predictor maintains a list of weights, which are combined with the global history of the branch predictor in order to determine a predicted branch outcome.
The weights of this predictor are then trained in the case of an incorrect or unconfident prediction to bias the predictor towards more confidence in correct predictions.
A real design will contain many perceptrons, each with their own weights, with the goal of allowing as many branches as possible to have a dedicated list of weights tracking branch outcomes.

We simultaneously implemented this design for the [BOOM core](https://boom-core.org/) and for [gem5](https://www.gem5.org), an architectural simulator. 
We verified that these two implementations had the same cycle-by-cycle functionality via microbenchmarks compiled for RISC-V. 
We were then able to run benchmarks such as [CoreMark](https://www.eembc.org/coremark/) in gem5 in order to efficiently benchmark the performance of this branch predictor, 
while also gaining insight into the area and power overheads of such a predictor by synthesizing our Chisel implementation through the [OpenROAD](https://theopenroadproject.org/) VLSI flow.

Through these results, we were able to gain insights into the tradeoff between area used (hardware budget) and performance of the predictor.
By analyzing the performance of many configurations of the predictor, we were able to verify the choices of optimal parameters for each hardware budget presented in the Jimenez and Lin paper.

{% include image.html file="history-length-hardware-budget.png" alt="Pareto Frontier of history length vs performance" caption="A graph showing our results for performance based on hardware budget and history length" %}

If desired, you can view our full final report [here](https://drive.google.com/file/d/119pvG79218wlF4r3N4nbrOQBsU9EFFjF/view?usp=sharing).
