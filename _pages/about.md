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

## The 2025 EEG decoding Challenge

The 2025 EEG decoding challenge: From  Cross-Task to learning subject invariance representation for EEG decoding is a biosignal challenge submitted by the [**NeurIPS 2025 Competition Track**](https://neurips.cc/Conferences/2025/CompetitionTrack). We aim to build universal EEG model...

## Goal

Based on the increasing interest in the generalizability of EEG decoding models, we propose the EEG (Foundation Model) Challenge that aims to: 

1. **Establish a benchmark dataset** for EEG decoding, encompassing diverse tasks and subjects.
2. **Promote the development of generalizable EEG decoders** that perform robustly across diverse subjects and tasks.
3. **Provide a set of varied benchmark tasks** for comprehensive evaluation.
4. **Offer a computational framework** to streamline data and metadata handling, accelerating deep model training.

## Dataset Description

The competition dataset includes EEG recordings from over 3,000 participants across six distinct cognitive tasks, divided into passive and active categories (Table 1). Each participant's data is accompanied by four psychopathology dimensions (internalizing, externalizing, attention, and p-factor) derived from a bifactor model of parent-reported questionnaire responses to the Child Behavior Checklist (CBCL) [Achenbach1999-ey, Scopel-Hoffmann2022-sy]. These psychopathology factors represent orthogonal dimensions of mental health and serve as target variables for the regression component of the competition.

**Overview of HBN-EEG tasks used in the competition.**

| Category | Task                     | Description                                                   | Key Features                                                                   |
|----------|--------------------------|---------------------------------------------------------------|--------------------------------------------------------------------------------|
| Passive  | Resting State (RS)       | Eyes open/closed conditions with fixation cross               | Pre-recorded voice instructions, event-marked transitions                        |
|          | Surround Suppression (SuS)| Four flashing peripheral disks with contrasting background    | Parametrized foreground/background stimuli, ~3.6 min duration per run           |
|          | Movie Watching (MW)      | Four short films with different themes                        | Includes animation, drama, and educational content                              |
| Active   | Contrast Change Detection (CCD) | Identifying dominant contrast in co-centric flickering grated disks | Includes response time and performance feedback                               |
|          | Sequence Learning (SL)   | Memorizing and reproducing sequences of flashed circles       | Age-adjusted difficulty (10 or 7 sequences), multiple repetitions              |
|          | Symbol Search (SyS)      | Computerized version of WISC-IV subtest                       | Target symbol identification among distractors                                  |


## Task Introduction

**1. Cross-task Transfer Learning**
[Train on passive tasks and predict active tasks.]

**2. Subject Invariance Representation**
[Predicting clinical factors, including p-factor, internalizing, externalizing, and attention.]

## Communication

[Slack/Discord]

## Workshop

Top-ranking teams will be invited to a dedicated workshop in the NeurIPS 2025 conference (December 14 or December 15, 2025). More information will be provided after the challenge is completed.

<!-- ## Paper Submission

Participants may feel free to submit their system description paper to any conference. -->

## Motivation

EEG decoding faces significant challenges due to signal heterogeneity from various factors like non-stationarity, noise sensitivity, inter-subject morphological differences, varying experimental paradigms, and differences in sensor placement. Though strong decoding performance has been shown in various settings 

[insert past approaches, including competitions like BEETL/Sleep data/Motor imagery ...] 

the field still suffers from poor generalization to new subjects, tasks, and even new recording of the same subject and task over time without expensive re-calibration.

While the shift towards training more complex non-linear models on larger datasets in machine learning community has motivated innovation in model developments in EEG decoding, there is a lack of a large-scale dataset with diversity that can be used to evaluate the generalization of these models. 

To address this, we introduce a large-scale dataset featuring EEG recordings from over 3,000 subjects across six distinct cognitive tasks, captured with 128 channels.

