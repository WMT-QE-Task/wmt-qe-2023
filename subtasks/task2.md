---
layout: page
title: 'Task 2: Explainable QE'
---


The main goal of the explainability for QE subtask is to explore the potential of building a quality estimation system that predicts the quality score for an input pair of source text and target MT and is able to provide word-level evidence as explanation for its predictions. In particular, for each pair of source and target sentences, participating teams are asked to provide (1) a sentence-level score estimating the translation quality and (2) a list of token-level scores where the tokens with the highest scores are expected to correspond to translation errors considered relevant by human annotators. 

For the explainable QE subtask this year, we will use the same language pairs used in [Task 1](../subtasks/task1.md):

 - English-Russian (En-Ru)
 - English-German (En-De)
 - Chinese-English (Zh-En)
 - English-Marathi (En-Mr)
 - English-Czech (En-Cs)
 - English-Japanese (En-Ja)
 - Khmer-English (Km-En)
 - Pashto-English (Ps-En)

For each language pair, the participants can use the sentence-level scores to train their QE systems, available [here](https://github.com/WMT-QE-Task/wmt-qe-2022-data/tree/main/sentence-level-subtask). (Please see the resources listed in the "[Additional training resources](../subtasks/resources.md)" section for more details.) The sentence level scores will be normalised to align the score directionality between the MQM and DA scores (since for DA scores higher score signifies better quality and for MQM higher scores signify more (or more serious) translation errors). The participants will be asked to provide token-level (i.e., word-level) errors, in the form of a continuous score for each token, as explanations for each predicted sentence score. As this subtask aims to promote the research in explainability of QE systems, we encourage the participants to use or develop explanation methods which can identify contributions of tokens in the input. **The participants are not allowed to supervise their models with any token-level or word-level labels or signals (whether they are from natural data or synthetic data) in order to directly predict word-level errors.** 


> #### **Upcoming**
> Apart from the language-pairs mentioned above, we will also provide test sets on some **surprise** language-pairs.  Check-back soon!


## Submission

For each language pair, a submission is a zip file consisting of three files.
- `metadata.txt` must have exactly two non-empty lines.
    - The first line contains your team name. You might use your CodaLab username as your team name.
    - The second line contains a short description (2-3 sentences) of the system you used to generate the results. This description will not be shown to other participants.
- `sentence.submission` with sentence-level scores, one score per line.
- `target.submission` with target token-level binary labels. Each line must contain a sequence of scores separated by white space. The number of scores must correspond to the number of target tokens. These token-level scores must represent the importance of each token towards the sentence-level prediction, where a higher score means the token is more likely to be an error. Note that the scores do not need to be normalized.


## Evaluation

This task focuses on assessing the quality of explanations, not sentence-level predictions. Therefore, **the main metrics for evaluation will be AUC, Average Precision, and Recall at Top-K scores for token-level explanations.** Since the explanations are required to correspond to translation errors, these statistics will be computed for **the subset of translations that contain errors according to human annotation**.

Besides, for sentence-level predictions, we will calculate Pearson's correlation as a metric for analysis purposes only (not used for deciding the winner). 


## Baselines

Following the Eval4NLP shared task, we will provide three baselines.
- Random explanations
- [TransQuest](https://aclanthology.org/2020.wmt-1.122.pdf) (as a QE model) + [LIME](https://www.kdd.org/kdd2016/papers/files/rfp0573-ribeiroA.pdf) (as an explaner)
- [XMover](https://aclanthology.org/2020.acl-main.151.pdf) (as a QE model) + [SHAP](https://proceedings.neurips.cc/paper/2017/hash/8a20a8621978632d76c43dfd28b67767-Abstract.html) (as an explaner)


## Recommended Resources

### Quality Estimation Systems
- [TransQuest (Ranasinghe et al. 2020)](https://github.com/TharinduDR/TransQuest)
- [deepQuest (Kepler et al. 2019)](https://github.com/sheffieldnlp/deepQuest)
- [OpenKiwi](https://github.com/Unbabel/OpenKiwi)

### Post-Hoc Explainability Tools
- [LIME (Ribeiro et al., 2016)](https://github.com/marcotcr/lime)
- [SHAP (Lundberg and Lee, 2017)](https://github.com/slundberg/shap)
- [Captum](https://captum.ai/)
- [AllenNLP Interpret (Wallace et al., 2019)](https://allennlp.org/interpret)
- [iNNvestigate (Alber et al., 2019)](https://github.com/albermax/innvestigate)


## References

As this subtask is similar to the [explainable QE shared task](https://eval4nlp.github.io/2021/sharedtask.html) organized by [the Eval4NLP workshop last year](https://eval4nlp.github.io/2021/index.html), we recommend checking [their findings paper](https://aclanthology.org/2021.eval4nlp-1.17/). Apart from that, please find the list of related papers below.

- Christoph Leiter, Piyawat Lertvittayakumjorn, Marina Fomicheva, Wei Zhao, Yang Gao, Steffen Eger (2022). Towards Explainable Evaluation Metrics for Natural Language Generation
- Scott M. Lundberg, Su-In Lee (2017). A Unified Approach to Interpreting Model Predictions. NIPS2017
- Tharindu Ranasinghe, Constantin Orasan, Ruslan Mitkov (2020). TransQuest at WMT2020: Sentence-Level Direct Assessment
- Tharindu Ranasinghe, Constantin Orasan, Ruslan Mitkov (2020). TransQuest: Translation Quality Estimation with Cross-lingual Transformers
- Marco Tulio Ribeiro, Sameer Singh, Carlos Guestrin. (2016). "Why Should I Trust You?": Explaining the Predictions of Any Classifier
- Wei Zhao, Goran Glavaš, Maxime Peyrard, Yang Gao, Robert West, Steffen Eger. (2020). On the Limitations of Cross-lingual Encoders as Exposed by Reference-Free Machine Translation Evaluation
- Marina Fomicheva, Shuo Sun, Erick Fonseca, Frédéric Blain, Vishrav Chaudhary, Francisco Guzmán, Nina Lopatina, Lucia Specia, André F. T. Martins. (2020) MLQE-PE: A Multilingual Quality Estimation and Post-Editing Dataset
- Mo Yu, Shiyu Chang, Yang Zhang, Tommi Jaakkola (2019). Rethinking Cooperative Rationalization: Introspective Extraction and Complement Control
- Mukund Sundararajan, Ankur Taly, Qiqi Yan (2017). Axiomatic Attribution for Deep Networks
- Eric Wallace, Jens Tuyls, Junlin Wang, Sanjay Subramanian, Matt Gardner, Sameer Singh (2019). AllenNLP Interpret: A Framework for Explaining Predictions of NLP Models
