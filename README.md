# Spontaneous_movements

# IMU Spontaneous Movement Bout Detection

This repository contains code for detecting spontaneous upper-limb movement bouts from infant wrist-worn IMU data. Algorithm adapted from Trujillo-Priego et al. (2017).

## Overview

The pipeline:
1. Loads raw accelerometer and gyroscope files.
2. Converts units.
    - Acceleration: g → m/s²
    - Angular velocity: deg/s → rad/s
3. Computes signal magnitude.
4. Identifies synchronization tap peaks.
5. Trims the recording to the analysis window.
6. Detrend signal by subtracting the median.
7. Full-wave rectify signal.
8. Apply moving average smoothing (31 samples).
9. Estimate individualized acceleration threshold.
10. Estimate individualized angular velocity threshold.
11. Identify time points exceeding both thresholds.
12. Merge adjacent detections into movement bouts.
13. Calculate bout metrics:
   - Mean duration
   - Total movement time
   - Movement proportion

## Repository structure

- `scripts/`: runnable analysis scripts
- `data_example/`: example input data
- `output_example/`: example output files
- `docs/`: method notes and workflow documentation
- `archive/`: original development scripts

## Main outputs

- Bout start/end times
- Bout duration
- Mean bout duration
- Total movement time
- Movement time proportion