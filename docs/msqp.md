---
layout: page
title: Meteor Scatter QSO Party
permalink: /msqp/
---

The Meteor Scatter QSO Party (MSQP) is HamSCI's recurring meteor scatter operating event. During each target meteor shower, operators on 10 m and 6 m (and some on 2 m) listen, make contacts using the MSK144 digital mode, and upload the WAV files of their decodes for later scientific analysis. The full announcement, the leader board of data contributors, and past results are at [hamsci.org/msqp](https://hamsci.org/msqp).

**Next event:** the Geminids, 13--15 December 2026.

## Table of Contents
{:.no_toc}
* TOC
{:toc}

## Taking part

- New to meteor scatter? Start with the [How-to Guide](https://www.hamsci.org/node/984) for advice on monitoring and completing meteor scatter contacts.
- To contribute data, follow the [MSQP Operating Guidelines](https://www.hamsci.org/msqp-rules), which explain how to record and submit data for scientific analysis.
- Upload your WAV files to the [HamSCI community on Zenodo](https://zenodo.org/communities/hamsci), following the step-by-step [Zenodo upload instructions](https://github.com/HamSCI/MSQP/blob/main/Zenodo.md). Each upload receives its own DOI.

## Showers observed so far

| Year | Showers |
| --- | --- |
| 2025 | Perseids, Geminids |
| 2026 | Eta Aquariids, Daytime Arietids, Southern Delta Aquariids, Perseids, Geminids (13--15 December) |
| 2027 | Quadrantids (2--4 January) |

Together these showers cover an assortment of meteor speeds and radiant geometries (declinations).

## 2026 target showers

| Shower | Code | Dates | Peak (UT) | Approx. ZHR | Speed (km/s) | Parent object | Radiant (RA, Dec) | Notes |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Eta Aquariids | ETA | 5--7 May 2026 | 6 May 2026, 16:30 | 75 | 66 | 1P/Halley | 22h33m, −01° | |
| Daytime Arietids | ARI | 9--11 June 2026 | 10 June 2026, 02:03 | 49 | 38 | 96P/Machholz or 1566 Icarus | 03h02m, +25° | |
| Southern Delta Aquariids | SDA | 29--31 July 2026 | 30 July 2026, 00:39 | 20 | 41 | 96P/Machholz | 22h40m, −16° | |
| Perseids | PER | 12--14 August 2026 | 13 August 2026, 14:09 | 92 | 59 | 109P/Swift-Tuttle | 03h13m, +58° | Circumpolar north of 32° latitude |
| Geminids | GEM | 13--15 December 2026 | 14 December 2026, 13:00 | 90 | 35 | 3200 Phaethon | 07h28m, +33° | |
| Quadrantids | QUA | 2--4 January 2027 | 3 January 2027, 06:38 | 65 | 41 | 2003 EH1 (196256) | 15h18m, +49° | Circumpolar north of 41° latitude; peak from the 2026 forecast |

*ZHR is the zenithal hourly rate. Values are from the working group kickoff slides (9 September 2026). The [complete shower table](https://hamsci.org/sites/default/files/article/MSQP/2026%20MS%20Data%20from%20NN4NT.png) at hamsci.org also gives approximate radiant rise, transit, and set times.*

## Data collected

- **PSKReporter spots** of MSK144 decodes.
- **WAV files uploaded to Zenodo.** The recordings allow individual meteors to be identified and the underdense echo decay time, *T*<sub>un</sub>, to be measured. Station geometry is known to the accuracy of the 4-character grid squares in the decoded messages.

All MSQP datasets are listed on the [Results page]({{ '/results/' | relative_url }}).

## Past results

- [August 2025 (Perseids) MSQP results](https://www.hamsci.org/Aug-2025-MSQP-results)
- [December 2025 (Geminids) MSQP results](https://www.hamsci.org/Dec-2025-MSQP-results)

## Analysis so far

As of the kickoff meeting:

- A student senior research project is making a machine-learning pass through the 2025 recordings to identify meteor echoes and other propagation modes.
- A Python script plots each WAV file and extracts the decoded callsign and grid square (example on the [home page]({{ '/' | relative_url }})).
- **Still needed:** an automated measurement of *T*<sub>un</sub>, the e-folding time of underdense meteor echoes. This would test how *T*<sub>un</sub> depends on wavelength and on ablation altitude, and through altitude on meteor speed.
- **Still needed:** more participants, and volunteers to develop the analysis scripts and run them over the archive.
