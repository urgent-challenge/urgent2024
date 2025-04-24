---
layout: default
title: About
permalink: /
subtitle: Transfer Learning, Domain Adaptation, Bio Signal, Brain Decoding, Electroencephalogram, Event-Related Potential

profile:
  align: right
  image: 
  image_circular: false # crops the image to make it circular
  address: >

news: true  # includes a list of news items
selected_papers: false # includes a list of papers marked as "selected={true}"
social: false  # includes social icons at the bottom of the page

bibliography: about.bib
---


<div style="padding: 20px; text-align: center;">
  <img alt="introduction" src="assets/eeg2025.png" style="max-width: 100%;" />
</div>

<!-- <p>We can also cite <d-cite key="VoiceFixer-Liu2022"></d-cite> external publications.</p>

<d-math block>
  \mathbb{E}_{z \sim q_\phi(z|x)}
</d-math>

Hi <d-footnote>This is a footnote.</d-footnote> how are you?

<d-code block language="python">
import torch

if isinstance(speech_mix, np.ndarray):
    speech_mix = torch.as_tensor(speech_mix)
</d-code> -->

## The 2025 EEG Decoding Challenge

The 2025 EEG Decoding Challenge: From Cross-Task to Learning Subject Invariance Representation for EEG Decoding is a biosignal challenge submitted to the [**NeurIPS 2025 Competition Track**](https://neurips.cc/Conferences/2025/CallForCompetitions). This competition aims to advance the field of EEG decoding by addressing two critical challenges:

1. **Cross-Task Transfer Learning**: Developing models that can effectively transfer knowledge from passive EEG tasks to active tasks
2. **Subject Invariance Representation**: Creating robust representations that generalize across different subjects while predicting clinical factors



## Competition Tasks

### Task 1: Cross-Task Transfer Learning
Participants will train models on passive EEG tasks (Resting State, Surround Suppression, Movie Watching) and evaluate their performance on active tasks (Contrast Change Detection, Sequence Learning, Symbol Search). The goal is to develop models that can effectively transfer knowledge across different cognitive tasks.

### Task 2: Subject Invariance Representation
Teams will develop models that can predict clinical factors (p-factor, internalizing, externalizing, and attention) while maintaining robustness across different subjects. This task focuses on creating subject-invariant representations that generalize well to unseen individuals.

## Dataset

The competition dataset includes EEG recordings from over 3,000 participants across six distinct cognitive tasks:

### Passive Tasks
- **Resting State (RS)**: Eyes open/closed conditions with fixation cross
- **Surround Suppression (SuS)**: Four flashing peripheral disks with contrasting background
- **Movie Watching (MW)**: Four short films with different themes

### Active Tasks
- **Contrast Change Detection (CCD)**: Identifying dominant contrast in co-centric flickering grated disks
- **Sequence Learning (SL)**: Memorizing and reproducing sequences of flashed circles
- **Symbol Search (SyS)**: Computerized version of WISC-IV subtest

Each participant's data is accompanied by four psychopathology dimensions derived from the Child Behavior Checklist (CBCL).

## Workshop

Top-ranking teams will be invited to present their work at a dedicated workshop during the NeurIPS 2025 conference (December 14-15, 2025). 

## Motivation

EEG decoding faces significant challenges due to signal heterogeneity from various factors like non-stationarity, noise sensitivity, inter-subject morphological differences, varying experimental paradigms, and differences in sensor placement. While recent advances in machine learning have shown promise, there remains a critical need for models that can generalize across different subjects and tasks without expensive recalibration.

This competition aims to address these challenges by:
1. Providing a large-scale, diverse dataset for evaluating model generalization
2. Encouraging the development of robust, transferable EEG decoding methods
3. Establishing benchmarks for cross-task and cross-subject performance
4. Fostering collaboration between machine learning and neuroscience communities

