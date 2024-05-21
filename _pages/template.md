---
layout: page
permalink: /template/
title: Template for README.md in each submission
description:  
nav: false
nav_order: 10
---

```markdown
# Basic information

- team: {your_teamname}
- team members:
  - {member_name1} (affiliation1)
  - {member_name2} (affiliation2)
  - {member_name3} (affiliation3)


# Data description

Training data: simulated on the fly using the official configuration

Validation data: same as official validation data (39 hours)


# Additional information

If any pre-trained model is used to develop the speech enhancement system, please provide its information below. For example:

Model 1
- Pre-trained model: HuBERT-Large
- Link: https://huggingface.co/facebook/hubert-large-ll60k
- Usage: used for converting the input speech signal into discrete tokens

Model 2
- Pre-trained model: EnCodec
- Link: https://github.com/facebookresearch/encodec
- Usage: used for generating compressed speech features
```
