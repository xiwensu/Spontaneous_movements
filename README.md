# Spontaneous_movements

# IMU Spontaneous Movement Bout Detection

This repository contains code for detecting spontaneous upper-limb movement bouts from infant wrist-worn IMU data.

## Overview

The pipeline:
1. Loads raw accelerometer and gyroscope files.
2. Converts units.
3. Computes signal magnitude.
4. Identifies synchronization tap peaks.
5. Trims the recording to the analysis window.
6. Applies a 31-point moving average.
7. Detects movement candidate points using acceleration and gyroscope thresholds.
8. Identifies overlapping acceleration and gyroscope activity.
9. Groups detected points into movement bouts.
10. Computes session-level movement metrics.

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