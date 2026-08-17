# MDES Annotation Information

This document describes the categorical labels and trial-level annotations
provided with MDES.

## 1. Annotation Organization

Each participant is provided with trial-level annotation information
corresponding to the 35 emotion-elicitation trials.

Participant-specific annotation files use the same anonymized participant IDs
as the physiological recordings, for example:

- `S003.csv`
- `S004.csv`
- `S005.csv`

Trial IDs and video IDs can be used to match annotations to physiological
recordings.

## 2. Five-Class Labels

The five-class emotion-recognition benchmark uses the following label mapping:

| Label | Emotion |
|---|---|
| 0 | Despair |
| 1 | Fear |
| 2 | Anxiety |
| 3 | Calmness |
| 4 | Excitement |

The five-class label is stored in the `label5` field.

## 3. Two-Class Labels

For the within-subject binary benchmark, the five emotions are grouped into
Negative and Non-negative categories.

| Label | Class | Included emotions |
|---|---|---|
| 0 | Negative | Despair, Fear, Anxiety |
| 1 | Non-negative | Calmness, Excitement |

The binary label is stored in the `label2` field.

## 4. Full Trial-Level Annotation Fields

The complete annotation file contains the following fields:

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

## 5. Intended and Participant-Reported Labels

`video_emotion` and `video_label` describe the intended affective category
assigned to the stimulus.

`emotion` and `label5` describe the participant-level categorical label derived
from the post-stimulus self-assessment.

These two labels are retained separately to support analyses of both stimulus
intention and participant-reported affective experience.

## 6. Continuous Self-Assessments

Participants provided continuous self-ratings for:

- Excitement
- Anxiety
- Fear
- Despair
- Calmness
- Psychological discomfort
- Physiological discomfort

These continuous ratings are retained in the annotation files in addition to
the categorical emotion labels.

## 7. Trial and Video Correspondence

For example:

`trial01, video09`

corresponds to the physiological recording:

`trial01_video09.mat`

Trial order was randomized across participants. Therefore, `trial01` does not
necessarily correspond to the same video for different participants.

## 8. Participant Metadata

A separate participant-information file provides de-identified participant
characteristics used in the dataset analyses.

Only de-identified research-relevant variables are included in the released
metadata.

## 9. Stimulus Metadata

A separate stimulus metadata file provides available information for the
emotion-elicitation videos, including:

- video ID;
- intended emotion;
- stimulus duration;
- title or description, when available;
- original source information or URL, when available.

For stimuli whose original title or source URL cannot be reliably recovered,
the corresponding field is marked as `NA`.
