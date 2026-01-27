# MedQARo: A Large-Scale Benchmark for Medical Question Answering in Romanian

We introduce MedQARo, the first large-scale medical QA benchmark in Romanian, alongside a comprehensive evaluation of state-of-the-art large language models (LLMs). We construct a high-quality and large-scale dataset comprising \hl{105,880} QA pairs about cancer patients \hl{from two medical centers}. The questions regard medical case summaries of \hl{1,242} patients, requiring both keyword extraction and reasoning. Our benchmark contains both in-domain and cross-domain (cross-center and cross-cancer) test collections, enabling a precise assessment of generalization capabilities. We experiment with four open-source LLMs from distinct families of models on MedQARo. Each model is employed in two scenarios: zero-shot prompting and supervised fine-tuning. We also evaluate two state-of-the-art LLMs exposed only through APIs, namely GPT-5.2 and Gemini 3 Flash. Our results show that fine-tuned models significantly outperform zero-shot models}, indicating that pretrained models fail to generalize on MedQARo. Our findings demonstrate the importance of both domain-specific and language-specific fine-tuning for reliable clinical QA in Romanian.

# License
The dataset and code are released under: [Creative Commons Attribution Non Commercial Share Alike 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.en)


# 📑 Table of Contents
<a name = "tabel_of_contents"></a>

  - [About ](#about-)
  - [Dataset](#dataset-)
  - [Methods](#methods-)
  - [Getting Started ](#getting-started-)
  - [Usage ](#usage-)


## About <a name = "about"></a>

We introduce **MedQARo**, the first and only large-scale medical QA dataset in Romanian, comprising 105,880 QA instances obtained with the help of trained physicians. For our dataset, we benchmark four LLMs from distinct families of models across multiple configurations and report comprehensive performance metrics under both zero-shot and fine-tuning configurations. We release the dataset, together with the relevant code to reproduce the results in this repository. 

### Dataset <a name = "dataset"></a>

Given the size of our dataset, we make it available externally at the following [link](https://drive.proton.me/urls/2ADFAY7YA0#Zu701wPBQXjs). 

We also present the detailed stats and composition of our dataset in the table below:

|                    | Number of patients |            |        | **Total** | Number of samples |            |        | **Total** |
|--------------------|--------------------|------------|--------|-----------|-------------------|------------|--------|-----------|
|                    | Train              | Validation | Test   |           | Train             | Validation | Test   |           |
| Breast cancer      | 557                | 119        | 120    | 796       | 53,472            | 11,424     | 11,520 | 76,416    |
| Lung cancer        | 150                | 32         | 33     | 215       | 18,300            | 3,904      | 4,026  | 26,230    |
| Other diagnosis    | –                  | –          | –      | 231       | –                 | –          | –      | 3,234     |
| **Total**          | **707**            | **151**    | **153**| **1,242** | **71,772**        | **15,328** | **15,546** | **105,880** |
|                    | **Unique: 1,011**  |            |        |           | **Unique: 102,646** |            |        |           |

### Methods <a name = "methods"></a>

In our work, we fine-tuned the following four models:
* [OpenLLM-Ro/RoLlama2-7b-Instruct](https://huggingface.co/OpenLLM-Ro/RoLlama2-7b-Instruct)
* [RoMistral-7b-Instruct](https://huggingface.co/OpenLLM-Ro/RoMistral-7b-Instruct)
* [Llama3-OpenBioLLM-8B](https://huggingface.co/aaditya/Llama3-OpenBioLLM-8B)
* [Phi-4-mini-instruct](https://huggingface.co/microsoft/Phi-4-mini-instruct)

## Getting Started <a name = "getting_started"></a>

There are no environment dependencies that should be installed, although the dataset should be downloaded before running each of the the notebooks.

## Usage <a name="usage"></a>
We make available under the `Fine tuning` dir the model fine-tuning, using our official data split and model config. After completing the fine-tuning, one can use our script under the `Evaluate` dir for assesing the performance of their model.

