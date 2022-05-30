---
layout: page
title: 'Task 1: Quality prediction'
---



The quality prediction task follows the trend of the previous years in comprising a **sentence-level subtask** where the goal is to predict the quality score for each source-target sentence pair and a **word-level subtask** where the goal is to predict the translation errors, assigning OK/BAD tags to each word of the target. 

Both subtasks include annotations derived in two different ways, depending on the language pair: direct assessments (DA), following the trend of the previous years, and multi-dimensional quality metrics (MQM), introduced for the first time in the QE shared task. Detailed information for the language pairs, the annotation specifics, and the available training and development resources in each category are provided below. We also note that the sentence- and word-level subtasks use the same source-target sentences for each language pair.


> #### **Important**
> Participants will be able to submit predictions for **any** of the subtasks/language pairs of their choice (or all of them). There will also be a **multilingual** phase of the competition covering all languages, to encourage development of multilingual systems.


# Sentence-level Subtask

The **training data** for the sentence level task can be downloaded [here](https://github.com/WMT-QE-Task/wmt-qe-2022-data/tree/main/sentence-level-subtask).
## MQM scores


We will provide test sets for three language pairs annotated with MQM annotations. 

 - English-Russian (En-Ru)
 - English-German (En-De)
 - Chinese-English (Zh-En)

For training resources with MQM annotations it is possible to use any of the resources listed in the "[Additional training resources](../subtasks/resources.md)" section or directly download the . 

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

For each language pair a single MT model has been used to translate the source sentences. Specifically, the English-Marathi has been translated with the model available [here](*), while the En-Cs, En-Ja, Km-En and Ps-En were translated using a [multilingual Transformer NMT model](https://arxiv.org/abs/2008.00401).


Apart from the provided training data, for training resources with DA annotations it is possible to use any of the resources listed in the "[Additional training resources](../subtasks/resources.md)" section. 

 Additionally this year we make available a *new* training dataset for English-Marathi, comprising 26K language pairs for training.

 We will also release a development set for each language pair. For release dates please consult the [home](../index.md) page

## Submission Format

We expect a single .tsv file for each submitted QE system output (submitted online in the respective codalab competition).

The file should be formatted with the two first lines indicating model size, and the rest containing predicted scores, one per line for each sentence, as follows:

Line 1: <DISK FOOTRPINT (in bytes, without compression)>

Line 2: \<NUMBER OF PARAMETERS>

Lines 3-n where -n is the number of test samples:
\<LANGUAGE PAIR> \<METHOD NAME> \<SEGMENT NUMBER> \<SEGMENT SCORE> 

Where:
* **LANGUAGE PAIR** is the ID (e.g. en-de) of the language pair of the plain text translation file you are scoring. Follow the LP naming convention provided in the test set.
* **METHOD NAME** is the name of your quality estimation method.
* **SEGMENT NUMBER** is the line number of the plain text translation file you are scoring.
* **SEGMENT SCORE** is the predicted (MQM/DA/HTER/Binary) score for the particular segment.

Each field should be delimited by a single tab character.

# Word-level Subtask

The word-level subtask evaluates the application of QE for post-editing purposes. It consists of predicting word-level tags for the target side (to detect mistranslated or missing words). Each token is tagged as either OK or BAD. 

The OK/BAD tags are provided for each of the language of the sentence level task, and are derived from MQM annotations and post-edited sentences respectively. 

<div class="panel panel-info">
**Note**
{: .panel-heading}
<div class="panel-body">

NOTE DESCRIPTION

</div>
</div>

Apart from the sentence tokens, an additional  \<EOS> token is appended to the end of each target setntence to represent potentially missing tokens that should havebeen inserted at the end of the sentence.