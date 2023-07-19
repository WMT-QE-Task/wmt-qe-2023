---
layout: page
title: 'Task 2: Fine-grained error span detection'
---

 This is a **word-level subtask** where the goal is to predict the translation error spans as opposed to binary OK/BAD tasks. 

 For this task we will use the error spans obtained from the **MQM annotations**. Participants will be asked to predict both the error span (start and end *indices*) as well as the error severity (**major** or **minor**) for each segment. 

 
> #### **Important**
> Participants will be able to submit predictions for **any** of the language pairs of their choice (or all of them). 

# Summary of data for 2023 fine-grained shared task

Below we present the language pairs for the 2023 shared task along with available training resources


| Language Pair | Sentence-level annotation| Word-level annotation | Train data  | Dev data | Test data  |
|--------------------------|----------------------|-----------------------|---------------------------|-------------------|--------------------|
| English-German (En-De)   | MQM                  |  MQM            | [MQM 2020 2022](https://github.com/google/wmt-mqm-human-evaluation)  | [MQM 2020 2022](https://github.com/google/wmt-mqm-human-evaluation)            | TBA: Aug 1st                  |
| Chinese-English (Zh-En)  | MQM                  |  MQM            | [MQM 2020 2022](https://github.com/google/wmt-mqm-human-evaluation) | [MQM 2020 2022](https://github.com/google/wmt-mqm-human-evaluation)             | TBA: Aug 1st                  |
| Hebrew-English           | MQM                  |  MQM            | - | -               | TBA: Aug 1st                  |


# Evaluation

The primary evaluation metric will be **F1-score** and we also plan to report Recall and Precision. 



# Baselines

We will use [CometKiwi](https://github.com/Unbabel/COMET/tree/master/comet/models/multitask) as a baseline, trained on the MQM 2020-2021 data to predict OK/BAD-major/BAD-minor errors.


# Submission Format

Line 1: <DISK FOOTRPINT (in bytes, without compression)>

Line 2: \<NUMBER OF PARAMETERS>

Line 3: \<NUMBER OF ENSEMBLED MODELS> (set to 1 if there is no ensemble)

Lines 4-n where -n is the number of test samples:
\<LANGUAGE PAIR> \<METHOD NAME> \<SEGMENT NUMBER> \<TARGET SENTENCE> \<ERROR START INDICES> \<ERROR END INDICES>  \<ERROR TYPES> 

Where:
* **LANGUAGE PAIR** is the ID (e.g. en-de) of the language pair of the plain text translation file you are scoring. Follow the LP naming convention provided in the test set.
* **METHOD NAME** is the name of your quality estimation method.
* **SEGMENT NUMBER** is the line number of the plain text translation file you are scoring (starting at 0).
* **TARGET SENTENCE** is the target sentence based on which the error span indices were extracted.  You should use **exactly the target sentence as provided by the test set** to ensure alignment with the gold labels.
* **ERROR START INDICES** the start indices (character level) of every exrror span extracted. For multiple error spans separate indices by a whitespace. For no errors output *-1*.
* **ERROR END INDICES** the end indices (character level) of every exrror span extracted. For multiple error spans separate indices by a whitespace. For no errors output *-1*. 
* **ERROR TYPES** indication of *minor* or *major* error for each detected error span. The number of indices should match the number of errors.

Each field should be delimited by a single tab (<\t>) character.


**Output example**

2409244995  
2280000000  
3  
he-en <\t> example-ensemble <\t> 0 <\t> This is a sample translation without errors. <\t> -1 <\t> -1 <\t> no-error  
he-en <\t> example-ensemble <\t> 1 <\t> This is a sample translation with a span that is *considered major error* and another span that is *considered minor error*. <\t> 49 97 <\t> 70 118 <\t> major minor
...