# MDES Dataset Structure

This document describes the organization and naming conventions of the MDES dataset distributed through the controlled-access procedure.

MDES contains synchronized physiological recordings from 90 quality-controlled participants, with 35 emotion-elicitation trials per participant and 3,150 complete trials in total.

## 1. Dataset Organization

An approved MDES release contains aligned physiological recordings, preprocessed recordings, benchmark labels, detailed trial-level annotations, and dataset metadata.

A typical release is organized as follows:

```text
MDES/
├── raw_aligned/
│   ├── S003/
│   │   ├── trial01_video09.mat
│   │   ├── trial02_video27.mat
│   │   ├── trial03_video29.mat
│   │   └── ...
│   ├── S004/
│   └── ...
│
├── preprocessed/
│   ├── S003/
│   │   ├── trial01_video09.mat
│   │   ├── trial02_video27.mat
│   │   └── ...
│   ├── S004/
│   └── ...
│
├── labels/
│   ├── five_class/
│   │   ├── S003.csv
│   │   ├── S004.csv
│   │   └── ...
│   ├── two_class/
│   │   ├── S003.csv
│   │   ├── S004.csv
│   │   └── ...
│   └── full_annotations/
│       ├── S003.csv
│       ├── S004.csv
│       └── ...
│
└── metadata/
    ├── channel_information.csv
    ├── participant_information.csv
    └── stimulus_metadata.csv
