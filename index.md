---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

# Welcome to the 2023 Quality Estimation Shared Task!

``❗`` The <a href="https://www.statmt.org/wmt23/quality-estimation-task_results.html">results of the 2023 edition</a> are available.

``❗`` Test data is now available on  [**github**](https://github.com/WMT-QE-Task/wmt-qe-2023-data/tree/main/test_data_2023).

``❗`` Codalab is now ready! See links and information below.

``❗`` To easily stay up-to-date you can also follow our [**Twitter account**](https://twitter.com/qe_task).

``❗`` Please also register to the [**QE google-group**](https://groups.google.com/g/wmt-qe-shared-task/) in order to be able to receive updates and announcements immediately, and **ask questions**.

# Codalab:


## Links
Task 1 - sentence-level:  https://codalab.lisn.upsaclay.fr/competitions/15043
Task 1 - word-level: https://codalab.lisn.upsaclay.fr/competitions/15044
Task 2 - error span detection: https://codalab.lisn.upsaclay.fr/competitions/15045 


## Instructions

Once you have created your account and registered to a competition, please make sure to:

1. Make only 1 registration for each team on Codalab;

2. Ensure you have the latest test data: especially the tokenised translations for Task 1 - word level which have been updated;

3. Follow the submission format indicated for each competition. Note that this year we do not have individual phases for each language pair. Instead, you can submit your predictions all together (in any order of language pairs), i.e. one submission may include all language pairs of a task or just the ones you want to focus on. 
To know how your submission performed, due to the leaderboard being blind, you need to manually download the scores via "View scoring error log".  Note: you will see the macro-average only if you submit to all language pairs.

4. Ensure you submit a zip file with the requested 'predictions.txt' file, and a 'metadata.txt' file that includes the following information:
    1. Team name
    2. Model description: method, use of external data, models used (we refer you to findings papers from previous years as to what information and format we expect).

5. Each participant is given a quota of 10 submissions overall, with a limit of 5 per day;

6. This year we are keeping the leaderboards private (or blind) during the "competition" phase (ending August 17th noon UTC or 23:59 AoE). After that deadline, the "post-competition" phase of each Codalab will become active and you will be able to make as many submissions as you want (still in a limit of 5 a day).
Note: only submissions received during the "competition" phase will be used to determine the winner(s) of each task, and thus will be considered for the findings paper.

7. If you have any questions/struggles, please use the Forum of the task you are participating in. This way, each question and its answers can benefit all.


# Description
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
| Announcement of results | 3rd September, 2023|
| System description submission deadline | 31st August 2023 |
| Paper submission deadline to WMT | 5th September, 2023 |
| WMT Notification of acceptance | 6th October, 2023 |
| WMT Camera-ready deadline | 18th October, 2023 |
| WMT Conference | 6-7 December, 2023 |

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
