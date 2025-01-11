---
title: "Pipelined FPGA CPU"
excerpt: "A MIPS-inspired CPU design with a 5-stage pipeline, all running at 50 MHz on an FPGA."
header:
    overlay_image: /assets/images/processorBanner.png
    overlay_filter: "0.7"
    teaser: /assets/images/processorBanner.png
order: 2
---
### February 2024 - April 2024

In this project, I designed a MIPS-inspired 5-stage pipelined processor in Verilog and synthesized it for an Artix-7 FPGA, from scratch.
It features microarchitectural optimizations such as full bypassing, pipeline stalls, and a 1-cycle Dadda Tree multiplier.
I also designed custom fixed-point arithmetic instructions and memory-mapped IO with the goal of accelerating digital signal processing operations. These features were used heavily in my [synthesizer]({{eliu}}{% link _portfolio/01-fpga-synth.md %}) project.
When synthesized, it can run at a clock speed of 50 MHz.

During the development of this project, I also became more familiar with shell scripting, which allowed me to efficiently run regression tests on my processor as changes were made.
Alongside GTKWave, these shell scripts allowed me to tease out bugs in my designs. This project simply would have been impossible without them.

This project taught me much about Verilog, digital system design, digital signal processing, and the importance of good developer and validation tools.
