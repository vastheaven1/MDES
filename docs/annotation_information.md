# MDES Annotation Information

This document describes the three types of annotation and metadata information
provided with MDES:

1. participant-specific trial-level annotations;
2. participant metadata;
3. stimulus metadata.

## 1. Trial-Level Annotations

Detailed trial-level annotations are provided separately for each participant.

The annotation filename uses the same anonymized participant ID as the
physiological recordings.

Examples:

- `S003.csv`
- `S004.csv`
- `S005.csv`

Each file contains 35 rows corresponding to the 35 emotion-elicitation trials
completed by that participant.

Trial IDs and video IDs can be used to match annotations to the corresponding
physiological recordings.

For example:

`trial01, video09`

corresponds to:

`trial01_video09.mat`

The presentation order was randomized across participants. Therefore,
`trial01` does not necessarily correspond to the same stimulus video for
different participants.

### 1.1 Five-Class Labels

The five-class emotion-recognition benchmark uses the following label mapping:

| Label | Emotion |
|---|---|
| 0 | Despair |
| 1 | Fear |
| 2 | Anxiety |
| 3 | Calmness |
| 4 | Excitement |

The five-class label is stored in the `label5` field.

### 1.2 Two-Class Labels

For the within-subject binary benchmark, the five emotions are grouped into
Negative and Non-negative categories.

| Label | Class | Included emotions |
|---|---|---|
| 0 | Negative | Despair, Fear, Anxiety |
| 1 | Non-negative | Calmness, Excitement |

The binary label is stored in the `label2` field.

### 1.3 Annotation Fields

Each participant-specific annotation file contains the following fields:

| Field | Description |
|---|---|
| `trial_id` | Trial order within the participant session |
| `video_id` | Identifier of the presented stimulus video |
| `emotion` | Participant-reported categorical emotion |
| `label2` | Binary Negative/Non-negative label |
| `label5` | Five-class participant-reported emotion label |
| `video_emotion` | Intended emotion category of the stimulus |
| `video_label` | Numerical label of the intended stimulus category |
| `excitement` | Participant self-rating of excitement |
| `anxiety` | Participant self-rating of anxiety |
| `fear` | Participant self-rating of fear |
| `despair` | Participant self-rating of despair |
| `calm` | Participant self-rating of calmness |
| `psychological_discomfort` | Psychological discomfort rating |
| `physiological_discomfort` | Physiological discomfort rating |
| `watched_video` | Prior-exposure information for the stimulus |

`video_emotion` and `video_label` describe the intended affective category
of the stimulus.

`emotion` and `label5` describe the participant-level categorical label
derived from the post-stimulus self-assessment.

The intended stimulus labels and participant-reported labels are retained
separately.

### 1.4 Continuous Self-Assessments

The participant-specific annotation files also contain continuous self-ratings
for:

- Excitement
- Anxiety
- Fear
- Despair
- Calmness
- Psychological discomfort
- Physiological discomfort

These ratings are retained in addition to the categorical benchmark labels.

---

## 2. Participant Metadata

Participant-level information is provided in a separate file:

`participant_information.csv`

This file contains one row per participant and uses the same anonymized
participant IDs as the physiological recordings and trial-level annotation
files.

The released participant metadata include:

- participant ID;
- sex;
- age;
- height;
- weight;
- psychology-background information, when available.

Only de-identified research-relevant participant information is included in
the released file.

---

## 3. Stimulus Metadata

Stimulus-level information is provided in a separate file:

`stimulus_metadata.csv`

This file contains one row for each of the 35 emotion-elicitation videos.

Available information includes:

- video ID;
- intended emotion category;
- video title or description, when available;
- original source or URL, when available.

For stimuli whose original title or source URL cannot be reliably recovered,
the corresponding field is marked as `NA`.
