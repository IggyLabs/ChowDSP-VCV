# ChowDSP for VCV

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Build Status](https://dev.azure.com/jatinchowdhury18/ChowDSP-VCV/_apis/build/status/jatinchowdhury18.ChowDSP-VCV?branchName=master)](https://dev.azure.com/jatinchowdhury18/ChowDSP-VCV/_build/latest?definitionId=1&branchName=master)

This repository contains [ChowDSP](https://ccrma.stanford.edu/~jatin/chowdsp) plugins built as VCV Rack modules.

To build these plugins, you must have the [VCV Rack development environment](https://vcvrack.com/manual/Building#building-rack-plugins) set up. Then use the following commands:
```bash
# clone repository
$ git clone https://github.com/jatinchowdhury18/ChowDSP-VCV.git

$ cd ChowDSP-VCV

$ make install
```

# Plugins

## CHOW Tape
<img src="./doc/ChowTape_cap.PNG" alt="Pic" height="300">

CHOW Tape is a port of the [CHOW Tape Model](https://github.com/jatinchowdhury18/AnalogTapeModel) audio plugin. Has controls for tape **bias**, **saturation**, and **drive**.

For more information on the physical modelling and signal processing happening internally, check out [this blog post](https://medium.com/@jatinchowdhury18/complex-nonlinearities-episode-3-hysteresis-fdeb2cd3e3f6) or for more technical readers, check out [this DAFx paper](http://dafx2019.bcu.ac.uk/papers/DAFx2019_paper_3.pdf) on tape modelling.

## CHOW Phaser
<img src="./doc/ChowPhaseFeedback_cap.PNG" alt="Pic" height="300">
<img src="./doc/ChowPhaseMod_cap.PNG" alt="Pic" height="300">

CHOW Phaser is made up two modules that together make up a port of the [CHOW Phaser](https://github.com/jatinchowdhury18/ChowPhaser) audio plugin. For a typical phaser effect, use a bipolar LFO as the CV input.

The **skew** knob emphasises different parts of the CV input, in a way inspired by the behaviour of Light-Dependent Resistors (LDRs).

<img src="https://miro.medium.com/max/800/1*Et0lRw3uBadjunDu1RPTrA.png" alt="Pic" height="300">

The Feedback module contains two modulating allpass stages arranged in a feedback architecture. The amount of feedback is controll by the **feedback** knob.

The Mod module contains a series of modulating allpass stages. The **mod** knob controls the mix of the modulated signal. The **stages** knob controls the number of allpass stages used.

## CHOW FDN
<img src="./doc/ChowFDN_cap.PNG" alt="Pic" height="300">

A [feedback delay network](https://ccrma.stanford.edu/~jos/cfdn/Feedback_Delay_Networks.html) reverb, with controls for **pre-delay**, room **size**, decay times (**T60 Low** and **T60 High**), and **dry/wet** mix. You can use up to 16 delay lines, but note that more delay lines will use more CPU.

## License

ChowDSP VCV Modules are licensed under the GPLv3 license. Enjoy!
