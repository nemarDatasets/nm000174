# Imagined Speech EEG dataset comparing paradigm designs (Aguilera-Rodriguez et al. 2025)

## Overview

An EEG dataset of imagined speech from 15 healthy participants comparing traditional cue-based and gamified (Pac-Man maze) paradigms for brain-computer interface applications. The dataset comprises 1,800 trials across four Spanish directional commands (avanzar, retroceder, derecha, izquierda) recorded at 500 Hz from 24 electrodes using the mBrainTrain Smarting system. This derivative dataset enables systematic evaluation of paradigm design effects on imagined speech decoding performance.

## Dataset Summary

| Property | Value |
|---|---|
| Subjects | 15 |
| Channels | 24 |
| Classes | 4 |
| Trial length | 4 s |
| Sampling frequency | 500 Hz |
| Sessions | 1 |
| Total trials | 1800 |
| Paradigm | MotorImagery |

## Data Collection Methods

EEG data were acquired from 15 healthy participants (8 male, 7 female, ages 18-27) using a 24-channel mBrainTrain Smarting system at 500 Hz sampling rate with FCz reference and Fpz ground. Two experimental paradigms were compared: (1) traditional cue-based with visual and auditory cues (5 beeps at 1.4s rhythm) followed by 7 imagined speech repetitions, with the last 3 repetitions extracted for analysis, and (2) gamified paradigm using a Pac-Man maze interface with 1.4s periods for movement decision, imagined speech, and vocalized speech. Each participant completed 2 sessions with 120 trials per session (30 per class), yielding 450 trials per class across the dataset. The final dataset contains the last 3 imagined speech repetitions per trial from the traditional paradigm.

## How to Access via MOABB

Install MOABB and load this dataset directly:

```python
from moabb.datasets import AguileraRodriguez2025
from moabb.paradigms import MotorImagery
paradigm = MotorImagery()

dataset = AguileraRodriguez2025()
X, y, metadata = paradigm.get_data(dataset)
```

For more details see the [MOABB documentation](https://moabb.neurotechx.com/) and the
[MOABB dataset page](https://moabb.neurotechx.com/docs/generated/moabb.datasets.AguileraRodriguez2025.html).

## Citation

If you use this dataset please cite the primary publication:

> DOI: [10.1038/s41597-025-05926-5](https://doi.org/10.1038/s41597-025-05926-5)

## NEMAR / MOABB Benchmark Collection

This BIDS-formatted dataset was converted from the original data using the
[MOABB](https://moabb.neurotechx.com/) pipeline and re-hosted on
[NEMAR](https://nemar.org/) as part of the MOABB benchmark collection.
The original data and license terms apply — see `dataset_description.json` for details.
