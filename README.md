# MDES: A Large-Scale Multimodal Physiological Dataset for Fine-Grained Emotion Recognition with Adjacent Negative States

## Overview

MDES is a multimodal physiological emotion dataset designed for fine-grained affective computing, with particular emphasis on adjacent negative emotional states. The dataset contains synchronized EEG and peripheral/ocular physiological recordings collected under a controlled video-based emotion elicitation protocol.

The current release is intended for **non-commercial academic research** and is distributed through a **controlled-access application procedure**.

## Dataset Summary

- **Participants:** 90 quality-controlled participants
- **Trials:** 3,150 complete trials
- **Stimuli:** 35 screened emotion-elicitation videos
- **Target emotions:** Excitement, Anxiety, Fear, Despair, and Calmness
- **Modalities:** EEG, ECG, PPG, EDA, RSP, EMG, EOG, and SKT
- **Recording duration:** approximately 70 hours of synchronized multimodal recordings
- **Annotations:** intended stimulus labels and trial-level participant self-assessments
- **Benchmark protocols:** within-subject cross-trial binary classification and cross-subject five-class classification

## Data Access

MDES is available to qualified researchers for non-commercial academic use through controlled access.

To request access:

1. Download the **MDES Data Access Application** from this repository.
2. Complete the applicant, institution, project, and intended-use information.
3. Read and sign the data-use terms.
4. Send the signed application to the contact email listed below.
5. Applications will be reviewed before access instructions are issued.

**Contact:** ye.li@siat.ac.cn

Please use an institutional email address whenever possible.

## Basic Data-Use Terms

By receiving access to MDES, users agree to:

- use the dataset only for the approved non-commercial academic research project;
- not redistribute, upload, sell, sublicense, or otherwise provide the dataset or access credentials to third parties;
- not attempt to identify or re-identify any participant;
- store the data securely and restrict access to approved research personnel;
- cite the MDES paper in publications or presentations that use the dataset;
- comply with applicable institutional ethics, privacy, and data-protection requirements.

Detailed terms are provided in the application form.

## Repository Contents

```text
MDES/
├── README.md
├── access/
│   └── MDES_Data_Access_Application.pdf
├── docs/
│   ├── dataset_structure.md
│   └── signal_information.md
├── code/
│   ├── feature_extraction/
│   ├── benchmark_splits/
│   └── SAGE-Net/
└── examples/
    └── example_metadata/
```

The repository structure above may be completed progressively. At minimum, the access application and basic dataset documentation should be available when the paper is submitted.

## Citation

Citation information will be provided after the manuscript is publicly available.

## Notes on Released Materials

The exact files included in an approved release will be described in the access approval message and accompanying dataset documentation. Any materials subject to third-party copyright or other distribution restrictions will only be shared when legally permitted.

## License / Access Policy

This repository provides documentation, code, and the controlled-access application. Access to the dataset itself is granted only after approval of a signed application. Approval is project-specific and does not authorize redistribution to other individuals or groups.
