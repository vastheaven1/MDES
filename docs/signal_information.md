# MDES Signal Information

This document describes the physiological signal organization, channel order,
sampling rates, and trial-file variables in MDES.

## 1. Signal Modalities

MDES contains 40 synchronized physiological channels, including:

- 32 EEG channels
- 2 PPG channels
- 1 RSP channel
- 1 ECG channel
- 1 EOG channel
- 1 EMG channel
- 1 EDA channel
- 1 SKT channel

## 2. Channel Order

The channel order is fixed across participants and trials.

The complete channel list and fixed channel order are also provided in:

`metadata/channel_information.csv`

### EEG channels

| Channel ID | Channel |
|---|---|
| 01 | Fp1 |
| 02 | PO3 |
| 03 | Fp2 |
| 04 | F7 |
| 05 | F3 |
| 06 | Fz |
| 07 | F4 |
| 08 | F8 |
| 09 | FC5 |
| 10 | FC1 |
| 11 | FC2 |
| 12 | FC6 |
| 13 | AF3 |
| 14 | T7 |
| 15 | C3 |
| 16 | Cz |
| 17 | C4 |
| 18 | T8 |
| 19 | AF4 |
| 20 | CP5 |
| 21 | CP1 |
| 22 | CP2 |
| 23 | CP6 |
| 24 | P7 |
| 25 | P3 |
| 26 | Pz |
| 27 | P4 |
| 28 | P8 |
| 29 | PO4 |
| 30 | O1 |
| 31 | Oz |
| 32 | O2 |

### Peripheral and ocular channels

| Channel ID | Channel |
|---|---|
| 33 | PPG1 |
| 34 | PPG2 |
| 35 | RSP |
| 36 | ECG |
| 37 | EOG |
| 38 | EMG |
| 39 | EDA |
| 40 | SKT |

## 3. Sampling Rates

- Raw aligned recordings: **500 Hz**
- Preprocessed recordings: **250 Hz**

The preprocessed version contains the corresponding filtered and downsampled
signals used for subsequent analysis.

## 4. Trial File Format

Each physiological trial is stored as a MATLAB `.mat` file.

A typical raw aligned trial contains the following variables:

| Variable | Description |
|---|---|
| `data` | 40 × N physiological signal matrix |
| `channels` | Modality information for the 40 channels |
| `lengths` | Sample lengths of the baseline, stimulation, and complete trial |
| `sampling_rate` | Sampling rate in Hz |

The first dimension of `data` follows the fixed channel order listed above.

## 5. Trial Segments

The `lengths` structure contains:

- `baseline`: number of baseline samples
- `stimulate`: number of stimulus-period samples
- `total`: total number of samples

where:

`total = baseline + stimulate`

Because the emotion-elicitation videos have different durations, the number
of samples may vary across trials.

## 6. Signal Units

The physical units of the released physiological signals are:

| Modality | Unit |
|---|---|
| EEG | µV |
| PPG | V |
| RSP | V |
| ECG | mV |
| EOG | mV |
| EMG | mV |
| EDA | µS |
| SKT | °C |
The released data should be interpreted according to the units specified in
the accompanying channel-information file.
