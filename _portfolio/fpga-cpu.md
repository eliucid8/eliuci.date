---
title: "Pipelined FPGA CPU"
excerpt: "A MIPS-inspired CPU design with a 5-stage pipeline, all running at 50 MHz on an FPGA."
header:
    overlay_image: /assets/images/processorBanner.png
    overlay_filter: "0.7"
    teaser: /assets/images/processorBanner.png
---

In this project, I: 
* Designed a MIPS-inspired 5-stage pipelined processor using Structural Verilog and developer tools written in Python and Bash.
* Implemented common microarchitectural optimizations such as full bypassing, pipeline stalls, and a Dadda Tree multiplier.
* Designed custom fixed-point arithmetic instructions and memory-mapped IO with the goal of accelerating digital signal processing
