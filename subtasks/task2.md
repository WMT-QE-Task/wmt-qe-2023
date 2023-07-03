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

TBA