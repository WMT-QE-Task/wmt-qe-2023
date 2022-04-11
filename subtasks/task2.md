---
layout: page
title: 'Task 2: Explainable QE'
---



The main goal of the explainability for QE subtask is to explore the potential of building a quality estimation system that predicts the quality score for an input pair of source text and target MT and is able to provide word-level evidence as explanation for its predictions. In particular, for each pair of source and target sentences, participating teams are asked to provide (1) a sentence-level score estimating the translation quality and (2) a list of token-level scores where the tokens with the highest scores are expected to correspond to translation errors considered relevant by human annotators.

For the explainable QE subtask we will use the same language pairs used in [Task 1](../subtasks/task1.md):

 - English-Russian (En-Ru)
 - English-German (En-De)
 - Chinese-English (Zh-En)
 - English-Marathi (En-Ma)
 - English-Czech (En-Cs)
 - English-Japanese (En-Ja)
 - Khmer-English (Km-En)
 - Pashto-English (Ps-En)

For each language pair the participants can use the sentence-level score to train their QE systems. The sentence level scores will be normalised to minimise differences between the MQM and DA scales. The participants will be to provide token-level (i.e., word-level) errors, in the form of a continuous score for each token, as explanations for each predicted sentence score. As this subtask aims to promote the research in explainability of QE systems, we encourage the participants to use or develop explanation methods which can identify contributions of tokens in the input. **The participants are not allowed to supervise their models with any token-level or word-level labels or signals (whether they are from natural data or synthetic data) in order to directly predict word-level errors.** 

 

> #### **Upcoming**
> Apart from the language-pairs mentioned above, we will also provide test sets on some **surprise** language-pairs.  Check-back soon!

## Evaluation

Details on the evaluation process and metrics TBA.
