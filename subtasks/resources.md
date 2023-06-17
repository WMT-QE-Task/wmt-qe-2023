---
layout: page
title: 'Additional training resources'
---

[Home](../index.md)


We provide below links to additional resources that can be used for training/augmentation.

# Task 1: Quality Prediction

 ## DA and post-edited annotation data

 For the subtasks using **DA annotations** for sentence level and **post-edited  annotations** for word-level, participants can use the annotations provided for the *Quality Estimation Shared Tasks* of the previous year(s) available on the MLQE-PE [github page](https://github.com/sheffieldnlp/mlqe-pe) or the [previous tasks section](previous.md). For a full description of the available language pairs and annotations please read the [MLQE-PE paper](https://arxiv.org/abs/2010.04480) and the [WMT QE 2022 findings paper](https://aclanthology.org/2022.wmt-1.3/).


The datasets were collected by translating sentences sampled from source language articles using state-of-the-art Transformer NMT models and annotated with a variant of Direct Assessment (DA) scores by professional translators. Each sentence was annotated following the FLORES setup, which presents a form of DA, where at least three professional translators rate each sentence from 0-100 according to the perceived translation quality. DA scores are standardised using the z-score by rater. Participating systems are required to score sentences according to z-standardised DA scores.

## MQM annotation data
For the subtasks using **MQM annotations** for sentence and word-level tasks, participants can use the annotations provided for the *Quality Estimation Shared Tasks* of 2022 available on [the github page](https://github.com/WMT-QE-Task/wmt-qe-2022-data/tree/main/train-dev_data/task1_mqm) or use the raw MQM scores from [https://github.com/google/wmt-mqm-human-evaluation](https://github.com/google/wmt-mqm-human-evaluation). For a full description of the available language pairs and annotations please read the [WMT QE 2022 findings paper](https://aclanthology.org/2022.wmt-1.3/). 

# Task 2: Fine-grained error span detection

For the subtasks using **MQM annotations** uswed for error span detection, participants can use the annotations provided for the *Metrics Shared Tasks* available on [the github page](https://github.com/google/wmt-mqm-human-evaluation). For a description of error severtities and MQM annotations you can also read:
* [Experts, Errors, and Context:
A Large-Scale Study of Human Evaluation for Machine Translation](https://arxiv.org/pdf/2104.14478.pdf)
* [Results of the WMT21 Metrics Shared Task](https://aclanthology.org/2021.wmt-1.73.pdf)
