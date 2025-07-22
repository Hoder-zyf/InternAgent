# InternAgent: When Agent Becomes the Scientist – Building Closed-Loop System from Hypothesis to Verification

[[ Paper 📓 ]](https://arxiv.org/abs/2505.16938) [[ Apply Page 💡 ]]() [[ Website 🏠 ]](https://alpha-innovator.github.io/InternAgent-project-page) [[ InternAgent Examples 🤗 ]](https://huggingface.co/U4R/InternAgent)

<i>
From One Idea to Autonomous Experimentation
</i>
</div>

# 🔥 News
  - <p style='text-align:justify'><i>2025.07.17</i>: &nbsp; 🔥 The source code of InternAgent has been partially open-sourced.
  - <p style='text-align:justify'><i>2025.07.10</i>: &nbsp; NovelSeek has be renamed to <b>InternAgent</b>. This change embodies our hopeful vision for autonomous scientific research framework, and we hope it will empower all researchers to achieve great scientific discoveries.</p>


## 📖 Overview

![InternAgent](/images/internagent_overall.png)

InternAgent can support **12** types of scientific research tasks ranging from the AI field to the science field, including reaction yield prediction, molecular dynamics, power flow estimation, time series forecasting, transcription prediction, enhancer activity prediction, sentiment classification, 2D image classification, 3D point classification, 2D semantic segmentation, 3D autonomous driving, large vision-language model fine-tuning.

## 🌟 Core Features

![Framework](/images/internagent_framework.png)

InternAgent covers three main capabilities: (1) **Self-evolving idea generation with human-interactive feedback**, (2) **Idea-to-methodology construction**, and (3) **Evolutionary experimental planning and execution**. 

It is a unified, closed-loop multi-agent system designed to automate and accelerate innovative research across scientific domains. Through intelligent agent collaboration, our system enables **end-to-end automation** from idea generation and methodology construction to experimental execution, dramatically enhancing research efficiency and creativity.

### 💡 Self-Evolving Idea Generation with Human-Interactive Feedback
- Autonomous generation, selection, and evolution of innovative research ideas through multi-agent collaboration
- Supports interactive human feedback, enabling continuous refinement of ideas with expert insights
- Dynamically integrates literature, code, and domain knowledge to inspire diverse innovation pathways

### 🏗️ Idea-to-Methodology Construction
- Systematically transforms creative ideas into actionable and verifiable research methodologies
- Integrates baseline code, literature, and expert knowledge to automatically generate comprehensive methodological frameworks
- Supports iterative refinement and traceability of research methods

### 🛠️ Evolutionary Experimental Planning and Execution
- Automates complex experimental workflow planning, code implementation, and debugging
- Employs exception-guided intelligent debugging to automatically identify and resolve code issues
- Enables adaptive evolution and continuous optimization of experimental plans

### 🤖 Multi-Agent Orchestration
- Coordinates specialized agents such as Survey, Coding, Idea Innovation, and Assessment Agents and so on 
- Manages data flow, task scheduling, and human interaction points for efficient and coherent research processes
- Supports extensibility and compatibility with diverse scientific tasks

---

**InternAgent** delivers an "end-to-end algorithmic innovation", empowering AI+X researchers to rapidly complete the full research loop—from idea to methodology to experimental validation—accelerating scientific discovery and breakthroughs.

## 🔬 Supported Research Tasks

- Suzuki Yield Prediction
- Molecular Dynamics Simulation
- Enhancer Activity Prediction
- Transcription Prediction for Perturbation Respons
- Power Flow Estimation
- Time Series Forecasting
- Semantic Segmentation
- Image Classification
- Sentiment Analysis
- Point Cloud Classification
- Point Cloud Object Detection
- VLM & LLM Fine-tuning
- ......



## 🚀 Performance

By leveraging multi-source knowledge injection, our system intelligently generates and verifies research ideas across multiple domains. Our system has significantly improved research efficiency in Suzuki Yield Prediction, Enhancer Activity Prediction, Transcription Prediction for Perturbation Respons, and so on.

## 🚀 How to use the early version, Dolphin?

### Installation

```
conda create -n dolphin python=3.11
conda activate dolphin

# Install PyPI requirements
pip install -r requirements.txt
```

### Start Auto-Research using Dolphin

```shell
bash launch_dolphin.sh

# modify launch_dolphin.py line # line 189 if round > 0
# exp_base_file_list = [List your exp dir] 
```

- Note that you need to add api_key and specify the model and topic in `launch_dolphin.sh`. You can refer to the [doc](./docs/ollama_doc.md) if you want to use self-deployed model.
- Data for Point Classfication, Image Classification, and Sentiment Classification tasks can be downloaded [here](https://drive.google.com/drive/folders/1mq1y7EWW9dgPlS26hXNa3wxL7_2vvNju?usp=sharing).

## Citation
```
@article{team2025novelseek,
  title={InternAgent: When Agent Becomes the Scientist--Building Closed-Loop System from Hypothesis to Verification},
  author={Team, InternAgent and Zhang, Bo and Feng, Shiyang and Yan, Xiangchao and Yuan, Jiakang and Yu, Zhiyin and He, Xiaohan and Huang, Songtao and Hou, Shaowei and Nie, Zheng and others},
  journal={arXiv preprint arXiv:2505.16938},
  year={2025}
}
```
