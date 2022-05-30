---
layout: page
title: 'Additional training resources'
---

[Home](../index.md)


We provide below links to additional resources that can be used for training/augmentation.

# Task 1: Quality Prediction

 ## DA annotation data

 For the subtasks using **DA annotations** participants can use the annotations provided for the *Quality Estimation Shared Tasks* of the previous year(s) available on the MLQE-PE [github page](https://github.com/sheffieldnlp/mlqe-pe). For a full description of the abvailable language pairs and annotations please read the [MLQE-PE paper](https://arxiv.org/abs/2010.04480).


The datasets were collected by translating sentences sampled from source language articles using state-of-the-art Transformer NMT models and annotated with a variant of Direct Assessment (DA) scores by professional translators. Each sentence was annotated following the FLORES setup, which presents a form of DA, where at least three professional translators rate each sentence from 0-100 according to the perceived translation quality. DA scores are standardised using the z-score by rater. Participating systems are required to score sentences according to z-standardised DA scores.



You can donwload the NMT models used to generate the Wikipedia translations, as well as the Ru-En Wikipedia/Reddit NMT model. Here are details on the training data used to build the Ru-En model. The zero-shot translations were produced by a multilimgual Transformer NMT model.
The multilingual NMT models used to generate translations for the zero-shot language pairs can be found here: mBART50 (many-to-one for Ps-En and Km-En, and one-to-many for En-Cs and En-Ja).

It is also possible to use the DA annotations that were created for the Metrics shared tasks in the previous years. 
