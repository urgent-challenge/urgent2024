---
layout: page
permalink: /submission/
title: Submission
description:  
nav: true
nav_order: 6
---


The submission system will be open from June 10, 2024, to September 20, 2024 (23:59:59 AoE).

### Submission format and requirements

* Each submission should be **a zip file** containing two parts:
    1. enhanced audios corresponding to the test set;
    2. a Markdown (README.md) file containing the basic information about the submission (as listed below). The template can be found [here](/urgent2024/template).
        * team information (team name, affiliation, team mambers)
        * description of the training & validation data used for the submission
        * description of pre-trained models used for the submission (if applicable)
* The zip file should be named as `{your_teamname}.zip`. Here, `{your_teamname}` should be replaced with your team name.
* The zip file should only contain a single Markdown (README.md) file and a folder named `enhanced` that contains all the enhanced audio files. That is, the directory structure after executing `unzip {your_teamname}.zip` should be as follows:

```bash
./
├── README.md
└── enhanced/
    ├── fileid_1.flac
    ├── fileid_2.flac
    ├── ...
    └── fileid_N.flac
```
* Please encode all audio files in the 16-bit [**FLAC**](https://xiph.org/flac/) format to reduce the file size.
    * The audio files should be encoded in mono-channel with its original sampling frequency.
    * All audio files should be named as the original audio files in the test set.
* The submission should be directly sent to the organizers via email at [urgent.challenge@gmail.com](mailto:urgent.challenge@gmail.com).
  * The subject of the email should be `URGENT2024 Submission from team {your_teamname}`.
* Each team can submit up to **2 submissions per day** during the challenge.
  * The third and later submissions will be ignored. The quota will be reset at 00:00 AoE every day.
  * No submission will be accepted after the deadline (23:59:59 AoE, Septermber 20, 2024).
* For each team, only the submission with the best leaderboard performance will be used for the final evaluation.


> Submissions that fail to conform to the above requirements may be rejected.
>
> Should you encounter any problem during the submission, please feel free to [contact the organizers](mailto:urgent.challenge@gmail.com).

### Agreement

By submitting the results, the participants agree to the following conditions:

<d-code block language="markdown">
As a condition of submission, entrants grant the organizers, a perpetual,
irrevocable, worldwide, royalty-free, and non-exclusive license to use,
reproduce, adapt, modify, publish, distribute, publicly perform, create a
derivative work from, and publicly display the submitted audio signals and
CSV files (containing the performance scores).

The main motivation for this condition is to donate the submitted audio
signals and corresponding performance scores to the community as a
voice quality dataset.
</d-code>