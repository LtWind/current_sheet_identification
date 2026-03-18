# Current Sheet Identification

Automated identification of **current sheets (CSs)** in solar wind data based on the methodology from:

**Khabarova et al. (2021)**  
*Automated Identification of Current Sheets—A New Tool to Study Turbulence and Intermittency in the Solar Wind*

---

## Overview

This repository implements a pipeline for detecting current sheets in solar wind plasma using time-series data of magnetic field and plasma parameters.

Current sheets are thin structures with sharp magnetic field rotations and are key to:

- Turbulence and intermittency  
- Magnetic reconnection  
- Plasma heating  

---

## What this repo does

- Loads solar wind datasets (OMNI / WIND / ACE style)
- Computes derived physical parameters
- Applies threshold-based detection of current sheets
- Outputs detected events for further analysis or ML pipelines

---

## Data

Expected input format:

- Time-indexed solar wind data
- Magnetic field components (Bx, By, Bz or |B|)
- Plasma parameters:
  - Density
  - Velocity
  - Temperature

Typical sources:

- OMNI / OMNI2
- WIND
- ACE

---

## Method

The detection algorithm follows a **multi-parameter approach**:

- Magnetic field derivative (|B|′)
- Plasma beta (β)
- Alfvén speed ratio (VA / V)

A current sheet is detected when thresholds on these parameters indicate a sharp transition.

---

## Output

The pipeline produces:

- Timestamps of detected current sheets
- Associated plasma parameters
- Optional labels for ML usage

---

## Use Cases

- Solar wind classification
- Turbulence analysis
- ICME / sheath detection
- Feature engineering for ML models (LSTM, TCN, etc.)

---

## Reference

Khabarova, O., Sagitov, T., Kislov, R., & Li, G. (2021)  
Automated Identification of Current Sheets—A New Tool to Study Turbulence and Intermittency in the Solar Wind  
DOI: 10.1029/2020JA029099

---

## Author

Timofei Treves
