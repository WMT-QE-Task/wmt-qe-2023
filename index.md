---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

# Welcome to the 2023 Quality Estimation Shared Task!


``❗`` To easily stay up-to-date you can also follow out [Twitter](https://twitter.com/qe_task) and [LinkedIn]() accounts.

``❗`` Please also register to the **QE google-group** [here](https://groups.google.com/g/wmt-qe-shared-task/) in order to be able to receive updates and announcements immediately, and **ask questions**.


This shared task focuses on automatic methods for estimating the quality of neural machine translation output at run-time, without relying on reference translations. It will cover estimation at sentence and word levels and critical error detection. This year we put emphasis on:

* Medium- and **low-resource** language pairs 
* Increased alignment with the [Metrics shared task](https://wmt-metrics-task.github.io/)
	* Shared translation sources
	* Shared annotation schema [MQM]
	* Shared submission platform [codalab]
* Few- and **zero-shot approaches**  
* Critical error detection



## Language pairs covered

This year we will release test-sets on the following language-pairs:
* English-German (En-De)   [MQM]
* Chinese-English (Zh-En)  [MQM]
* Hebrew-English   (He-Ee)  [MQM]
* English-Marathi (En-Mr)    [DA + post-edits]
* English-Hindi (En-Hi)        [DA + post-edits]
* English-Tamil (En-Ta)       [DA + post-edits]
* English-Telegu (En-Te)  [DA]
* English-Gujarati (En-Gu)   [DA]
<!-- | English-Farsi (En-Fa) 


See more details in [Task 1](./subtasks/task1.md) description.




## Quality Estimation Task Important Dates (AoE)

|  | Date |
| ----------- | :-----------: |
| Release of training data | 30 May, 2023 |
| Release of dev data | TBA |
| Release of test data | (TBA) July, 2023 |
| Submission of test predictions deadline | (TBA) August, 2023 | 
| Announcement of results | (TBA) September, 2023|
| System description submission deadline | (TBA) August 2023 |
| Paper submission deadline to WMT | (TBA) September, 2023 |
| WMT Notification of acceptance | 06 October, 2023 |
| WMT Camera-ready deadline | 20 October, 2023 |
| WMT Conference | 	(TBA) December, 2023 |

## Goals

In addition to generally advancing the state of the art in quality estimation, our specific **goals** are:

- to extend the available public benchmark datasets;
- to investigate the potential and suitability of MQM annotations for quality estimation;
- to investigate new multilingual and language independent approaches esp. for zero-shot prediction;
- to study the feasibility of explainable quality estimation; and
- to focus on detection of extreme/catastrophic errors in MT.

For all tasks, the datasets and NMT models that generated the translations will be made publicly available.

Participants are also allowed to explore any additional data and resources deemed relevant. Below are the three QE tasks addressing these goals.

### Subtasks:

1. [Quality estimation](./subtasks/task1/)
2. [Few-shot Quality Estimation](./subtasks/task2/)
3. [Critical Error Detection](./subtasks/task3/)

## Submission Information
The shared task competition will take place on CODALAB. 

Please register with one account per team.

<!-- Task 1:
- Sentence level DA: [https://codalab.lisn.upsaclay.fr/competitions/6841](https://codalab.lisn.upsaclay.fr/competitions/6841)
- Sentence level MQM: [https://codalab.lisn.upsaclay.fr/competitions/6866](https://codalab.lisn.upsaclay.fr/competitions/6866)
- Word level: [https://codalab.lisn.upsaclay.fr/competitions/6883](https://codalab.lisn.upsaclay.fr/competitions/6883)


Task 2:
- Explainability task: [https://codalab.lisn.upsaclay.fr/competitions/6863](https://codalab.lisn.upsaclay.fr/competitions/6863)


Task 3:
- Critical error detection: [https://codalab.lisn.upsaclay.fr/competitions/6893](https://codalab.lisn.upsaclay.fr/competitions/6893)

It is not necessary to participate on all tasks/subtasks/phases. Participating teams can choose which tasks/language pairs they want to make submissions for. -->
## Useful Software
Here are some open source software for QE that might be useful for participants:
- [OpenKiwi](https://github.com/Unbabel/OpenKiwi)
- [COMET-QE](https://unbabel.github.io/COMET/html/models.html)
- [TransQuest](https://github.com/TharinduDR/TransQuest)
- [DeepQuest](https://github.com/sheffieldnlp/deepQuest)

## Submission Requirements
TBA

## Organization:

- Chrysoula Zerva (Instituto de Telecomunicações) [chryssa.zrv@gmail.com](chryssa.zrv@gmail.com)
- André Martins (Instituto de Telecomunicações, Unbabel)
- Frédéric Blain (Tilburg University)
- Ricardo Rei (INESC-ID, Unbabel)
- José Souza (Unbabel)
- Diptesh Kanojia (Surrey Institute for People-Centred AI, University of Surrey)
- Constantin Orasan (University of Surrey)
<!-- - Lucia Specia (Imperial College London)
- Piyawat Lertvittayakumjorn (Imperial College London)
- Steffen Eger (Technische Universität Darmstadt) -->
<!-- - Marina Fomicheva (University of Sheffield) -->

## Sponsors

<style>
	.column {
	  float: left;
	  padding: 20px;
	}
	
</style>
<div style="position: relative; width: 700px; height: 100px; min-height: 200px">    
    <div style="position: relative; bottom: 0px;">
	   <div class="column">
	     <img src="/public/css/IT.png" height=70px width=auto>
	   </div>
	   <div class="column">
	     <img src="/public/css/unbabel.png" height=70px width=auto>
	   </div>
	   <div class="column">
	     <img src="/public/css/IST.png" height=70px width=auto>
	   </div>
	</div>
<div style="position: relative; width: 700px; height: 100px; min-height: 200px">    
    <div style="position: relative; bottom: 0px;">
	   <div class="column">
	     <img src="/public/css/Surrey.png" height=70px width=auto>
	   </div>
	   <div class="column">
	     <img src="/public/css/tilburg.jpeg" height=70px width=auto>
	   </div>
	   <div class="column">
	     <img src="/public/css/INESC-ID.png" height=70px width=auto>
	   </div>
	   <div class="column">
	     <img src="/public/css/surrey.jpeg" height=70px width=auto>
	   </div>
	</div>
