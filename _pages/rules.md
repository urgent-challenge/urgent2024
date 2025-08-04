---
layout: page
permalink: /rules/
title: Rules
description:  
nav: true
nav_order: 4

---

The rules provided to contestants are as follows:

- **Evaluation and testing will be done on the downsampled data.** To ensure timely evaluation, we will downsample the data to 100 Hz after filtering the data to the 0.5-50 Hz range. The down sampled datasets will be used for evaluation and testing. The downsmapling script is available on the [downsample-datasets](https://github.com/eeg2025/downsample-datasets) repository.
- Contestants are allowed and encouraged to use any datasets for pre-training. However, they must clearly mention and document any additional data sources used in their submission.
- Contestants are allowed to use existing foundation models, but they must clearly mention and document which pre-trained models were used and how they were fine-tuned in their submission.
- Contestants must submit their code during the inference stage; this is a code submission competition.
- Models must be able to run on a single GPU with 20 GB of memory at the inference stage. Contestants are encouraged to validate their models on a similar machine before submitting their code.
- Related members from the organizing team can participate but are ineligible for prizes.
- The top 10 teams will have their code released after the final submission.

## Evaluation Criteria

### Challenge 1: Cross-Task Transfer Learning
- Mean Absolute Error (MAE) - 40%
- Coefficient of Determination (R²) - 20%
- Area Under ROC Curve (AUC-ROC) - 30%
- Balanced Accuracy - 10%

### Challenge 2: Psychopathology Factor Prediction
- Concordance Correlation Coefficient (CCC) - 50%
- Root Mean Square Error (RMSE) - 30%
- Spearman's Rank Correlation - 20%

### Overall Ranking
- Challenge 1 contributes 40% to final score
- Challenge 2 contributes 60% to final score
