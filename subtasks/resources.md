---
layout: page
title: 'Additional training resources'
---

[Home](../index.md)


We provide below links to additional resources that can be used for training/augmentation.

# Task 1: Quality Prediction

## MQM annotation data

For the subtasks using **MQM annotations** participants can use the En-De and Zh-En MQM annotations provided for the *Metrics Shared Task 2021* available on the following [github link](https://github.com/google-research/mt-metrics-eval). 

The data consists of:

- Sentences onbtained from the WMT 2020 and WMT 2021 newstests. Specifically per language:
  - English-German (En-De) 
    - 2020: <span style="color:#6495ED">[11K src-mt pairs]</span>
    - 2021: <span style="color:#6495ED">[7K src-mt pairs]</span>
  - Chinese-English (Zh-En) 
    - 2020: <span style="color:#6495ED">[15K src-mt pairs]</span>
    - 2021: <span style="color:#6495ED">[8K src-mt pairs]</span>
  - English-Russian (En-Ru) 
    - 2021: <span style="color:#6495ED">[7K src-mt pairs]</span>
- Sentences onbtained from TEDTalks. Specifically per language:
  - English-German (En-De) 
    - 2021: <span style="color:#6495ED">[8K src-mt pairs]</span>
  - English-Russian (En-Ru) 
    - 2021: <span style="color:#6495ED">[8K src-mt pairs]</span>
  - Chinese-English (Zh-En) 
    - 2021: <span style="color:#6495ED">[8K src-mt pairs]</span>   <br />
<br />
  


 ## DA annotation data

 For the subtasks using **DA annotations** participants can use the annotations provided for the *Quality Estimation Shared Tasks* of the previous year(s) available on the MLQE-PE [github page](https://github.com/sheffieldnlp/mlqe-pe). For a full description of the abvailable language pairs and annotations please read the [MLQE-PE paper](https://arxiv.org/abs/2010.04480).

 The data consists of:
 
 -  Wikipedia data for 6 language pairs that includes:
 
    - English-German (En-De)  <span style="color:#1ABC9C">[high resource]</span><span style="color:#6495ED">[10K segments]</span>. 
    - English-Chinese (En-Zh) <span style="color:#1ABC9C">[high resource]</span><span style="color:#6495ED">[10K segments]</span>. 
    - Romanian-English (Ro-En) <span style="color:#1ABC9C">[medium resource]</span><span style="color:#6495ED">[10K segments]</span>. 
    - Estonian-English (Et-En) <span style="color:#1ABC9C">[medium resource]</span><span style="color:#6495ED">[10K segments]</span>. 
    - Sinhalese-English (Si-En) <span style="color:#1ABC9C">[low resource]</span><span style="color:#6495ED">[10K segments]</span>. 
    - Nepalese-English (Ne-En)  <span style="color:#1ABC9C">[low resource]</span><span style="color:#6495ED">[10K segments]</span>

- a dataset with a combination of Wikipedia articles and Reddit articles for 
   - Russian-English (Ru-En)  <span style="color:#1ABC9C">[medium resource]</span><span style="color:#6495ED">[10K segments]</span>. 
   
- 4 smaller datasets from Wikipedia that were used as blid tests in the WMT 2021 QE Shared Task
   - English-Czech <span style="color:#1ABC9C">[medium resource]</span><span style="color:#6495ED">[1K segments]</span>. 
   - English-Japanese <span style="color:#1ABC9C">[medium resource]</span><span style="color:#6495ED">[1K segments]</span>. 
   - Pashto-English <span style="color:#1ABC9C">[low resource]</span><span style="color:#6495ED">[1K segments]</span>. 
   - Khmer-English <span style="color:#1ABC9C">[low resource]</span><span style="color:#6495ED">[1K segments]</span>. 



The datasets were collected by translating sentences sampled from source language articles using state-of-the-art Transformer NMT models and annotated with a variant of Direct Assessment (DA) scores by professional translators. Each sentence was annotated following the FLORES setup, which presents a form of DA, where at least three professional translators rate each sentence from 0-100 according to the perceived translation quality. DA scores are standardised using the z-score by rater. Participating systems are required to score sentences according to z-standardised DA scores.



You can donwload the NMT models used to generate the Wikipedia translations, as well as the Ru-En Wikipedia/Reddit NMT model. Here are details on the training data used to build the Ru-En model. The zero-shot translations were produced by a multilimgual Transformer NMT model.
The multilingual NMT models used to generate translations for the zero-shot language pairs can be found here: mBART50 (many-to-one for Ps-En and Km-En, and one-to-many for En-Cs and En-Ja).



> #### **Upcoming**
> Links for English-Marathi (En-Ma) train data TBA




 # Task 2: Explainable QE

```
TBA
```

 # Task 3: Critical Error Detection 
```
 TBA
 ```
