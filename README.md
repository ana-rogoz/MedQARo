# RoMedQA: The First Benchmark for Medical Question Answering in Romanian

Question answering (QA) is an actively studied topic, being a core natural language processing (NLP) task that needs to be addressed before achieving Artificial General Intelligence (AGI). However, the lack of QA datasets in specific domains and languages hinders the development of robust AI models able to generalize across various domains and languages. To this end, we introduce RoMedQA, the first Romanian QA benchmark for the medical domain, alongside a comprehensive evaluation of state‐of‐the‐art large language models (LLMs). We construct a high‑quality and large-scale dataset comprising 102,646 QA pairs related to cancer patients. The questions regard medical case summaries of 1,011 patients, requiring either keyword extraction or reasoning to be answered correctly. RoMedQA is the result of a time-consuming manual annotation process carried out by seven physicians specialized in oncology or radiotherapy, who spent a total of about 2,100 work hours to generate the QA pairs. We experiment with four LLMs from distinct families of models on RoMedQA. Each model is employed in two scenarios, namely one based on zero‑shot prompting and one based on supervised fine‑tuning. Our results show that fine‑tuned models significantly outperform their zero-shot counterparts, clearly indicating that pretrained models fail to generalize on RoMedQA. Our findings demonstrate the importance of both domain‐specific and language‐specific fine-tuning for reliable clinical QA in Romanian.



# License
The dataset and code are released under: [Creative Commons Attribution Non Commercial Share Alike 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.en)


# 📑 Table of Contents
<a name = "tabel_of_contents"></a>

  - [About ](#about-)
  - [Dataset](#dataset-)
  - [Methods](#method-)
  - [Getting Started ](#getting-started-)
  - [Usage ](#usage-)
  - [Developed with ](#️-developed-with-)


## About <a name = "about"></a>

We introduce **RoMedQA**, the first and only large-scale medical QA dataset in Romanian, comprising 102,646 QA instances obtained with the help of trained physicians. For our dataset, we benchmark four LLMs from distinct families of models across multiple configurations and report comprehensive performance metrics under both zero-shot and fine-tuning configurations. We release the dataset, together with the relevant code to reproduce the results in this repository. 

### Dataset <a name = "dataset"></a>

Given the size of our dataset, we make it available externally at the following [link](https://drive.proton.me/urls/TRYG8BYNH0#6od8qxDPk8qy). 

|                | Number of patients              |                     |       | Number of samples              |                     |       |
|----------------|---------------------------------|---------------------|-------|--------------------------------|---------------------|-------|
|                | Train                           | Validation          | Test  | Train                          | Validation          | Test  |
| Breast cancer  | 557                             | 119                 | 120   | 53,472                         | 11,424              | 11,520|
| Lung cancer    | 150                             | 32                  | 33    | 18,300                         | 3,904               | 4,026 |
| **Total**      | **707**                         | **151**             | **153** | **71,772**                    | **15,328**          | **15,546** |
|                | **Total: 1,011**                |                     |       | **Total: 102,646**             |                     |       |


### Methods <a name = "method"></a>

## Getting Started <a name = "getting_started"></a>

There are no environment dependencies that should be installed, although the dataset should be downloaded before running each of the the notebooks.

## Usage <a name="usage"></a>

The training and testing of the models is performed by running the notebook with the respective model name.


