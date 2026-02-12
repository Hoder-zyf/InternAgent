# InternAgent-1.5: A Unified Agentic Framework for Long-Horizon Autonomous Scientific Discovery
> *Autonomous Discovery Across All Sciences*
- **Papers**: [InternAgent 1.0](https://arxiv.org/abs/2505.16938) | [InternAgent 1.5](https://huggingface.co/papers/2602.08990)
- **Links**: [Website](https://discovery.intern-ai.org.cn) | [HuggingFace](https://huggingface.co/collections/InternScience/internagent)


## 🔥 News
- **2026.2.12**: 🔥 🔥 Leveraging the general capabilities of InternAgent 1.5, a**nyone can now submit their algorithm tasks for optimization by opening an issue/PR in this repository.** We will **regularly update** the algorithm design results. For other scientific discovery tasks, please visit [Intern-Discovery](https://discovery.intern-ai.org.cn/org/ailab/).

- **2026.2.10**: 🔥 Official release of the [InternAgent 1.5 Technical Report](https://huggingface.co/papers/2602.08990). InternAgent 1.5 achieves leading performance on scientific reasoning benchmarks including **GAIA, HLE, GPQA, and FrontierScience**, and supports end-to-end autonomous scientific discovery tasks across **Physical, Biology, Earth, and Life Science domains**, enabling both algorithm discovery and empirical discovery (dry/wet-lab experiments).

- **2025.10.13**: InternAgent-1.0 code has been fully open-sourced, supporting end-to-end automation and autonomous evolution across 12 scientific research tasks.

- **2025.07.17**: The source code of InternAgent has been partially open-sourced. The complete version of InternAgent (covering 12 types of tasks for autonomous scientific research) will be open-sourced soon. This code repository can be used for full-cycle autonomous scientific research, ranging from hypothesis generation to automated experimental execution.

- **2025.07.10**: *NovelSeek* has been renamed to **InternAgent**. This change embodies our hopeful vision for autonomous scientific research framework, and we hope it will empower all researchers to achieve great scientific discoveries.

---

## 📖 Overview

![InternAgent](assets/internagent_overall.png)

**InternAgent 1.5** is a unified autonomous system for end-to-end scientific discovery across both **Algorithm Discovery** and **Empirical Discovery**. Building on InternAgent 1.0, it organizes scientific inquiry into three coordinated subsystems: **Generation** (hypothesis construction via deep research), **Verification** (methodological evaluation via solution refinement), and **Evolution** (evidence-driven refinement via long-horizon memory).
![Benchmark](assets/benchmark.png)
InternAgent 1.5 achieves **leading performance** on scientific reasoning benchmarks (GAIA, HLE, GPQA, FrontierScience, SGI-bench) and demonstrates **sustained autonomous optimization** across extended discovery cycles. The system supports **algorithm discovery** (agent memory, reinforcement learning, test-time scaling, ...) and **empirical discovery** workflows (dry-lab simulations and wet-lab experimentation) across Physical, Biological, Earth, and Life Sciences.
![Capability](assets/capability.png)

---
## 🌟 Core Features

![Framework](assets/internagent_framework.png)

InternAgent 1.5 is built on three foundational subsystems that enable autonomous scientific discovery:

### 🔍 Generation: Deep Research for Hypothesis Construction
- Autonomous literature analysis and knowledge synthesis across scientific domains
- Multi-source information integration from papers, code repositories, and domain-specific databases
- Structured hypothesis formulation grounded in existing scientific evidence

### ✅ Verification: Solution Refinement for Methodological Evaluation
- Systematic transformation of hypotheses into executable experimental protocols
- Automated code generation, debugging, and execution across computational and experimental environments
- Exception-guided intelligent error correction and iterative solution optimization

### 🔄 Evolution: Long-Horizon Memory for Evidence-Driven Refinement
- Persistent memory architecture that accumulates knowledge across extended research cycles
- Cross-iteration learning from experimental outcomes and methodological feedback
- Adaptive optimization that continuously refines hypotheses and experimental designs

### 🧩 Three-Subsystem Coordination
- **Generation → Verification → Evolution** forms a complete discovery cycle
- Seamless integration of dry-lab (computational modeling) and wet-lab (physical experimentation) workflows
- Extensible architecture supporting diverse tasks across Algorithm Discovery and Empirical Discovery

**InternAgent 1.5** delivers end-to-end autonomous scientific discovery, enabling researchers to complete the full cycle—from hypothesis generation to experimental validation—across Physical, Biological, Earth, and Life Sciences.

---
## 🔬 Supported Research Tasks

**Scientific Algorithm Discovery**
- Suzuki–Miyaura Reaction Yield Prediction
- Transcription Prediction for Perturbation Response
- Power Flow Estimation
- Time Series Forecasting
- Molecular Dynamics Simulation
- Enhancer Activity Prediction

**AI Algorithm Discovery**
- Test-Time Scaling for LLM Reasoning
- Long-Term Memory Management for Agents
- Self-Distillation for Mathematical Reasoning
- Test-Time Reinforcement Learning

**Empirical Discovery**
- Automated Climate Diagnostics
- Climate Downscaling Optimization
- Biological Evidence Synthesis for Target Discovery
- Hypothesis Generation and Target Prioritization
- Fluorescent Protein Engineering
- Automated Reaction Outcome Prediction
- Generative Scaffold Hopping
*And more...*

---

## 🎉 Benchmark Results

### Results on Al Research Tasks

InternAgent consistently improves upon the baseline and outperforms Dolphin across all tasks, spanning AI and scientific domains.

#### Max Performance

| Task | Metric | Baseline | Dolphin | InternAgent |
|------|--------|----------|---------|-------------|
| AutoRYP | R² ↑ | 27.6 | 31.8 (+4.2) | **35.4 (+7.8)** |
| AutoMD | Forces-MAE ↓ | 0.158 | 0.152 | **0.148** |
| AutoPower | RMSE ↓ | 0.00473 | 0.00455 | **0.00426** |
| AutoTSF | MAE ↓ | 0.4382 | 0.4627 | **0.4331** |
| AutoTPPR | MSE ↓ | 0.197 | 0.173 | **0.146** |
| AutoEAP | HK-PCC ↑ | 0.65 | 0.76 | **0.79** |
| AutoSenCls | Acc ↑ | 91.0 | 92.5 (+1.5) | **93.5 (+2.5)** |
| Auto2DCls | Top-1 Acc ↑ | 81.2 | 82.0 (+0.8) | **83.3 (+2.1)** |
| Auto3DCls | OA ↑ | 91.0 | 93.9 (+2.9) | **95.5 (+4.5)** |
| Auto2DSeg | mIoU ↑ | 78.8 | - | **81.0 (+2.2)** |
| AutoPCDet | mAP ↑ | 65.0 | - | **65.9 (+0.9)** |
| AutoVLM | QA ↑ | 67.1 | - | **67.6 (+0.5)** |

#### Average Performance

| Task | Metric | Baseline | Dolphin | InternAgent |
|------|--------|----------|---------|-------------|
| AutoRYP | R² ↑ | 27.6 | 31.3 (+3.7) | **33.5 (+5.9)** |
| AutoMD | Forces-MAE ↓ | 0.158 | 0.155 | **0.152** |
| AutoPower | RMSE ↓ | 0.00473 | 0.00459 | **0.00447** |
| AutoTSF | MAE ↓ | 0.4382 | - | **0.4346** |
| AutoTPPR | MSE ↓ | 0.197 | 0.179 | **0.170** |
| AutoEAP | HK-PCC ↑ | 0.65 | 0.73 | **0.77** |
| AutoSenCls | Acc ↑ | 91.0 | 91.8 (+0.8) | **92.5 (+1.5)** |
| Auto2DCls | Top-1 Acc ↑ | 81.2 | 81.8 (+0.6) | **82.2 (+1.0)** |
| Auto3DCls | OA ↑ | 91.0 | 92.0 (+1.0) | **93.4 (+2.4)** |
| Auto2DSeg | mIoU ↑ | 78.8 | - | **80.1 (+1.3)** |
| AutoPCDet | mAP ↑ | 65.0 | - | **65.7 (+0.7)** |
| AutoVLM | QA ↑ | 67.1 | - | **67.6 (+0.5)** |

---

### 🧪 GAIA, GPQA-Diamond, FrontierScience and HLE Benchmarks

InternAgent-1.5 achieved state-of-the-art results across multiple benchmarks.
### Humanity's Last Exam (HLE)

| Setting | Model | Math | Bio/Med | CS/AI | Physics | Human. | Chem. | Engineer. | Other | Avg. |
|---------|-------|------|---------|-------|---------|--------|-------|-----------|-------|------|
| **Text-Only** | Deepseek-R1 | 9.30 | 8.60 | 7.40 | 5.80 | 11.00 | 5.60 | 10.30 | 7.50 | 8.60 |
| | Gemini-3-pro-preview | 45.08 | 26.13 | 26.79 | 32.67 | 44.04 | **34.65** | **29.69** | 32.39 | 38.00 |
| | **InternAgent-1.5** | **48.96** | **30.63** | **29.46** | **34.16** | **44.56** | 30.69 | 28.13 | **37.50** | **40.87** |
| **All-Set** | o4-mini | 19.00 | 11.40 | 12.90 | 12.60 | 9.10 | 12.70 | 12.60 | 6.90 | 14.30 |
| | GPT-5 | 31.00 | 22.10 | 24.90 | 21.70 | 20.60 | 16.40 | 14.40 | 18.00 | 24.80 |
| | Gemini-3-pro-preview | 44.76 | 27.14 | 29.05 | 31.30 | **42.92** | **40.00** | **32.43** | 34.33 | 38.04 |
| | **InternAgent-1.5** | **48.09** | **30.36** | **30.71** | **33.04** | 42.47 | 34.55 | 30.63 | **38.63** | **40.00** |

---

### FrontierScience Benchmark

| Method | **Olympiad (avg N=20)** |  |  |  | **Research (avg N=30)** |  |  |  |
|--------|---------|---------|---------|---------|---------|---------|---------|---------|
|  | **Bio** | **Chem** | **Phy** | **All** | **Bio** | **Chem** | **Phy** | **All** |
| o4-mini | **47.00±14.90** | 65.00±6.40 | 53.40±4.50 | 57.40±3.30 | 9.67±5.47 | 8.17±4.37 | 0.83±2.27 | 6.20±2.54 |
| InternS1-235B | 17.00±12.69 | 52.88±4.05 | 50.40±3.88 | 48.05±2.84 | 4.50±4.35 | 11.00±3.74 | 2.67±3.35 | 6.06±2.30 |
| Mirothinker-v1.5-30B-A3B | 22.86±4.52 | 69.64±7.49 | 54.86±3.18 | 57.57±3.66 | 8.17±6.39 | 8.50±6.21 | 5.83±4.10 | 7.50±3.77 |
| DeepSeek-V3.2-Thinking | 26.50±7.26 | 72.25±3.25 | 66.30±2.63 | 64.70±2.41 | 2.50±3.10 | 16.33±4.64 | 1.40±2.70 | 6.84±1.88 |
| Qwen3-235B-A22B-Thinking | 24.00±9.17 | 61.13±6.05 | 57.10±4.79 | 55.40±3.68 | 10.17±5.08 | 10.00±6.32 | 1.58±2.41 | 7.34±3.37 |
| Qwen3-30B-A3B-Thinking | 13.50±9.10 | 47.25±4.47 | 42.70±3.65 | 41.60±2.94 | 1.50±2.93 | 2.00±3.32 | 0.70±1.79 | 1.41±1.52 |
| **InternAgent-1.5** | 46.00±8.00 | **85.50±3.67** | **76.80±2.99** | **77.20±3.06** | **10.33±4.64** | **22.00±6.00** | **3.67±2.87** | **12.00±2.49** |

---

### GPQA-Diamond Benchmark

| Agent | Bio | Chem | Phys | Avg. |
|-------|-----|------|------|------|
| **Base Models** |  |  |  |  |
| Qwen-3-8B | - | - | - | 44.44 |
| Qwen3-32B | - | - | - | 49.49 |
| Qwen3-235B | - | - | - | 47.47 |
| Intern-S1 | **89.47** | 59.49 | 93.02 | 78.26 |
| Deepseek-R1 | 63.16 | 76.34 | 91.86 | 82.32 |
| o4-mini | 78.95 | 63.44 | 94.19 | 78.28 |
| GPT-5 | 84.21 | 76.34 | 95.35 | 85.35 |
| **React Model with Tools** |  |  |  |  |
| WebShaper | 47.37 | 52.69 | 81.40 | 64.65 |
| MiroThinker | 84.21 | 75.27 | 95.35 | 84.85 |
| Tongyi DR | 78.95 | 67.74 | 95.35 | 80.30 |
| **InternAgent-1.5** | 84.21 | **79.57** | **96.51** | **87.37** |

---
## 🚀🚀 Getting Started with InternAgent 1.5

### Algorithm Discovery Tasks
For **algorithm discovery tasks** such as Reinforcement Learning, Test-time Scaling, Agent Memory... we currently support access to InternAgent 1.5 by **submitting an issue or pull request in this repository**. Please describe your optimization task, and we will regularly update the algorithm design results.

### Empirical Discovery Tasks
For **empirical discovery tasks** including computational modeling, dry-lab simulations, and wet-lab experimentation across Physical, Biological, Earth, and Life Sciences, please visit **[Intern-Discovery](https://discovery.intern-ai.org.cn/org/ailab/)**.

***Stay tuned for more updates as we expand access and capabilities!***

## 🚀 Getting Started with InternAgent 1.0

### Installation

```bash
conda create -n InternAgent python=3.11
conda activate InternAgent

# Install PyPI requirements
pip install -r requirements.txt

# Install aider
python -m pip install -U --upgrade-strategy only-if-needed aider-chat
```

### Set Your API Key

Rename `.env.example` to `.env` and fill in your API keys:

```bash
mv .env.example .env
```

### Start Your Research Project

```bash
./scripts/run_pipeline.sh
```

**Configuration Tips:**
- Modify `configs/config.yaml` to customize your research project
- Results will be saved in the `results/` directory
- Check logs in the `logs/` directory
- To skip idea generation, refer to `scripts/run_skip-idea.sh`
- Visualize idea evolution using `internagent/vis_tree.py`

### About Research Tasks

We provide the tasks mentioned in our technical report as examples. Each task has different training environments and datasets. Please refer to the code in each task's folder for configuration details.

---

## 📝 Citation

```bibtex
@article{feng2026internagent,
  title={InternAgent-1.5: A Unified Agentic Framework for Long-Horizon Autonomous Scientific Discovery},
  author={Shiyang Feng and Runmin Ma and Xiangchao Yan and Yue Fan and Yusong Hu and Songtao Huang and Shuaiyu Zhang and Zongsheng Cao and Tianshuo Peng and Jiakang Yuan and Zijie Guo and Zhijie Zhong and Shangheng Du and Weida Wang and Jinxin Shi and Yuhao Zhou and Xiaohan He and Zhiyin Yu and Fangchen Yu and Bihao Zhan and Qihao Zheng and Jiamin Wu and Mianxin Liu and Chi Zhang and Shaowei Hou and Shuya Li and Yankai Jiang and Wenjie Lou and Lilong Wang and Zifu Wang and Jiong Wang and Wanghan Xu and Yue Deng and Dongrui Liu and Yiheng Wang and Wenlong Zhang and Fenghua Ling and Shufei Zhang and Xiaosong Wang and Shuangjia Zheng and Xun Huang and Siqi Sun and Shuyue Hu and Peng Ye and Chunfeng Song and Bin Wang and Conghui He and Yihao Liu and Xin Li and Qibin Hou and Tao Chen and Xiangyu Yue and Bin Wang and Liang He and Dahua Lin and Bowen Zhou and Bo Zhang and Lei Bai},
  journal={arXiv preprint arXiv:2602.08990},
  year={2026}
}
```

```bibtex
@article{team2025internagent,
  title={InternAgent: When Agent Becomes the Scientist--Building Closed-Loop System from Hypothesis to Verification},
  author={Team, InternAgent and Zhang, Bo and Feng, Shiyang and Yan, Xiangchao and Yuan, Jiakang and Ma, Runmin and Hu, Yusong and Yu, Zhiyin and He, Xiaohan and Huang, Songtao and others},
  journal={arXiv e-prints},
  pages={arXiv--2505},
  year={2025}
}
```

```bibtex
@article{hu2025flowsearch,
  title={FlowSearch: Advancing deep research with dynamic structured knowledge flow},
  author={Yusong Hu and Runmin Ma and Yue Fan and Jinxin Shi and Zongsheng Cao and Yuhao Zhou and Jiakang Yuan and Xiangchao Yan and Wenlong Zhang and Lei Bai and Bo Zhang},
  journal={arXiv preprint arXiv:2510.08521},
  year={2025}
}
```

```bibtex
@article{du2025automlgen,
  title={AutoMLGen: Navigating Fine-Grained Optimization for Coding Agents},
  author={Shangheng Du and Xiangchao Yan and Dengyang Jiang and Jiakang Yuan and Yusong Hu and Xin Li and Liang He and Bo Zhang and Lei Bai},
  journal={arXiv preprint arXiv:2510.08521},
  year={2025}
}
```
