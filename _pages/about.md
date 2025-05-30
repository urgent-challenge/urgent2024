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

news: false  # includes a list of news items
selected_papers: false # includes a list of papers marked as "selected={true}"
social: false  # includes social icons at the bottom of the page

bibliography: about.bib
---

# EEG Foundation Challenge: From Cross-Task to Cross-Subject EEG Decoding

The 2025 EEG Decoding Challenge: From Cross-Task to Learning Subject Invariance Representation for EEG Decoding is a biosignal challenge accepted to the [**NeurIPS 2025 Competition Track**](https://neurips.cc/Conferences/2025/CallForCompetitions). This competition aims to advance the field of EEG decoding by addressing two critical challenges:

1. **Cross-Task Transfer Learning**: Developing models that can effectively transfer knowledge from passive EEG tasks to active tasks
2. **Subject Invariance Representation**: Creating robust representations that generalize across different subjects while predicting clinical factors

Check the complete proposal [here](https://eeg2025.github.io/assets/files/proposal.pdf)


## Competition Tasks

<div style="padding: 20px; text-align: center;">
  <img alt="introduction" src="https://eeg2025.github.io/assets/img/workflow.png" style="max-width: 100%;" />
  <p style="text-align: left; margin-top: 10px; font-family: sans-serif; font-size: 0.9e">
    <b>Figure 1</b>: HBN-EEG Dataset and Data split. <b>A.</b> EEG is recorded using a 128-channel system during active tasks (i.e., with user input) or passive tasks. <b>B.</b> The psychopathology and demographic factors. <b>C.</b> The datasets split into Train, Test and Validation. Details in <b><a href="https://eeg2025.github.io/assets/files/proposal.pdf">subsection 1.2 for the proposal.</a></b>
  </p>
</div>

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


## Institution Organization

<div style="padding: 20px; text-align: center;">
  <div style="display: flex; justify-content: space-around; align-items: center; flex-wrap: wrap; margin-bottom: 20px;">
    <img src="https://eeg2025.github.io/assets/logos/ups.png" style="max-width: 30%; margin: 10px;" alt="Université Paris-Saclay Logo" />
    <img src="https://eeg2025.github.io/assets/logos/lisn.png" style="max-width: 30%; margin: 10px;" alt="LISN Logo" />
    <img src="https://eeg2025.github.io/assets/logos/ucsd.png" style="max-width: 30%; margin: 10px;" alt="UCSD Logo" />
  </div>
  <div style="display: flex; justify-content: space-around; align-items: center; flex-wrap: wrap; margin-bottom: 20px;">
    <img src="https://eeg2025.github.io/assets/logos/inria.png" style="max-width: 30%; margin: 10px;" alt="Inria Logo" />
    <img src="https://eeg2025.github.io/assets/logos/icm.png" style="max-width: 30%; margin: 10px;" alt="Paris Brain Institute (Institut du Cerveau – ICM) Logo" />
    <img src="https://eeg2025.github.io/assets/logos/radboud.png" style="max-width: 30%; margin: 10px;" alt="Radboud University Logo" />
  </div>
  <div style="display: flex; justify-content: space-around; align-items: center; flex-wrap: wrap; margin-bottom: 20px;">
    <img src="https://eeg2025.github.io/assets/logos/chalearn.png" style="max-width: 30%; margin: 10px;" alt="ChaLearn Logo" />
    <img src="https://eeg2025.github.io/assets/logos/mind_intitute.png" style="max-width: 30%; margin: 10px;" alt="Child Mind Institute Logo" />
    <img src="https://eeg2025.github.io/assets/logos/nki.jpg" style="max-width: 30%; margin: 10px;" alt="Nathan Kline Institute for Psychiatric Research Logo" />
  </div>
  <div style="display: flex; justify-content: space-around; align-items: center; flex-wrap: wrap; margin-bottom: 20px;">
    <img src="https://eeg2025.github.io/assets/logos/meta.png" style="max-width: 30%; margin: 10px;" alt="Meta Logo" />
    <img src="https://eeg2025.github.io/assets/logos/ben_logo.png" style="max-width: 30%; margin: 10px;" alt="Ben-Gurion University of the Negev Logo" />
    <img src="https://eeg2025.github.io/assets/logos/ufabc.png" style="max-width: 30%; margin: 10px;" alt="Federal University of ABC (UFABC) Logo" />
  </div>
<div style="display: flex; justify-content: space-around; align-items: center; flex-wrap: wrap; margin-bottom: 20px;">
    <img src="https://eeg2025.github.io/assets/logos/cneuro.jpg" style="max-width: 10%; margin: 10px;" alt="Cuban Neuroscience Center (CNEURO) Logo" />
    <img src="https://eeg2025.github.io/assets/logos/UESTC.png" style="max-width: 30%; margin: 10px;" alt="University of Electronic Science and Technology of China Logo" />
    <img src="https://eeg2025.github.io/assets/logos/cnrs.png" style="max-width: 10%; margin: 10px;" alt="CNRS Centre National de la Recherche Scientifique Logo" />
    <img src="https://eeg2025.github.io/assets/logos/mcgill.png" style="max-width: 25%; margin: 10px;" alt="McGill University Logo" />
  </div>
</div>