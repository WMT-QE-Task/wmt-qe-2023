---
layout: page
title: 'Task 1: Quality prediction'
---

<a href="https://wmt-qe-task.github.io/" style="float: right;">Home</a>


The quality prediction task follows the trend of the previous years in comprising a **sentence-level subtask** where the goal is to predict the quality score for each source-target sentence pair and a **word-level subtask** where the goal is to predict the translation errors, assigning OK/BAD tags to each word of the target. 

Both subtasks include annotations derived in two different ways, depending on the language pair: direct assessments (DA), following the trend of the previous years, and multi-dimensional quality metrics (MQM), introduced for the first time in the QE shared task. Detailed information for the language pairs, the annotation specifics, and the available training and development resources in each category are provided below. We also note that the sentence- and word-level subtasks use the same source-target sentences for each language pair.


> #### **Important**
> Participants will be able to submit predictions for **any** of the subtasks/language pairs of their choice (or all of them). There will also be a **multilingual** phase of the competition covering all languages, to encourage development of multilingual systems.


# Sentence-level Subtask


## MQM scores


We will provide test sets for three language pairs annotated with MQM annotations. 

 - English-Russian (En-Ru)
 - English-German (En-De)
 - Chinese-English (Zh-En)

For training resources with MQM annotations it is possible to use any of the resources listed in the "[Additional training resources](../subtasks/resources.md)" section. 

We will also release a development set for each language pair. For release dates please consult the [home](../index.md) page

Note that in order to align with the DA annotations the MQM scorfes will be inverted (such that higher score will indicate better quality) and standardized per annotator. The individual annotations from each annotator will also be made available per segment.

For annotation guidelines see: **TBA**

## DA scores

We will provide test sets for five language pairs annotated with DA scores. 

 - English-Marathi (En-Ma)
 - English-Czech (En-Cs)
 - English-Japanese (En-Ja)
 - Khmer-English (Km-En)
 - Pashto-English (Ps-En)

For each language pair a single MT model has been used to translate the source sentences. Specifically, the English-Marathi has been translated with *** while the En-Cs, En-Ja, Km-En and Ps-En were translated using a [multilimgual Transformer NMT model](https://arxiv.org/abs/2008.00401).


 For training resources with DA annotations it is possible to use any of the resources listed in the "[Additional training resources](../subtasks/resources.md)" section. 

 Additionally this year we will make available a *new* training dataset for English-Marathi, comprising 30K language pairs.

 We will also release a development set for each language pair. For release dates please consult the [home](../index.md) page



# Word-level Subtask

The word-level subtask evaluates the application of QE for post-editing purposes. It consists of predicting word-level tags for the target side (to detect mistranslated or missing words). Each token is tagged as either OK or BAD. 

The OK/BAD tags are provided for each of the language of the sentence level task, and are derived from MQM annotations and post-edited sentences respectively.