---
layout: page
permalink: /baseline/
title: Starter&nbsp;Kit
description:  
nav: true
nav_order: 5

---

The starter kit will be released following the timeline details, to give equal opportunities to people who cannot download the dataset, and will depend on our infrastructure to run the code.

This code relies on the [Braindecode](https://braindecode.org) and [EEGDash](https://eegdash.org) libraries. These libraries allow data search, loading, fetching, and readily applying deep learning methods on EEG data. The provided scripts are only for reference, and the contestants can freely use their codebase for development.

## Challenge 1: Cross-Task Transfer Learning Data

For Challenge 1, participants will have access to the following data for validation and test phases:

**EEG Data:**
- **Surround Suppression (SuS) task**: Complete EEG recordings from the passive paradigm
- **Pre-trial epochs**: 2-second EEG data segments preceding each contrast change event (see figure below)
- **Recording specifications**: 128-channel high-density EEG at standard sampling rate

**Additional Features:**
- **Demographics**: Age, sex (gender), and handedness (Edinburgh Handedness Questionnaire scores)
- **Psychopathology factors**: Four bifactor model dimensions (p-factor, internalizing, externalizing, attention)

**Target Variables** (validation only):
- Response time relative to contrast change onset (regression target)
- Success rate/hit accuracy (classification target)

Formally, let **X** ∈ ℝ^(c×t) be an EEG recording segment with c=128 channels and t time steps, and **P** ∈ ℝ^7 be subject's traits including 3 demographic attributes and 4 psychological factors. Participants can choose which data modalities to utilize in their models.

<div style="text-align: center; margin: 20px 0;">
  <img src="https://eeg2025.github.io/assets/img/CCD_sequence.png" alt="CCD Trial Sequence" style="max-width: 80%; height: auto;">
  <p style="font-size: 0.9em; color: #666; margin-top: 10px;">
    <strong>Figure:</strong> Exemplar Contrast Change Detection (CCD) trial sequence showing the 2-second pre-trial epochs (hatched regions) that will be provided as input data for Challenge 1.
  </p>
</div>

## Challenge 2: Psychopathology Factor Prediction Data

For Challenge 2, participants will have access to the following data for validation and test phases:

**EEG Data:**
- **Multi-task recordings**: EEG data from all available cognitive paradigms (passive and active tasks)
- **Minimum data requirement**: Only subjects with ≥15 minutes of total EEG data included (>78% of participants)
- **Recording specifications**: 128-channel high-density EEG across multiple experimental sessions

**Input Features:**
- **Demographics**: Age, sex (gender), and handedness (Edinburgh Handedness Questionnaire scores)
- **EEG recordings**: Complete datasets from multiple cognitive tasks per subject

**Target Variables** (validation only):
- **P-factor**: General psychopathology factor (continuous score)
- **Internalizing**: Inward-focused traits dimension (continuous score) 
- **Externalizing**: Outward-directed traits dimension (continuous score)
- **Attention**: Focus and distractibility dimension (continuous score)

All psychopathology factors are derived from Child Behavior Checklist (CBCL) responses using a bifactor model, providing orthogonal, privacy-preserving dimensional measures of mental health.

---

**Note:** Starter kit code samples and baseline model implementations will be added following the competition timeline. Participants are encouraged to explore the data structure and develop their approaches using the validation set during the warm-up phase.
