---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

# Welcome to the 2023 Quality Estimation Shared Task!


``❗`` Test data is now available on  [**github**](https://github.com/WMT-QE-Task/wmt-qe-2023-data/tree/main/test_data_2023).

``❗`` Note that the codalab will be ready for submissions on the **~~7th~~ 8th of August 23:59 AoE** (submission deadline extended to 17th of August 23:59 AoE).

``❗`` To easily stay up-to-date you can also follow our [**Twitter account**](https://twitter.com/qe_task).

``❗`` Please also register to the [**QE google-group**](https://groups.google.com/g/wmt-qe-shared-task/) in order to be able to receive updates and announcements immediately, and **ask questions**.


This shared task focuses on automatic methods for estimating the quality of neural machine translation output at run-time, without relying on reference translations. It will cover estimation at sentence and word levels and critical error detection. This year we put emphasis on:

* Medium- and **low-resource** language pairs  
* New fine-grained quality estimation shared task 
* Increased alignment with the [Metrics shared task](https://wmt-metrics-task.github.io/) to facilitate cross-submissions and multi-task approaches
	* Shared translation sources
	* Shared annotation schema [MQM]
	* Shared submission platform [CODALAB]
* Increased alignment with the [APE shared task](http://www2.statmt.org/wmt23/ape-task.html) to facilitate cross-submission and multi-task approaches
	* Shared sources - translations - post-edits  (English-Marathi) 
* Incorporated critical error detection tasks
* Incorporated zero-shot tasks

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
* English-Farsi (En-Fa) [post-edits]


See more details in [Task 1](./subtasks/task1.md) and [Task 2](./subtasks/task2.md) description.




## Quality Estimation Task Important Dates (AoE)

|  | Date |
| ----------- | :-----------: |
| Release of extra training data | 3rd July, 2023 |
| Release of dev data | 3rd July 2023 | 
| Release of test data | 1st August, 2023 |
| Submission of test predictions deadline | ~~15th~~ <span style="color:red">17th August 2023</span> |  
| Announcement of results | (TBA) September, 2023|
| System description submission deadline | (TBA) August 2023 |
| Paper submission deadline to WMT | (TBA) September, 2023 |
| WMT Notification of acceptance | 06 October, 2023 |
| WMT Camera-ready deadline | 20 October, 2023 |
| WMT Conference | 	(TBA) December, 2023 |

## Goals

In addition to generally advancing the state of the art in quality estimation, our specific **goals** are:

- to extend the available public benchmark datasets with medium- and low-resource languages;
- to investigate the potential of **fine-graned quality estimation**;
- to investigate new multilingual and language independent approaches esp. for **zero-shot** approaches; and
- to study the robustness of QE approaches

For all tasks, the datasets and NMT models that generated the translations will be made publicly available.

Participants are also allowed to explore any additional data and resources deemed relevant. Below are the three QE tasks addressing these goals.

### Subtasks:

1. [Quality estimation](./subtasks/task1/)
2. [Fine-grained error span detection](./subtasks/task2/) 


## Submission Information
The shared task competition will take place on CODALAB (link in July).

Please register with one account per team.

# Useful Software
Here are some open source software for QE that might be useful for participants:
- [OpenKiwi](https://github.com/Unbabel/OpenKiwi)
- [COMET-QE](https://unbabel.github.io/COMET/html/models.html) 
- [TransQuest](https://github.com/TharinduDR/TransQuest)
- [DeepQuest](https://github.com/sheffieldnlp/deepQuest)   

 
# Organization

- Chrysoula Zerva (Instituto de Telecomunicações) [chryssa.zrv@gmail.com](chryssa.zrv@gmail.com)
- André Martins (Instituto de Telecomunicações, Unbabel)
- Frédéric Blain (Tilburg University)
- Ricardo Rei (INESC-ID, Unbabel)
- José Souza (Unbabel) 
- Diptesh Kanojia (Surrey Institute for People-Centred AI, University of Surrey)
- Constantin Orasan (University of Surrey)
- Nuno Guerreiro (Instituto de Telecomunicações) 
- Fatemeh Azadi (University Of Tehran) 


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
	   <div class="column">
	     <img src="/public/css/eamt-logo.jpg" height=70px width=auto>
	   </div>
	</div>
<div style="position: relative; width: 700px; height: 100px; min-height: 200px">    
    <div style="position: relative; bottom: 0px;">
	   <div class="column">
	     <img src="/public/css/Surrey.png" height=70px width=auto>
	   </div>
	   <div class="column">
	     <img src="/public/css/tilburg3.png" height=70px width=auto>
	   </div>
	   <div class="column">
	     <img src="/public/css/INESC-ID.png" height=70px width=auto>
	   </div>
	   <div class="column">
	     <img src="/public/css/surrey.jpeg" height=70px width=auto>
	   </div>
	</div>
