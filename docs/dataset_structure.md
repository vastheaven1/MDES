# MDES Dataset Structure

This document describes the organization and naming conventions of the MDES dataset.

## Dataset Organization

A typical approved MDES release is organized by participant and trial:

```text
MDES/
├── subject_001/
│   ├── trial_001/
│   │   ├── eeg.*
│   │   ├── ecg.*
│   │   ├── ppg.*
│   │   ├── eda.*
│   │   ├── rsp.*
│   │   ├── emg.*
│   │   ├── eog.*
│   │   ├── skt.*
│   │   └── metadata.*
│   ├── trial_002/
│   └── ...
├── subject_002/
└── ...
