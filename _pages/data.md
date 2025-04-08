---
layout: page
permalink: /data/
title: Data
description:  
nav: true
nav_order: 3

bibliography: data.bib
---

### Data description

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
