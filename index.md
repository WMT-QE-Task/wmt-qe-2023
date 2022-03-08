---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

# Welcome to the 2022 Quality Estimation Shared Task!

This shared task focuses on automatic methods for estimating the quality of neural machine translation output at run-time, without relying on reference translations. It will cover estimation at sentence and word levels. This year we introduce the following new elements:

- Updated quality annotation scheme: quality annotations for the majority of the tasks are now based on <strong>Multidimentional Quality Metrics (MQM)</strong> instead of direct assessments.
- MQM annotated data aligned with the  <a href="https://wmt-metrics-task.github.io/">Metrics shared task</a>: we share part of the data used in this year's Metrics task, to promote research that bridges the two domains.
- <strong>New language pairs:</strong> we introduce a novel dataset on English-Marathi, with sentence level and word level annotations (direct assesments).
- An <strong>explability subtask</strong>, following up on the first edition of Eval4NLP shared task.
- Updated catastrophic error detection task: TBA.
  
Have questions or suggestions? Feel free to <a href="mailto:andre.t.martins@gmail.com">Contact Us</a>!


## Metrics Task Important Dates

|  | Date |
| ----------- | :-----------: |
| Release of training and dev data | TBA |
| Release of test data | TBA |
| Test predictions deadline | TBA |

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

1. [Quality prediction](./subtasks/task1/): **TBA**
2. [Explainable Quality Estimation](./subtasks/task2/): **TBA**
3. [Critical Error Detection](./subtasks/task3/): **TBA**

## Submission Information
The shared task competition will take place on CODALAB. Details **TBA**

## Useful Software
Here are some open source software for QE that might be useful for participants:
- OpenKiwi
- DeepQuest-py
- TransQuest

## Submission Requirements
Each participating team can submit at most 15 systems for each of the language pairs of each subtask, except for the multilingual track of tasks 1 & 2 (10 systems max). These should be submitted to a CODALAB page for each subtask.
Please check that your system output on the dev data is correctly read by the official evaluation scripts.

## Organization:

- Chrysoula Zerva (Instituto de Telecomunicações)
- André Martins (Instituto de Telecomunicações, Unbabel)
- Marina Fomicheva (University of Sheffield)
- Frédéric Blain (University of Wolverhampton)
- Ricardo Rei (INESC-ID, Unbabel)
- José Souza (Unbabel)
- Diptesh Kanojia (University of Surrey)
- Constantin Orasan (University of Surrey)
- Lucia Specia (Imperial College London)

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
	     <img src="/public/css/Sheffield.png" height=70px width=auto>
	   </div>
	</div>
<div style="position: relative; width: 700px; height: 100px; min-height: 200px">    
    <div style="position: relative; bottom: 0px;">
	   <div class="column">
	     <img src="/public/css/Surrey.png" height=70px width=auto>
	   </div>
	   <div class="column">
	     <img src="/public/css/Wolverhampton.jpeg" height=70px width=auto>
	   </div>
	   <div class="column">
	     <img src="/public/css/INESC-ID.png" height=70px width=auto>
	   </div>
	   <div class="column">
	     <img src="/public/css/Imperial.jpeg" height=70px width=auto>
	   </div>
	</div>