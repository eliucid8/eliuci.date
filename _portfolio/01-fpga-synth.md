---
title: "FPGA MIDI Synthesizer"
excerpt: "A polyphonic synthesizer that interfaces with MIDI instruments, all running on a custom soft-core FPGA"
header:
    overlay_image: /assets/images/synth-mid-build.jpg
    overlay_filter: "0.7"
    teaser: /assets/images/synth-mid-build.jpg
    # video:
    #     id: 1bHtXSqo0AJeKrj7kuaZBhUttnHXL6bu_
    #     provider: google-drive
# sidebar:
#   - title: "Role"
#     image: http://placehold.it/350x250
#     image_alt: "logo"
#     text: "Designer, Front-End Developer"
#   - title: "Responsibilities"
#     text: "Reuters try PR stupid commenters should isn't a business model"
# gallery:
#   - url: /assets/images/unsplash-gallery-image-1.jpg
#     image_path: assets/images/unsplash-gallery-image-1-th.jpg
#     alt: "placeholder image 1"
#   - url: /assets/images/unsplash-gallery-image-2.jpg
#     image_path: assets/images/unsplash-gallery-image-2-th.jpg
#     alt: "placeholder image 2"
#   - url: /assets/images/unsplash-gallery-image-3.jpg
#     image_path: assets/images/unsplash-gallery-image-3-th.jpg
#     alt: "placeholder image 3"
order: 1
---
### February 2024 - April 2024

This was our final project for ECE 350 - Digital Systems.
After [designing our own processors]({{eliu}}{% link _portfolio/02-fpga-cpu.md %}), we were tasked with collaborating with a partner to "do something cool with \[them]." 
Annie and I decided on making a synthesizer, both of us being musicians and finalists in the Signals and Systems song competition. 
Our original idea was to also create mechatronic puppets that would "sing" along to the synthesizer as it was played: this would also allow us to flex our DSP muscles and implement some sort of spectrum analyzer.
However, the short 3-week period we were given to implement all of our ideas resulted in us dramatically tightening our scope.

In the end, we were still able to implement most of our goals. These included:
* Memory-mapped I/O
* MIDI input interface
* I2S audio output
* Waveform generation: Sawtooth, Square, Triangle, and Sine Waves
* Pitch Bend
* Polyphonic Synthesis
* Spectrum Analyzer: FFT-inspired Discrete Cosine Transform
* WS2812b LED interface (not successfully integrated)

Of course, this list does not do this project justice, so here's a video:

{% include video id="1bHtXSqo0AJeKrj7kuaZBhUttnHXL6bu_" provider="google-drive" %}

If you're interested, you can view the software and FPGA files for this project on GitHub: [https://github.com/eliucid8/ECE350-midisynth](https://github.com/eliucid8/ECE350-midisynth)
