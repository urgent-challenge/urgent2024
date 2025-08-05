---
layout: page
permalink: /data/
title: Data
description:  
nav: true
nav_order: 3

bibliography: data.bib
---

**Table of Contents**

- [Data description](#data-description)
  - [Task-specific procedures](#task-specific-procedures)
  - [Psychopathology Dimensions and Demographics](#psychopathology-dimensions-and-demographics)
    - [Understanding the Four Psychopathology Dimensions](#understanding-the-four-psychopathology-dimensions)
    - [Bifactor Model and Advantages](#bifactor-model-and-advantages)
    - [Demographic Information](#demographic-information)
- [Downloading the Data](#downloading-the-data)
    - [Mini Releases (for initial exploration)](#mini-releases-for-initial-exploration)
    - [NEMAR.org](#nemarorg)
        - [Option 1: NEMAR.org direct download](#option-1-nemarorg-direct-download)
        - [Option 2: EEGDash API](#option-2-eegdash-api)
    - [OpenNeuro and its API](#openneuro-and-its-api)
        - [Option 3: OpenNeuro direct download](#option-3-openneuro-direct-download)
        - [Option 4 and 5: OpenNeuro API](#option-4-and-5-openneuro-api)
    - [Option 6: Amazon S3](#option-6-amazon-s3)
- [References](#references)

## Data description

The competition dataset includes EEG recordings from over 3,000 participants across six distinct cognitive tasks, divided into passive and active categories (see table below). Each participant's data is accompanied by four psychopathology dimensions (internalizing, externalizing, attention, and p-factor) derived from a bifactor model of parent-reported questionnaire responses to the Child Behavior Checklist (CBCL). These psychopathology factors represent orthogonal dimensions of mental health and serve as target variables for the regression component of the competition.

More details about the **dataset download links**, task-specific procedures, video recordings of the experiment, and more can be found on **[the HBN-EEG dataset page](https://neuromechanist.github.io/data/hbn/)**.

**Overview of HBN-EEG tasks used in the competition.**

| Category | Task                     | Description                                                   | Key Features                                                                   |
|----------|--------------------------|---------------------------------------------------------------|--------------------------------------------------------------------------------|
| Passive  | Resting State (RS)       | Eyes open/closed conditions with fixation cross               | Pre-recorded voice instructions, event-marked transitions                        |
|          | Surround Suppression (SuS)| Four flashing peripheral disks with contrasting background    | Parametrized foreground/background stimuli, ~3.6 min duration per run           |
|          | Movie Watching (MW)      | Four short films with different themes                        | Includes animation, drama, and educational content                              |
| Active   | Contrast Change Detection (CCD) | Identifying dominant contrast in co-centric flickering grated disks | Includes response time and performance feedback                               |
|          | Sequence Learning (SL)   | Memorizing and reproducing sequences of flashed circles       | Age-adjusted difficulty (10 or 7 sequences), multiple repetitions              |
|          | Symbol Search (SyS)      | Computerized version of WISC-IV subtest                       | Target symbol identification among distractors                                  |

### Task-specific procedures

**Resting State.** In the Resting State task, participants rested their heads on a chin rest, looking forward at the computer screen with a fixation cross at the center of the screen. A pre-recorded voice instructed them to keep their eyes closed or open and fixate on the central cross during 'eyes open' periods. The timeline of the event markers for the task is shown in the figure.

<img src="https://eeg2025.github.io/assets/img/image.png" style="max-width: 100%;"/>

**Surround Suppression.** Participants observed a modified Surround Suppression stimulus sequence. Four flashing peripheral disks in the foreground were presented with a contrasting background in two runs, each ~3.6 minutes long. We imported and synchronized foreground and background stimulus parameters from the corresponding behavioral recording for each subject to complete the stimulus event description. Figure 5 shows an example of an actual event-marker stream during the Surround Suppression task.

<img src="https://eeg2025.github.io/assets/img/image-1.png"  style="max-width: 100%;"/>

**Movie Watching.** The final passive task involved watching movies. Participants were asked to watch four short movies with different themes and aims: (1) 'Despicable Me', (2) 'Diary of a Wimpy Kid', (3) 'Fun with Fractals', and (4) 'The Present' [1]. Details and rationale for the movie choices and links to access the presented movies are available in the top-level _eeg.json files. The recorded event markers for each movie presentation include only the start and stop times. We will soon introduce methods and remodeling tools to insert custom event sequences for each movie relative to these event anchors (movie presentation start and stop) so researchers will be able to plug in an event stream of choice.

**Contrast Change Detection.** In this task, two co-centric flickering grated disks (one with left-leaning gratings and one with right-leaning gratings) appear on the screen. After a randomly selected time, one of the two flickering grated disks on the screen changes contrast. Participants were asked to identify the left-leaning or right-leaning grated disk with dominant contrast as soon as they could identify the disk. Based on their responses, feedback (a smiley face or sad face) was presented. We imported participant responses from the behavioral recordings and assembled HED descriptions for the main task and the respective subject responses.

<img src="https://eeg2025.github.io/assets/img/image-2.jpg"  style="max-width: 100%;"/>

**Sequence learning.** Participants were shown a sequence of 10 (or 7 if <8 years old) flashed circles among 8 (or 6) possible and predetermined targets positioned on the periphery of a larger invisible circle on the screen (Figure 7). The same sequence was repeated five times, and after each repetition, participants were asked to repeat the sequence using a computer mouse. The participant's response sequence was recorded for each repetition, but unfortunately, the timestamps of these responses were not recorded. Because of the difference in the target and sequence counts, we divided this task into two tasks: a six-target task and an eight-target task. The task is based on a similarly designed sequence learning experiment by Steinemann [24].

<img src="https://eeg2025.github.io/assets/img/image-4.png"  style="max-width: 100%;"/>

**Symbol search.** The final task in the interactive battery of experiments involves an emulation of a standard neuropsychological test (a subset of the Wechsler Intelligence Scale for Children IV, WISC-IV [25]) on the computer screen, in which participants were asked to confirm if either of the target symbols in each row was present among the five search symbols in the same row (Figure 8). The test was presented to the participants in 15-row sequences, and participants were asked to go to the next set of sequences once they responded to all 15 rows. Since each of the 15 questions was presented simultaneously, only the times when participants pressed the mouse button to respond were recorded.

### Psychopathology Dimensions and Demographics
The p-factor and psychopathology dimensions are broad, dimensional measures of mental health derived from the Child Behavior Checklist (CBCL), a parent-report tool for assessing behavioral and emotional traits in children and adolescents.

#### Understanding the Four Psychopathology Dimensions
**P-factor (General Psychopathology Factor):** The p-factor captures a general tendency for various psychological traits to co-occur, reflecting overall emotional and behavioral vulnerability.

**Internalizing:** This dimension reflects inward-focused traits such as emotional sensitivity, withdrawal, or somatic complaints.

**Externalizing:** This dimension describes outward-directed traits like impulsivity, activity level, or rule-challenging behaviors.

**Attention:** This dimension measures traits related to focus, distractibility, and sustained attention.

#### Bifactor Model and Advantages
These four dimensions are derived using a bifactor model, which separates general psychopathology (p-factor) from specific, independent trait clusters. This statistical approach provides a nuanced, robust, and privacy-preserving summary of mental health by transforming raw questionnaire responses into anonymized, stable factor scores. **This method reduces noise, increases stability and generalizability, and enhances statistical power, while protecting participant privacy by avoiding the use of raw, potentially identifiable responses.** Researchers can thus study neural correlates of mental health traits with greater confidence in both confidentiality and scientific rigor.

#### Demographic Information
Demographic variables available in the dataset include **age**, **sex** (male/female), and **handedness** as assessed by the Edinburgh Handedness Questionnaire. These variables enable researchers to control for or examine the effects of developmental stage, biological sex, and lateralization (such as biases in right-hand and left-hand button presses) in their analyses.

<img src="https://eeg2025.github.io/assets/img/image-5.jpg"  style="max-width: 100%;"/>

## Downloading the Data

The public part of the competition dataset contains 11 public releases, each between 91 and 245 GB. 
To facilitate downloading this large amount of data, we provide multiple different solutions, such that all setups and personal preferences are accommodated.
If you encounter difficulties downloading the data with one solution, we suggest you try using another one before filing an issue.
In addition, we provide **mini releases** that can be used for preliminary exploration of the data.

### Mini Releases (for initial exploration)
We provide a *mini release* for each release, that can be used for preliminary exploration of the data. 
Each mini release contains only 20 subjects, and represents approximately 15 GB of data.
These mini releases are available both as zip files and as Google Drive folders. 

The download links for the mini releases are available on the [dataset page](https://neuromechanist.github.io/data/hbn/).

### NEMAR.org
The releases are hosted on NEMAR. The releases 1-11 have the following names on NEMAR: 

```
ds005505, ds005506, ds005507, ds005508, ds005509, ds005510, ds005511, ds005512, ds005514, ds005515, ds005516
```

#### Option 1: NEMAR.org direct download
Each release can be downloaded as a single Zip file using a direct download link. For example the link to the download page of the first release is:

```
https://nemar.org/dataexplorer/detail?dataset_id=ds005505
```

#### Option 2: EEGDash API
The [EEGDash](https://github.com/sccn/EEGDash) python API allows you to download the data programmatically. 
For example, to download the first release, you can use the following code snippet:
```python
from eegdash import EEGDashDataset

dataset = EEGDashDataset({
    "dataset": "ds005505", 
    # "subject": "NDARAG340ERT",          # to download a specific subject
    # "task": "contrastChangeDetection",  # or a specific task
    # "run": 1,                           # or a specific run
})
```

### OpenNeuro and its API
The releases are also hosted on OpenNeuro. They have the same names as on NEMAR.org.

#### Option 3: OpenNeuro direct download
On OpenNeuro, the releases can also be downloaded using direct download links. For example the link to the download page of the first release is:

```
https://openneuro.org/datasets/ds005505
```

#### Option 4 and 5: OpenNeuro API

The [openneuro-py](https://pypi.org/project/openneuro-py/) library offers both a python API and a command line interface to download the data programmatically.

**Python API:**
```python
import openneuro

openneuro.download(dataset="ds005505")
```

**Command line interface:**
```bash
openneuro-py download --dataset=ds005505
```


### Option 6: Amazon S3

Finally, the releases are also hosted on Amazon S3. The releases can be found at the following S3 bucket:
```
s3://fcp-indi/data/Projects/HBN/BIDS_EEG/cmi_bids_R1
s3://fcp-indi/data/Projects/HBN/BIDS_EEG/cmi_bids_R2
s3://fcp-indi/data/Projects/HBN/BIDS_EEG/cmi_bids_R3
s3://fcp-indi/data/Projects/HBN/BIDS_EEG/cmi_bids_R4
s3://fcp-indi/data/Projects/HBN/BIDS_EEG/cmi_bids_R5
s3://fcp-indi/data/Projects/HBN/BIDS_EEG/cmi_bids_R6
s3://fcp-indi/data/Projects/HBN/BIDS_EEG/cmi_bids_R7
s3://fcp-indi/data/Projects/HBN/BIDS_EEG/cmi_bids_R8
s3://fcp-indi/data/Projects/HBN/BIDS_EEG/cmi_bids_R9
s3://fcp-indi/data/Projects/HBN/BIDS_EEG/cmi_bids_R10
s3://fcp-indi/data/Projects/HBN/BIDS_EEG/cmi_bids_R11
```
Having installed the [`AWS CLI`](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html), you can download a dataset using this command: `aws s3 cp <s3_uri> <local_path> --recursive --no-sign-request`, where the `<s3_uri>` can be any of the s3 addresses above.

For more details on how to download data from Amazon S3, please refer to the [Amazon S3 documentation](https://docs.aws.amazon.com/AmazonS3/latest/userguide/download-objects.html) or use the AWS CLI tool.

## References

- Seyed Yahya Shirazi, Alexandre Franco, Mauricio Scopel Hoffmann, Nathalia Esper, Dung Truong,
Arnaud Delorme, Michael Milham, and Scott Makeig. HBN-EEG: The FAIR implementation of the
healthy brain network (HBN) electroencephalography dataset. bioRxiv, page 2024.10.03.615261,
3 October 2024. doi: [10.1101/2024.10.03.615261](https://doi.org/10.1101/2024.10.03.615261).


<style>
/* Basic */

table {
border-spacing: 0px;
border-collapse: collapse;     /* Share borders between adjacent cells */
width: 100%;
max-width: 100%;
margin-bottom: 15px;
background-color: transparent; /* Change the background-color of table here */
text-align: left;              /* Change the text-alignment of table here */
}

th {
font-weight: bold;
border: 1px solid #cccccc;  /* Change the border-color of heading here */
padding: 8px;
}

td {
border: 1px solid #cccccc;  /* Change the border-color of cells here */
padding: 8px;
}

/* Stylized */

/* Adding Striped Effect for even rows */

tr {
/* background-color: transparent; Change the default background-color of rows here */
background-color: white; /* Change the default background-color of rows here */
}

tr:nth-of-type(2n) {
background-color: #f6f8fa;  /* Change the background-color of even rows here */
}

/* Reset styles for the shortcut helper */
.light-keys tr:nth-of-type(2n) {background-color: black;}
.light-keys tr:hover {background-color: black;}
.light-keys table {border: none;}
.light-keys tr {border: none;}
.light-keys td {border: none;}
.light-keys th {border: none;}

tr th {
background-color: white;    /* Change the background-color of heading here */
}

/* Adding Hover Effect for rows */

tr {
-moz-transition: background-color 300ms ease-in-out 0s;
-ms-transition: background-color 300ms ease-in-out 0s;
-o-transition: background-color 300ms ease-in-out 0s;
-webkit-transition: background-color 300ms ease-in-out 0s;
transition: background-color 300ms ease-in-out 0s;
}

tr:hover {
background-color: #fff176;  /* Change the hover background-color of rows here */
}
