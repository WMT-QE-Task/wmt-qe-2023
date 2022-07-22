---
layout: page
title: 'Task 3: Critical Error Detection'
---
> ``❗`` Since these errors are artificially created we strongly encourage participants not to use the training data and if so, we will split participants into _unconstrained & constrained settings_. The baseline results using the provided training data are really high, indicating that the task is easy for a model that has access to training data that was created in a the same way. Nonetheless a traditional QE system trained on DA's has a hard time finding which sentences where modified. For a _constrained_ setting we will ask participants to submit systems that are purely trained on quality annotations such as DA's, MQM and/or HTER. A strong QE system should be robust to these artificially created errors while maintaining a high correlation with human judgments!

The goal of this task is to predict sentence-level binary scores indicating whether or not a translation contains a critical error. Translations with such errors are defined as translations that deviate in meaning as compared to the source sentence in such a way that they are misleading and may carry health, safety, legal, reputation, religious or financial implications. Meaning deviations from the source sentence can happen in three ways:

Mistranslation: critical content is translated incorrectly into a different meaning.
Hallucination: critical content that is not in the source is introduced in the translation, for example, addition of content that is not present in the source.
Deletion: critical content that is in the source sentence is not present in the translation.


We focus on a set of critical error categories:

- Additions: Deviation where the translation content is only partially supported by the source.
- Deletions: Deviation where part of the source sentence is ignored by the MT engine. 
- Named Entities: Deviation in named entities. A named entity (people, organization, location, etc.) is deleted, mistranslated by either another incorrect named entity or a common word or gibberish.
- Meaning: Deviation in sentence meaning. The MT either introduces or removes a negation and the sentence meaning is completely reversed.
- Numbers: Deviation in units. The MT translated a number/date/time or unit incorrectly

Examples:

| source | Translation | Label |
| :----: |  :--------: |  :---: |
| A questão, em última análise, é saber porque deve a Alemanha tentar reduzir o seu excedente de transacções correntes. | The question, **ultimately, is which is not so simple: Is there an effective excuse** why Germany should seek to reduce its current-account deficit surplus. | ADD |
| Alguns observadores, **como o Presidente do Banco do Japão Haruhiko Kuroda,** sugeriram que a China podia considerar o reforço dos controlos. | A few observers, have suggested that China might consider tightening controls. | DEL |
| Na verdade, as mulheres ocupam apenas 14% das posições dos conselhos de direcção Europeus. | Indeed, women hold only 14% of positions on **US** corporate boards. | NE |
| Os exportadores Chineses foram apanhados na tenaz da fraca procura externa e dos salários nacionais em rápido crescimento. | Chinese exporters are caught between the pincers of weak foreign demand and rapidly **lower** domestic wages. | MEAN |
| Por exemplo, os povos indígenas constituem apenas 5% da população global, mas representam 15% da população pobre mundial. | For example, indigenous peoples constitute just **0.7%** of the global population, but account for 15% of the world’s poor. | NUM | 

#### Training and development data:
Data consists of News articles containing instances in the following languages:
- Portuguese into English
- English into German

**Note:** For the Enlgish into German we do not have any Meaning errors!


#### Test data: 
Approximately 500 sentence pairs for each language pair are provided (News domain).

**The data is extremely unbalanced because in practice these phenomenas are rare and for that reason difficult to detect in a reliable way.**

#### Baselines: 
- _Unconstrained_ XLM-R base model for sequence classification
- _Constrained_ [wmt21-comet-qe-mqm](https://github.com/Unbabel/COMET/blob/master/METRICS.md#wmt21-comet-metrics)

For the _Constrained_ baseline we rank data according to the scores produced by `wmt21-comet-qe-mqm` and anything below a certain threshold is assigned a BAD tag. A perfect QE system should easily rank segments with critical errors below the other translations.

#### Evaluation: 
Submissions will be evaluated in terms of ranking. We ask participants to provide a score for each sentence and a threshold that separates Good translations from Bad ones. We will analyse the precision recall curve given the scores provided. 

TBA: Evaluation script for `wmt21-comet-qe-mqm`.

#### Previous Edition
This subtask is similar to the [Critical Error Detection shared task organized last year](https://www.statmt.org/wmt21/quality-estimation-task.html), we recommend checking their findings paper. Nonetheless, note that the domain is totally different from last years shared task and the annotations also differ.
