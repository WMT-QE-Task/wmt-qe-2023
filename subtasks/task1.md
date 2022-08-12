---
layout: page
title: 'Task 1: Quality prediction'
---

The quality prediction task follows the trend of the previous years in comprising a **sentence-level subtask** where the goal is to predict the quality score for each source-target sentence pair and a **word-level subtask** where the goal is to predict the translation errors, assigning OK/BAD tags to each word of the target. 

Both subtasks include annotations derived in two different ways, depending on the language pair: direct assessments (DA), following the trend of the previous years, and multi-dimensional quality metrics (MQM), introduced for the first time in the QE shared task. Detailed information for the language pairs, the annotation specifics, and the available training and development resources in each category are provided below. We also note that the sentence- and word-level subtasks use the same source-target sentences for each language pair.


> #### **Important**
> Participants will be able to submit predictions for **any** of the subtasks/language pairs of their choice (or all of them). There will also be a **multilingual** phase of the competition covering all languages, to encourage development of multilingual systems.

# Summary of data for 2022 shared task

> ``❗`` The **training data** for all subtasks can now be downloaded [here 🔗](https://github.com/WMT-QE-Task/wmt-qe-2022-data/tree/main/sentence-level-subtask). We provide an overview of the datasets, annotations and LPs below. For more information check also the individual task tabs and the additional data.


| Language Pair | Sentence-level score type| Word-level annotation | Train set and size  | Dev set and size  | Test set and size  |
|--------------------------|----------------------|-----------------------|---------------------------|-------------------|--------------------|
| English-Russian (En-Ru)  | MQM                  | MQM Binary: OK/BAD             | Metrics 2021: <br /> Newstest ➝ 7K,  <br />  Tedtalks ➝ 8K      | 1K               | TBA - 1K                 |
| English-German (En-De)   | MQM                  |  MQM Binary: OK/BAD           | Metrics 2020: 11K <br /> Metrics 2021: Newstest ➝ 7K, <br /> Tedtaks ➝ 8K | 1K               | TBA - 1K                 |
| Chinese-English (Zh-En)  | MQM                  |  MQM Binary: OK/BAD         | Metrics 2020: 15K <br /> Metrics 2021: <br /> Newstest ➝ 8K <br /> Tedtalks ➝ 8K | 1K               | TBA - 1K                 |
| English-Marathi (En-Mr)  | DA                   | Post-editing Binary: OK/BAD  | **NEW**❗ 26K                    | **NEW**❗ 1K            | TBA - 1K               |
| English-Czech (En-Cs)    | DA                   | Post-editing Binary: OK/BAD  | No training set           | MLQE-PE Test 21 1K | TBA - 1K  |
| English-Japanese (En-Ja) | DA                   | Post-editing Binary: OK/BAD   | No training set           | MLQE-PE Test 21 1K | TBA - 1K  |
| Khmer-English (Km-En)    | DA                   | Post-editing Binary: OK/BAD   | No training set           | MLQE-PE Test 21 1K | TBA - 1K |
| Pashto-English (Ps-En)   | DA                   | Post-editing Binary: OK/BAD   | No training set           | MLQE-PE Test 21 1K | TBA - 1K  |
| English-German (En-De)   | DA                   | Post-editing Binary: OK/BAD   | 9K (MLQE-PE Train/Dev/Test20)          | MLQE-PE Test 21 1K |  -- |
| English-Chinese (En-Zh)   | DA                   | Post-editing Binary: OK/BAD   | 9K (MLQE-PE Train/Dev/Test20)          | MLQE-PE Test 21 1K |  -- |
| Esthonian-English (Et-En)   | DA                   | Post-editing Binary: OK/BAD   | 9K (MLQE-PE Train/Dev/Test20)          | MLQE-PE Test 21 1K |  -- |
| Nepali-English (Ne-En)   | DA                   | Post-editing Binary: OK/BAD   | 9K (MLQE-PE Train/Dev/Test20)          | MLQE-PE Test 21 1K |  -- |
| Romanian-English (Ro-En)   | DA                   | Post-editing Binary: OK/BAD   | 9K (MLQE-PE Train/Dev/Test20)          | MLQE-PE Test 21 1K |  -- |
| Russian-English (Ru-En)   | DA                   | Post-editing Binary: OK/BAD   | 9K (MLQE-PE Train/Dev/Test20)          | MLQE-PE Test 21 1K |  -- |
| Sinhala-English (Si-En)   | DA                   | Post-editing Binary: OK/BAD   | 9K (MLQE-PE Train/Dev/Test20)          | MLQE-PE Test 21 1K |  -- |
| Surprise LP  | DA                   | Binary: OK/BAD           | – (zero-shot)             | – (zero-shot)     | TBA - 1K       |

# Sentence-level Subtask

> ``❗`` The **training data** for the sentence level task can be downloaded [here](https://github.com/WMT-QE-Task/wmt-qe-2022-data/tree/main/sentence-level-subtask).
## MQM scores


We will provide test sets for three language pairs annotated with MQM annotations. 

 - English-Russian (En-Ru)
 - English-German (En-De)
 - Chinese-English (Zh-En)

For training resources with MQM annotations it is possible to use any of the resources listed in the "[Additional training resources](../subtasks/resources.md)" section or directly download the data from the [github page](https://github.com/WMT-QE-Task/wmt-qe-2022-data/tree/main/sentence-level-subtask/MQM_QE_data/train_data_2022). 

We will also release a development set for each language pair. For release dates please consult the [home](../index.md) page

Note that in order to align with the DA annotations the MQM scores will be inverted (such that higher score will indicate better quality) and standardized per annotator. The individual annotations from each annotator will also be made available per segment.

For annotation guidelines see: **TBA**

## DA scores

We will provide test sets for five language pairs annotated with DA scores. 

 - English-Marathi (En-Mr)
 - English-Czech (En-Cs)
 - English-Japanese (En-Ja)
 - Khmer-English (Km-En)
 - Pashto-English (Ps-En)

For each language pair a single MT model has been used to translate the source sentences. Specifically, the English-Marathi has been translated with the English-Indic model available [here](https://drive.google.com/file/d/1itxbV2RqIsduOJ7_7AdUaxTdIddMBmJ2/view?usp=sharing), while the En-Cs, En-Ja, Km-En and Ps-En were translated using a [multilingual Transformer NMT model](https://arxiv.org/abs/2008.00401).


Apart from the provided training data, for training resources with DA annotations it is possible to use any of the resources listed in the "[Additional training resources](../subtasks/resources.md)" section. 

 Additionally this year we make available a *new* training dataset for English-Marathi, comprising 26K language pairs for training.

 We will also release a development set for each language pair. For release dates please consult the [home](../index.md) page

---

## Evaluation

Sentence-level submissions will be evaluated using the Spearman's rank correlation coefficient to estimate correlation with the human scores (z-normalized scores). Pearson's correlation coefficient as well as MAE and RMSE will also be used as secondary metrics.

The evaluation will focus on multilingual systems, i.e. systems that are able to provide predictions for all languages, including the zero-shot ones. Therefore, average Spearman correlation across all these languages will be used to rank QE systems. We will also evaluate QE systems on a per-language basis for those interested in particular languages, and a per annotation schema scenario (comparing performance on MQM and DA separately).



---
## Submission Format
For each submission you wish to make (under "Participate>Submit" on codalab), please upload a **single zip** file with the predictions and the system metadata. 

For the **metadata**, we expect a 'metadata.txt' file, with exactly two non-empty lines which are for the teamname and the short system description, respectively.
The first line of metadata.txt must contain your team name. You can use your CodaLab username as your teamname. The second line of metadata.txt must contain a short description (2-3 sentences) of the system you used to generate the results. This description will not be shown to other participants. Note that submissions without a description will be invalid. It is fine to use the same submission for multiple submissions/phases if you use the same model (e.g. a multilingual or multitasking model)

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
* **SEGMENT SCORE** is the predicted (MQM/DA/HTER/Binary) score for the particular segment.

Each field should be delimited by a single tab character.

# Word-level Subtask


> ``❗`` The **training data** for the sentence level task can be downloaded [here](https://github.com/WMT-QE-Task/wmt-qe-2022-data/tree/main/word-level-subtask).

The word-level subtask evaluates the application of QE for post-editing purposes. It consists of predicting word-level tags for the target side (to detect mistranslated or missing words). Each token is tagged as either OK or BAD. 

The OK/BAD tags are provided for each of the language pairs of the sentence level task, and are derived from either MQM annotations (En-De, Zh-En and En-Ru) or post-edited sentences. 


---
##  Tagging conventions 
The OK/BAD tags on the target sentence are annotated as follows: 
* If a target token is (part of) a mistranslation of the corresponding source token(s) it obtains the tag BAD. 
* If a token is completely irrelevant to the source (wrong insertion) it also obtains the tag BAD. 
* If there is one or more missing token(s) between two tokens in the target (translation) then the token on the right of the ommision (where the missing token(s) should have been inserted) should be annotated as BAD (regardless of whether that token is correct or not). 
* All other correctly translated tokens should be tagged as OK.

> ``📝`` Apart from the sentence tokens, an additional  \<EOS> token is appended to the end of each target sentence to represent potentially missing tokens that should have been inserted at the end of the sentence.


---
## Tagging specifications by annotation type

As we have language pairs with different annotation schemes this year, the training data is derived differently and follows different conventions for MQM and post-edited sentences.
### **MQM:**
For the En-De and Zh-En language pairs we did not have any token-level information for deletions (missing tokens on the target side), hence all \<EOS> tokens are tagged as OK and there are no BAD tags related to deletion errors. 

The En-Ru data included annotations for missing tokens on the target side, hence it includes such token-level information.

> ``📝`` **NOTE:** The dev and test data for the MQM word-level tasks will follow the En-Ru setup.


### **Post-Edits:**
For the post edited data the word-level tags for the target side include mistranslation/insertion and deletion errors as descibed in the beginning. The code used to process the data and obtain the files can be found on [this github repository](https://github.com/deep-spin/qe-corpus-builder).


---

## Evaluation

For word-level QE, the submissions will be evaluated in terms of MCC (Matthews correlation coefficient) as a primary metric. F1 scores will also be calculated and used as secondary evaluation metrics. 

The evaluation will focus on multilingual systems, i.e. systems that are able to provide predictions for all languages, including the zero-shot ones. We will also evaluate QE systems on a per-language basis for those interested in particular languages, and a per annotation schema scenario (comparing performance on MQM and post-edits separately).

---
## Submission Format

For each submission you wish to make, both in the DA and MQM competitions, please upload a **single zip** file with the predictions and the system metadata (under "Participate>Submit" on codalab). 

For the **metadata**, we expect a 'metadata.txt' file, with exactly two non-empty lines which are for the teamname and the short system description, respectively.
The first line of metadata.txt must contain your team name. You can use your CodaLab username as your teamname. The second line of metadata.txt must contain a short description (2-3 sentences) of the system you used to generate the results. This description will not be shown to other participants. Note that submissions without a description will be invalid. It is fine to use the same submission for multiple submissions/phases if you use the same model (e.g. a multilingual or multitasking model)

For the **predictions** we expect a single TSV file for each submitted QE system output (submitted online in the respective codalab competition), named 'predictions.txt'.

You can submit different systems for any of the MQM or post-edited language pairs independently. The output of your system should be the predicted word-level tags, formatted in the following way:

Line 1: \<DISK FOOTRPINT (in bytes, without compression)>

Line 2: \<NUMBER OF PARAMETERS> 

Line 3: \<NUMBER OF ENSEMBLED MODELS> (set to 1 if there is no ensemble)

Lines 4-n where -n is the number of test samples:
\<LANGUAGE PAIR> \<METHOD NAME> \<TYPE> \<SEGMENT NUMBER> \<WORD INDEX> \<WORD> \<BINARY SCORE>

Where:

* **LANGUAGE PAIR** is the ID (e.g., en-de) of the language pair.
* **METHOD NAME** is the name of your quality estimation method.
* **TYPE** should contain 'MT' for all segments.
* **SEGMENT NUMBER** is the line number of the plain text translation file you are scoring (starting at 0).
* **WORD INDEX** is the index of the word in the tokenised sentence, as given in the training/test sets (starting at 0). This will be the word index within the MT sentence.
* **WORD** actual word or \<EOS> token
* **BINARY SCORE** is either 'OK' for no issue or 'BAD' for any issue.

Each field should be delimited by a single tab character.
