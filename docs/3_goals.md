---
layout: page
title: Goals
permalink: /goals/
mermaid: true
---
## Goals
{:.no_toc}

The kickoff meeting on 9 September 2026 set out the working group's goals in three groups: science, communications engineering, and ham radio. They will be refined as the group works. The longer list of research questions behind the Meteor Scatter QSO Party is in [MSQP Research Questions](https://github.com/HamSCI/MSQP/blob/main/Research%20Questions.md).

## Table of Contents
{:.no_toc}
* TOC
{:toc}

## Background: why wavelength matters

A meteoroid entering the atmosphere at 10 to 70 km/s ionizes the air along its path, and the free electrons in the trail scatter radio signals over the horizon. Two relations from McKinley's *Meteor Science and Engineering* (1961) shape most of the goals below.

- **Scattered power** from an underdense trail goes as the cube of the wavelength, λ³, and the square of the electron line density, *q* (McKinley eq. 9-3). The longest usable wavelength should therefore give the strongest echoes. At HF, ionospheric effects dominate, so lower VHF (40 to 100 MHz) is the best compromise. By this argument, 10 m should outperform 6 m.
- **Echo duration** of an underdense trail, *T*<sub>un</sub> = λ² sec²φ / (16π²*D*), goes as the square of the wavelength and inversely as the electron diffusion coefficient, *D* (φ is half the forward-scatter angle). Because *D* depends on the altitude at which the meteoroid ablates, and faster meteoroids ablate higher, echo duration also depends on meteor speed.

## Science goals

- **Compare 10 m and 6 m (and perhaps 2 m)** for:
  - the wavelength dependence of received power, *P*<sub>r</sub>, and underdense echo duration, *T*<sub>un</sub>;
  - the echo height ceiling for meteors of different speeds and ablation altitudes.
- **Determine meteor speeds.** This may require CW transmitters; [Balis et al. (2025)](https://github.com/HamSCI/MSQP/blob/main/Radio%20Science%20-%202025%20-%20Balis%20-%20Enhanced%20Meteoroid%20Trajectory%20and%20Speed%20Reconstruction%20Using%20a%20Forward%20Scatter%20Radio%20Network.pdf) show what a forward-scatter CW network can do.
- **Determine the range to meteors**, as one part of the orbit problem. An open question is whether time difference of arrival (TDOA) with a special waveform could do this; the short duration of the bursts makes it difficult.
- **Contribute data on meteor fragmentation**, which appears as "blooming" of a CW signal.

## Communications engineering goals

- **Predict optimal times and paths** for meteor scatter data transmission, including the radiant geometry of sporadic meteors from the NASA Meteoroid Engineering Model. Students of Jay Weitzen (AC1SN) have been working on a sporadic-meteoroid communications tool.
- An open question from the kickoff meeting: could JS8Call be used with MSK144?

## Ham radio goals

- **Is 10 m really better than 6 m** for meteor scatter? The physics above says it should be. The MSQP recordings can say whether it is.

## Signals the group could use

| Signal | Notes |
| --- | --- |
| Amateur MSK144 | The mode used in the MSQP |
| Pure CW | May be needed to measure meteor speeds |
| Digital TV pilot tones | Echo counts show diurnal variation (example below) |
| Canadian analog TV video carriers | |

As an example of the pilot-tone approach, the NASA Marshall Space Flight Center Amateur Radio Club (NN4SA) counts underdense echoes of DTV channel 3 pilot tones at 60.3085 MHz (USB), from several transmitters in range, using an Icom R8500 receiver, a dipole 6 ft above ground, and echo-counting software written by Rob Suggs (NN4NT). The counts show diurnal variation.

## Ways to collect data

- **Personal Space Weather Station (PSWS).** Its receiver covers up to 60 MHz. The HamSCI SIGMOND station software already decodes MSK144, through the [meteor-scatter](https://github.com/HamSCI/meteor-scatter) client.
- **RTL-SDR receivers with resonant antennas**, which could record 10 m and 6 m MSK144 as well as digital and analog TV carriers.
- **Correlation with optical meteor networks**, such as the [Global Meteor Network](https://globalmeteornetwork.org/).
