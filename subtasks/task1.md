---
layout: page
title: 'Task 1: Quality estimation'
---

The quality prediction task follows the trend of the previous years in comprising a **sentence-level subtask** where the goal is to predict the quality score for each source-target sentence pair and a **word-level subtask** where the goal is to predict the translation errors, assigning OK/BAD tags to each word (token) of the target translation. 

Both subtasks include annotations derived in two different ways, depending on the language pair:  **direct assessments (DA)**, following the trend of older editions, and **multi-dimensional quality metrics (MQM)**, aligned with the [Metrics shared task](https://wmt-metrics-task.github.io/). Detailed information for the language pairs, the annotation specifics, and the available training and development resources in each category are provided below. We also note that the sentence- and word-level subtasks use the same source-target sentences for each language pair.


> #### **Important**
> Participants will be able to submit predictions for **any** of the subtasks/language pairs of their choice (or all of them). 

# New elements

## Critical error detection subtask

This year we will evaluate submitted models not only on correlations with human scores, but also with respect to the ability to properly **distinguish translations with critical errors** (e.g. hallucinations) and attribute low quality scores to them. To that end the provided test sets will include a set of source-target segments with critical errors for which **no additional training data** will be provided. We thus aim to investigate whether submitted models are robust to cases such as significant deviations in meaning, hallucinations, etc. 

> #### **Note**
> The evaluation for critical errors will be separate to the main evaluation of performance for quality prediction and will not be included in the leaderboard. 

## Zero-shot LPs
We introduce two new zero-shot test sets, aiming to further motivate zero-/few-shot approaches.
- **He-En:**  MQM annotations 
- **En-Fa:**  post-edit annotations 
 

# Summary of data for 2023 shared task

Below we present the language pairs for the 2023 shared task along with available training resources

> ``❗`` Check back soon for updated information.

| Language Pair | Sentence-level annotation| Word-level annotation | Train data  | Dev data | Test data  |
|--------------------------|----------------------|-----------------------|---------------------------|-------------------|--------------------|
| English-German (En-De)   | MQM                  |  MQM            | [previously released](https://github.com/WMT-QE-Task/wmt-qe-2022-data) | [previously released](https://github.com/WMT-QE-Task/wmt-qe-2022-data/tree/main/test_data-gold_labels/task1_mqm/en-de)            | TBA: Aug 1st               |
| Chinese-English (Zh-En)  | MQM                  |  MQM            | [previously released](https://github.com/WMT-QE-Task/wmt-qe-2022-data) | [previously released](https://github.com/WMT-QE-Task/wmt-qe-2022-data/tree/main/test_data-gold_labels/task1_mqm/zh-en)               | TBA: Aug 1st               |
| Hebrew-English           | MQM                  |  MQM            | - | -               | TBA: Aug 1st                |
| English-Marathi (En-Mr)  | DA                   | Post-edits  | [previously released](https://github.com/WMT-QE-Task/wmt-qe-2022-data) | [previously released](https://github.com/WMT-QE-Task/wmt-qe-2022-data/tree/main/test_data-gold_labels/task1_da/en-mr)               | TBA: Aug 1st                |
| English-Hindi (En-Hi)  | DA                | Post-edits*  | [new train set released](https://github.com/WMT-QE-Task/wmt-qe-2023-data/tree/main/task_1/en-hi)| [new dev set released](https://github.com/WMT-QE-Task/wmt-qe-2023-data/tree/main/task_1/en-hi)                | TBA: Aug 1st                |
| English-Tamil (En-Ta)  | DA                   | Post-edits*  | [new train set released](https://github.com/WMT-QE-Task/wmt-qe-2023-data/tree/main/task_1/en-ta)  | [new dev set released](https://github.com/WMT-QE-Task/wmt-qe-2023-data/tree/main/task_1/en-ta)                | TBA: Aug 1st
| English-Telegu (En-Te)  | DA                   | -  | [new train set released](https://github.com/WMT-QE-Task/wmt-qe-2023-data/tree/main/task_1/en-te) | [new dev set released](https://github.com/WMT-QE-Task/wmt-qe-2023-data/tree/main/task_1/en-te)              | TBA: Aug 1st                |
| English-Gujarati (En-Gu)  | DA                   | - | [new train set released](https://github.com/WMT-QE-Task/wmt-qe-2023-data/tree/main/task_1/en-gu) | [new dev set released](https://github.com/WMT-QE-Task/wmt-qe-2023-data/tree/main/task_1/en-gu)              | TBA: Aug 1st                |
| English-Farsi (En-Fa)  | -                   |  Post-edits  | - | -               | TBA: Aug 1st                | 



 &nbsp;&nbsp; (*) post-edits (word level quality estimation) available as test-set only


---
## Baselines

We will use the following baselines:
- Sentence level subtask: **COMET QE** 
    - wmt21-comet-qe-mqm [🔗](https://unbabel-experimental-models.s3.amazonaws.com/comet/wmt21/wmt21-comet-qe-mqm.tar.gz)
    - wmt21-comet-qe-da [🔗](https://unbabel-experimental-models.s3.amazonaws.com/comet/wmt21/wmt21-comet-qe-da.tar.gz)
- Word level subtask: **COMETKiwi** [🔗](https://github.com/Unbabel/COMET/tree/master/comet/models/multitask) 


---
# Evaluation 

## Sentence-level
  
 We will use **Spearman** as primary metric and also compute Kendall and Pearson as secondary metrics.  


 ### Critical error detection
As a complementary evaluation, we will evaluate systems with respect to the detection of critical errors. We specifically want to assess the ability of submitted models to score translations with critical errors, such as hallucinations, *lower* than the other translations. To evaluate this, we will compute the *AUROC* and *recall@n* for each submission, with respect to the translations flagged as critical errors.

## Word-level
We will use **MCC** (Matthews correlation coefficient) as a primary metric and F1-score as secondary.


---
# Submission Format
The competition will take place on CODALAB with one competition instance for sentence-level and one for word-level subtasks. 
 
> ``❗`` This year we will also require participants to fill in a **form** describing their model and data choices for each submission. 

For each submission you wish to make (under "Participate>Submit" on codalab), please upload a **single zip** file with the predictions and the system metadata. 

For the **metadata**, we expect a 'metadata.txt' file, with exactly two non-empty lines which are for the teamname and the short system description, respectively.
The first line of metadata.txt must contain your team name. You can use your CodaLab username as your teamname. The second line of metadata.txt must contain a short description (2-3 sentences) of the system you used to generate the results. This description will not be shown to other participants. Note that submissions without a description will be invalid. It is fine to use the same submission for multiple submissions/phases if you use the same model (e.g. a multilingual or multitasking model)

For the **predictions** we describe the exact format expected separately for each subtask:
 
## Sentence level:

For the **predictions** we expect a single TSV file for each submitted QE system output (submitted online in the respective codalab competition), named 'predictions.txt'. 

The file should be formatted with the two first lines indicating model size, then indication of ensemble model number,and the rest containing predicted scores, one per line for each sentence, as follows:

Line 1: <DISK FOOTRPINT (in bytes, without compression)>

Line 2: \<NUMBER OF PARAMETERS>

Line 3: \<NUMBER OF ENSEMBLED MODELS> (set to 1 if there is no ensemble)

Lines 4-n where -n is the number of test samples:
\<LANGUAGE PAIR> \<METHOD NAME> \<SEGMENT NUMBER> \<SEGMENT SCORE> 

Where:
* **LANGUAGE PAIR** is the ID (e.g. en-de) of the language pair of the plain text translation file you are scoring. Follow the LP naming convention provided in the test set.
* **METHOD NAME** is the name of your quality estimation method.
* **SEGMENT NUMBER** is the line number of the plain text translation file you are scoring (starting at 0).
* **SEGMENT SCORE** is the predicted numerical (MQM/DA) score for the particular segment.

Each field should be delimited by a single tab (<\t>) character.


## Word-level  

For the **predictions** we expect a single TSV file for each submitted QE system output (submitted online in the respective codalab competition), named 'predictions.txt'.

You can submit different systems for any of the MQM or post-edited language pairs independently. The output of your system should be the predicted word-level tags, formatted in the following way:

Line 1: \<DISK FOOTRPINT (in bytes, without compression)>

Line 2: \<NUMBER OF PARAMETERS> 

Line 3: \<NUMBER OF ENSEMBLED MODELS> (set to 1 if there is no ensemble)

Lines 4-n where -n is the total number of tokens (words) in the test samples:
\<LANGUAGE PAIR> \<METHOD NAME> \<TYPE> \<SEGMENT NUMBER> \<WORD INDEX> \<WORD> \<BINARY SCORE>

Where:

* **LANGUAGE PAIR** is the ID (e.g., en-de) of the language pair.
* **METHOD NAME** is the name of your quality estimation method.
* **TYPE** should contain 'MT' for all segments.
* **SEGMENT NUMBER** is the line number of the plain text translation file you are scoring (starting at 0).
* **WORD INDEX** is the index of the word in the tokenised sentence, as given in the training/test sets (starting at 0). This will be the word index within the MT sentence.
* **WORD** actual word or \<EOS> token
* **BINARY SCORE** is either 'OK' for no issue or 'BAD' for any issue.

Each field should be delimited by a single tab (<\t>) character. 
