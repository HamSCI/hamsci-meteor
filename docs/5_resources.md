---
layout: page
title: Resources
permalink: /resources/
---

## Introduction
{:.no_toc}

Reading and viewing for newcomers to meteor scatter. The first list is the homework set at the kickoff meeting. Most of the documents are kept in the [HamSCI/MSQP](https://github.com/HamSCI/MSQP) repository.

## Table of Contents
{:.no_toc}
* TOC
{:toc}

## Start here

- **Meteor scatter overview.** J. A. Weitzen and W. T. Ralston (1988), [*Meteor Scatter: An Overview*](https://github.com/HamSCI/MSQP/blob/main/Weitzen_and_Ralston_Meteor_scatter_an_overview.pdf), *IEEE Transactions on Antennas and Propagation*, 36(12). An invited tutorial review of meteor burst communication.
- **Meteor scatter physics for operators.** Rob Suggs (NN4NT), [*Forward Scatter Meteor Radar: The Science Behind the Pings*](https://www.hamsci.org/sites/default/files/article/Workshop_2026/Meteor_Scatter_Science_Behind_the_Pings_HamSCI_conference_RevB.pdf), HamSCI Workshop, March 2026. Also available as a [video on Ham Radio 2.0](https://www.youtube.com/watch?v=1pgrXqg435g).
- **What a CW forward-scatter network can do.** Balis et al. (2025), [*Enhanced meteoroid trajectory and speed reconstruction using a forward scatter radio network: Pre-t0 phase technique and uncertainty analysis*](https://github.com/HamSCI/MSQP/blob/main/Radio%20Science%20-%202025%20-%20Balis%20-%20Enhanced%20Meteoroid%20Trajectory%20and%20Speed%20Reconstruction%20Using%20a%20Forward%20Scatter%20Radio%20Network.pdf), *Radio Science*, 60, e2025RS008305, [doi:10.1029/2025RS008305](https://doi.org/10.1029/2025RS008305).
- **The classic reference.** D. W. R. McKinley, *Meteor Science and Engineering* (1961), chapters [7](https://github.com/HamSCI/MSQP/blob/main/McKinley%20Meteor%20Science%20chapter%207.pdf), [8](https://github.com/HamSCI/MSQP/blob/main/McKinley%20Meteor%20Science%20chapter%208.pdf), and [9](https://github.com/HamSCI/MSQP/blob/main/McKinley%20Meteor%20Science%20chapter%209.pdf).
- **The MSK144 protocol.** S. J. Franke (K9AN) and J. H. Taylor (K1JT), [*The MSK144 Protocol for Meteor-Scatter Communication*](https://github.com/HamSCI/MSQP/blob/main/MSK144_Protocol_QEX.pdf), *QEX*, July/August 2017.
- **A professional meteor radar.** [Introduction to the Canadian Meteor Orbit Radar (CMOR)](https://aquarid.physics.uwo.ca/research/radar/cmor_intro.html).

## Operating in the MSQP

- [MSQP announcement and results](https://hamsci.org/msqp)
- [How-to Guide](https://www.hamsci.org/node/984) for monitoring and completing meteor scatter contacts
- [MSQP Operating Guidelines](https://www.hamsci.org/msqp-rules) for recording and submitting data
- [How to find, zip, and upload your WAV files to Zenodo](https://github.com/HamSCI/MSQP/blob/main/Zenodo.md)
- [MSQP research questions](https://github.com/HamSCI/MSQP/blob/main/Research%20Questions.md)

## Software

- [HamSCI/meteor-scatter](https://github.com/HamSCI/meteor-scatter): an MSK144 meteor-ping recorder and decoder for [ka9q-radio](https://github.com/ka9q/ka9q-radio), part of the HamSCI SIGMOND station software. It records and decodes the 10 m and 6 m MSK144 channels, and can report the resulting spots to PSKReporter.

## Terminology

- **Meteoroids** are small pieces of material in space, from dust grains to sand grains in size, mostly cometary (about 90%) and partly asteroidal (about 10%). Shower meteoroids follow the orbits of particular comets and asteroids; sporadic meteoroids come mostly from comet families.
- **Meteors** are meteoroids burning up in the atmosphere. Their visible light comes mostly from the ionization of the atmosphere.
- **Meteorites** are the pieces that reach the ground.
- **Underdense** trails have a low enough electron line density that each electron scatters independently. Their echoes are short and decay exponentially with the e-folding time *T*<sub>un</sub> (see [Goals]({{ '/goals/' | relative_url }})).
