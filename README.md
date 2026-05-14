# Awesome Fine-Grained Multimodal Perception [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

<p align="center">
    <img src="icon.png" alt="Overview" width="100%">
</p>

A curated collection of the latest research and resources on **Fine-Grained Multimodal Perception**. This repository encompasses datasets, benchmarks, research papers, and practical methods for enhancing fine-grained perception capabilities in Multimodal Large Language Models (MLLMs).

🚀🚀🚀 Contributions are welcome! If you find any missing papers, datasets, or tools, feel free to open an issue or submit a pull request.

## Contents
- [Introduction](#introduction)
- [Benchmarks & Datasets](#benchmarks--datasets)
- [Research Papers](#research-papers)
  - [Data-Centric Methods](#data-centric-methods)
  - [Training-Free Methods](#training-free-methods)
  - [Agentic Methods (Thinking with Images)](#agentic-thinking-with-images)
  - [Training-Based Methods](#training-based-methods)
    - [Supervised Fine-Tuning & Distillation](#supervised-fine-tuning--distillation)
    - [Reinforcement Learning](#reinforcement-learning)
- [Applications & Domains](#applications--domains)
- [About Our Team](#-about-our-team)

---

## Introduction

Multimodal Large Language Models (MLLMs) excel at broad visual understanding but still struggle with **fine-grained perception**, where decisive evidence is small and easily overwhelmed by global context. Recent advancements have shifted towards a **"Thinking-with-Images"** paradigm, where MLLMs actively acquire local information during inference rather than relying solely on a global image encoding.

This awesome list categorizes methods into four paradigms:

- **Data-Centric Methods**: Improving perception through data quality, quantity, and synthetic generation
- **Training-Free Methods**: Enhancing perception at inference time via prompting, chain-of-thought, and attention strategies
- **Agentic: Thinking with Images**: Actively interacting with images through tools (zoom, crop, search, edit) during inference
- **Training-Based Methods**: Improving perception through supervised fine-tuning, distillation, and reinforcement learning

⬆ [Back to Top](#contents)

---

## Benchmarks & Datasets

> **Task Legend:** `FG`: Fine-Grained Perception | `OCR`: Text Recognition | `Cnt`: Counting | `Grd`: Grounding | `Rea`: Reasoning

| Benchmark | Paper | Venue & Year | Task | Highlights | Download |
| :-------- | :---- | :----------- | :--- | :--------- | :------- |
| GeoBrowse | [GeoBrowse: A Geolocation Benchmark for Agentic Tool Use with Expert-Annotated Reasoning Traces](https://arxiv.org/abs/2604.04017v1) | Arxiv 2026 | `FG`, `Rea` | Geolocation benchmark, agentic tool use, expert reasoning traces | [Arxiv](https://arxiv.org/abs/2604.04017v1) |
| VisuRiddles | [VisuRiddles: Fine-grained Perception is a Primary Bottleneck for Multimodal Large Language Models in Abstract Visual Reasoning](https://arxiv.org/abs/2506.02537) | AAAI 2026 | `FG` | Visual riddles, fine-grained perception evaluation | [Arxiv](https://arxiv.org/abs/2506.02537) |
| ZoomBench | [Zooming without Zooming: Region-to-Image Distillation for Fine-Grained Multimodal Perception](https://arxiv.org/abs/2602.11858) | Arxiv 2026 | `FG`, `Rea` | 845 VQA samples, 6 perceptual dimensions, dual-view evaluation | [GitHub](https://github.com/inclusionAI/Zooming-without-Zooming) |
| RTV-Bench | [RTV-Bench: Benchmarking MLLM Continuous Perception](https://arxiv.org/abs/2505.02064) | ICLR 2026 | `FG`, `Rea` | Real-time video analysis, 552 videos, 4,608 QA pairs, multi-timestamp reasoning | N/A |
| SFE | [Scientists' First Exam: Probing Cognitive Abilities of MLLM via Perception, Understanding, and Reasoning](https://arxiv.org/abs/2506.10521) | ICLR 2026 | `FG`, `Rea` | Scientific cognitive evaluation, three interconnected levels | [GitHub](https://github.com/PrismaX-Team/sfe) |
| VStar | [V*: Guided Visual Search as a Core Mechanism in Multimodal LLMs](https://arxiv.org/abs/2312.14135) | CVPR 2024 | `FG` | Visual search, attribute recognition | [GitHub](https://github.com/penghao-wu/vstar) |
| CV-Bench | [Cambrian-1: A Fully Open, Vision-Centric Exploration of Multimodal LLMs](https://arxiv.org/abs/2406.16860) | CVPR 2024 | `FG`, `Rea` | Computer vision-centric benchmark | [HuggingFace](https://huggingface.co/datasets/nyu-visionx/CV-Bench) |
| HR-Bench | [Divide and Conquer: A Comprehensive Benchmark for High-Resolution Image Understanding](https://arxiv.org/abs/2408.15556) | AAAI 2025 | `FG` | High-resolution image understanding | [GitHub](https://github.com/hrbench/HR-Bench) |
| CountQA | [CountQA: How Well Do MLLMs Count in the Wild?](https://arxiv.org/abs/2508.06585) | Arxiv 2025 | `Cnt` | Visual counting with reasoning | [GitHub](https://github.com/CountQA/CountQA) |
| CoCoT | [CoCoT: Contrastive Chain-of-Thought Prompting for Large Multimodal Models with Multiple Image Inputs](https://arxiv.org/abs/2401.02582) | Arxiv 2024 | `Grd` | Visual grounding with reasoning | N/A |
| Thyme-SFT/RL | [Thyme: Thinking with Images for Visual Reasoning](https://arxiv.org/abs/2508.11630) | Arxiv 2025 | `FG`, `Rea` | Visual reasoning with tool use | [GitHub](https://github.com/thyme) |
| Visual Probe | [Mini-o3: Scaling Up Reasoning Patterns and Interaction Turns for Visual Search](https://arxiv.org/abs/2509.07969) | Arxiv 2025 | `FG` | Visual probing for perception | [GitHub](https://github.com/Mini-o3/Mini-o3) |
| Rexverse | [ChatRex: Taming Multimodal LLM for Joint Perception and Understanding](https://arxiv.org/abs/2411.18363) | Arxiv 2024 | `FG` | Fine-grained visual understanding | [GitHub](https://github.com/rexverse) |
| Visual Genome | [Visual Genome: Connecting Language and Vision Using Crowdsourced Dense Image Annotations](https://arxiv.org/abs/1602.07332) | IJCV 2017 | `Grd`, `FG` | Dense image annotations, grounding | [VisualGenome](https://visualgenome.org/) |
| MMVP | [Eyes Wide Shut? Exploring the Visual Shortcomings of Multimodal LLMs](https://arxiv.org/abs/2401.06209) | CVPR 2024 | `FG` | Visual shortcomings evaluation | [GitHub](https://github.com/mmvp/MMVP) |
| ColorBench | [ColorBench: Can VLMs See and Understand the Colorful World? A Benchmark for Color Perception](https://arxiv.org/abs/2504.10514) | Arxiv 2025 | `FG` | Color perception evaluation | [GitHub](https://github.com/tianyi-lab/ColorBench) |
| GroundingME | [GroundingME: Grounding Multi-Modal Evaluation](https://arxiv.org/abs/2512.17495) | Arxiv 2025 | `Grd` | Multi-modal grounding evaluation | N/A |
| MME-RealWorld | [MME-RealWorld: Evaluating Real-World Perception in MLLMs](https://arxiv.org/abs/2408.13257) | Arxiv 2024 | `FG`, `Grd` | Real-world perception benchmark | [GitHub](https://github.com/MME-RealWorld) |
| TreeBench | [Traceable Evidence Enhanced Visual Grounded Reasoning: Evaluation and Methodology](https://arxiv.org/abs/2507.07999) | Arxiv 2025 | `Rea` | Traceable reasoning evaluation | [GitHub](https://github.com/Haochen-Wang409/TreeVGR) |

⬆ [Back to Top](#contents)

---

## Research Papers

> **💡 Note:** Papers are sorted by year (descending) within each category.

### Data-Centric Methods

*This category focuses on methods that improve fine-grained perception through data quality, quantity, and synthetic data generation pipelines.*

| Title | Venue & Year | Highlights/Keywords | Code |
| --- | --- | --- | --- |
| [First SFT, Second RL, Third UPT: Continual Improving Multi-Modal LLM Reasoning via Unsupervised Post-Training](https://arxiv.org/abs/2505.22453) | Arxiv 2025 | Unsupervised Pre-training | [GitHub](https://github.com/waltonfuture/MM-UPT) |
| [Oasis: One Image is All You Need for Multimodal Instruction Data Synthesis](https://arxiv.org/abs/2503.08741) | Arxiv 2025 | Autonomous Synthesis, Open-source | [GitHub](https://github.com/Letian2003/MM_INF) |
| [MMEvol: Empowering Multimodal Large Language Models with Evol-Instruct](https://arxiv.org/abs/2409.05840) | Arxiv 2025 | Evolution, Instruction Tuning | N/A |
| [Hallucination at a Glance: Controlled Visual Edits and Fine-Grained Multimodal Learning](https://arxiv.org/abs/2506.07227) | Arxiv 2025 | Minimally Edited, Difference Detection | N/A |
| [Multimodal Self-Instruct: Synthetic Abstract Image and Visual Reasoning Instruction Using Language Model](https://arxiv.org/abs/2407.07053) | Arxiv 2024 | Self-Instruct, Synthetic Data | [GitHub](https://github.com/zwq2018/Multi-modal-Self-instruct) |
| [Genixer: Empowering Multimodal Large Language Models as a Powerful Data Generator](https://arxiv.org/abs/2312.06731) | Arxiv 2024 | VQA Generation, Unlabeled Images | [GitHub](https://github.com/zhaohengyuan1/Genixer) |

⬆ [Back to Top](#contents)

---

### Training-Free Methods

*This category covers inference-time approaches that enhance fine-grained perception without additional training, leveraging prompting strategies, chain-of-thought reasoning, and attention mechanisms.*

| Title | Venue & Year | Highlights/Keywords | Code |
| --- | --- | --- | --- |
| [See It, Say It, Sorted: An Iterative Training-Free Framework for Visually-Grounded Multimodal Reasoning in LVLMs](https://arxiv.org/abs/2602.21497v2) | Arxiv 2026 | Training-Free, Iterative, Visually-Grounded Reasoning | N/A |
| [Q-Zoom: Query-Aware Adaptive Perception for Efficient Multimodal Large Language Models](https://arxiv.org/abs/2604.06912v1) | Arxiv 2026 | Query-Aware, Adaptive Perception, Efficient Zoom | N/A |
| [ERGO: Efficient High-Resolution Visual Understanding for Vision-Language Models](https://arxiv.org/abs/2509.21991v2) | Arxiv 2025 | Efficient High-Resolution, Visual Understanding | N/A |
| [SvfEye: A Semantic-Visual Fusion Framework with Multi-Scale Visual Context for Multimodal Reasoning](https://arxiv.org/abs/2603.00171v2) | Arxiv 2026 | Semantic-Visual Fusion, Multi-Scale Context | N/A |
| [Imagine while Reasoning in Space: Multimodal Visualization-of-Thought](https://arxiv.org/abs/2501.07542) | Arxiv 2025 | Spatial Visualization, Imaginative Reasoning | N/A |
| [Socratic Questioning: Learn to Self-guide Multimodal Reasoning in the Wild](https://arxiv.org/abs/2501.02964) | Arxiv 2025 | Self-guided Reasoning, Socratic Method | N/A |
| [ZoomEye: Enhancing Multimodal LLMs with Human-Like Zooming Capabilities through Tree-Based Search](https://arxiv.org/abs/2411.16044) | Arxiv 2025 | Tree Search, Attention Mapping | [GitHub](https://github.com/om-ai-lab/ZoomEye) |
| [Adaptive Chain-of-Focus Reasoning via Dynamic Visual Search and Zooming for Efficient VLMs](https://arxiv.org/abs/2505.15436) | Arxiv 2025 | Focusing Strategy, Chain Reasoning | N/A |
| [Hide: Rethinking the zoom-in method in high resolution mllms via hierarchical decoupling](https://arxiv.org/abs/2510.00054) | Arxiv 2025 | Attention-based Detection | [GitHub](https://github.com/Tennine2077/HiDe) |
| [Image-of-Thought Prompting for Visual Reasoning Refinement in Multimodal Large Language Models](https://arxiv.org/abs/2405.13872) | Arxiv 2024 | Image-of-Thought, Reasoning Refinement | N/A |
| [Mind's Eye of LLMs: Visualization-of-Thought Elicits Spatial Reasoning in Large Language Models](https://arxiv.org/abs/2404.03622) | NeurIPS 2024 | Visualization-of-Thought, Spatial Reasoning | [GitHub](https://github.com/MichaelStott/Minds-Eye) |
| [Compositional Chain-of-Thought Prompting for Large Multimodal Models](https://arxiv.org/abs/2311.17076) | CVPR 2024 | Compositional Prompting | [GitHub](https://github.com/chancharikmitra/CCoT) |
| [TextCoT: Zoom In for Enhanced Multimodal Text-Rich Image Understanding](https://arxiv.org/abs/2404.09797) | Arxiv 2024 | Text-rich Images, Zoom-in Strategy | [GitHub](https://github.com/bzluan/TextCoT) |
| [Cantor: Inspiring Multimodal Chain-of-Thought of MLLM](https://arxiv.org/abs/2404.16033) | MM 2024 | CoT Inspiration, MLLM Reasoning | N/A |
| [KAM-CoT: Knowledge Augmented Multimodal Chain-of-Thoughts Reasoning](https://arxiv.org/abs/2401.12863) | AAAI 2024 | Knowledge Augmentation, CoT Reasoning | N/A |
| [Chameleon: Plug-and-Play Compositional Reasoning with Large Language Models](https://arxiv.org/abs/2304.09842) | NeurIPS 2023 | Compositional Reasoning, Tool Integration | [GitHub](https://github.com/lupantech/chameleon-llm) |
| [See, Think, Confirm: Interactive Prompting Between Vision and Language Models](https://arxiv.org/abs/2301.05226) | Arxiv 2023 | Interactive Prompting, Knowledge-based Reasoning | N/A |
| [Visual Chain of Thought: Bridging Logical Gaps with Multimodal Infillings](https://arxiv.org/abs/2305.02317) | Arxiv 2023 | Multimodal Infillings, Visual CoT | N/A |
| [Chain of Thought Prompt Tuning in Vision Language Models](https://arxiv.org/abs/2304.07919) | Arxiv 2023 | Prompt Tuning, VLM CoT | N/A |
| [Multimodal Chain-of-Thought Reasoning in Language Models](https://arxiv.org/abs/2302.00923) | Arxiv 2023 | Multimodal CoT, Two-stage Framework | [GitHub](https://github.com/amazon-science/mm-cot) |

⬆ [Back to Top](#contents)

---

### Agentic: Thinking with Images

*This category includes models that actively interact with images during inference using tools (zoom, crop, search, edit, sketch), enabling iterative visual exploration and dynamic focus on regions of interest. These methods reduce interference by isolating micro-crops but typically incur higher latency due to multi-pass inference.*

| Title | Venue & Year | Highlights/Keywords | Code |
| --- | --- | --- | --- |
| [S1-VL: Scientific Multimodal Reasoning Model with Thinking-with-Images](https://arxiv.org/abs/2604.21409v1) | Arxiv 2026 | Scientific Reasoning, Thinking-with-Images | N/A |
| [Test-time Scaling over Perception: Resolving the Grounding Paradox in Thinking with Images](https://arxiv.org/abs/2604.11025v1) | Arxiv 2026 | Test-time Scaling, Grounding Paradox | N/A |
| [Walk the Talk: Bridging the Reasoning-Action Gap for Thinking with Images via Multimodal Agentic Policy Optimization](https://arxiv.org/abs/2604.06777v1) | Arxiv 2026 | Agentic Policy Optimization, Reasoning-Action Gap | N/A |
| [Visual Planning: Let's Think Only with Images](https://github.com/yix8/VisualPlanning) | ICLR 2026 | Visual Planning, Image-only Reasoning | [GitHub](https://github.com/yix8/VisualPlanning) |
| [Let's Think with Images Efficiently! An Interleaved-Modal Chain-of-Thought Reasoning Framework with Dynamic and Precise Visual Thoughts](https://arxiv.org/abs/2603.21754v1) | AAAI 2026 | Interleaved-Modal CoT, Dynamic Visual Thoughts | [GitHub](https://github.com/67L1/DaP-ICoT) |
| [VR-Thinker: Boosting Video Reward Models through Thinking-with-Image Reasoning](https://arxiv.org/abs/2510.10518v4) | Arxiv 2025 | Video Reward Models, Thinking-with-Image | N/A |
| [DeepSketcher: Internalizing Visual Manipulation for Multimodal Reasoning](https://arxiv.org/abs/2509.25866v2) | Arxiv 2025 | Visual Manipulation, Sketching, Internalized | [GitHub](https://github.com/MiliLab/DeepSketcher) |
| [Thinking with Video: Video Generation as a Promising Multimodal Reasoning Paradigm](https://arxiv.org/abs/2511.04570v2) | Arxiv 2025 | Video Generation, Multimodal Reasoning Paradigm | N/A |
| [CodeDance: A Dynamic Tool-integrated MLLM for Executable Visual Reasoning](https://arxiv.org/abs/2512.17312v2) | Arxiv 2025 | Tool-integrated, Executable Visual Reasoning | N/A |
| [AGILE: Agentic Jigsaw Interaction Learning for Enhancing Visual Perception and Reasoning in VLMs](https://arxiv.org/abs/2510.01304) | ICLR 2026 | Agentic Interaction, Jigsaw Puzzle, Visual Perception | N/A |
| [DeepEyes: Incentivizing "Thinking with Images" in Vision-Language Models via Reinforcement Learning](https://arxiv.org/abs/2505.14362) | Arxiv 2025 | Reinforcement Learning, Zoom/Crop Tools, Long CoT | [GitHub](https://github.com/deepeyes) |
| [DeepEyesV2: Toward Agentic Multimodal Model](https://arxiv.org/abs/2511.05271) | Arxiv 2025 | Scaled Tool Learning, Visual Search | N/A |
| [Thyme: Thinking with Images for Visual Reasoning](https://arxiv.org/abs/2508.11630) | Arxiv 2025 | Pixel-space Operations, Code Generation | [GitHub](https://github.com/thyme) |
| [PixelReasoner: Incentivizing Pixel-Space Reasoning with Curiosity-Driven Reinforcement Learning](https://arxiv.org/abs/2505.15966) | Arxiv 2025 | Pixel-level Operations, Dynamic Visual Manipulation | N/A |
| [Mini-o3: Scaling Up Reasoning Patterns and Interaction Turns for Visual Search](https://arxiv.org/abs/2509.07969) | Arxiv 2025 | Visual Probing, Agentic Tools | N/A |
| [VLM-R3: Region Recognition, Reasoning, and Refinement for Enhanced Multimodal Chain-of-Thought](https://arxiv.org/abs/2505.16192) | Arxiv 2025 | Region Refinement, Recursive Focusing | N/A |
| [Argus: Vision-Centric Reasoning with Grounded Chain-of-Thought](https://arxiv.org/abs/2505.23766) | Arxiv 2025 | Visual CoT, Attention Grounding | N/A |
| [ReFocus: Visual Editing as a Chain of Thought for Structured Image Understanding](https://arxiv.org/abs/2501.05452) | Arxiv 2025 | Visual Editing, Structured Understanding | [GitHub](https://github.com/zeyofu/ReFocus_Code) |
| [Visual Sketchpad: Sketching as a Visual Chain of Thought for Multimodal Language Models](https://arxiv.org/abs/2406.09403) | Arxiv 2024 | Sketching, Visual Chain of Thought | [GitHub](https://github.com/Yushi-Hu/VisualSketchpad) |
| [Chain-of-Spot: Interactive Reasoning Improves Large Vision-Language Models](https://arxiv.org/abs/2403.12966) | CVPR 2024 | Interactive Spot Identification, Zoom-in Reasoning | [GitHub](https://github.com/chain-of-spot) |
| [V*: Guided Visual Search as a Core Mechanism in Multimodal LLMs](https://arxiv.org/abs/2312.14135) | CVPR 2024 | Visual Search, Search-based Perception | [GitHub](https://github.com/penghao-wu/vstar) |

⬆ [Back to Top](#contents)

---

### Training-Based Methods

*This category covers methods that improve fine-grained perception through training procedures, including supervised fine-tuning, knowledge distillation, and reinforcement learning.*

#### Supervised Fine-Tuning & Distillation

| Title | Venue & Year | Highlights/Keywords | Code |
| --- | --- | --- | --- |
| [LanteRn: Latent Visual Structured Reasoning](https://arxiv.org/abs/2603.25629v1) | Arxiv 2026 | Latent Visual Reasoning, Structured Reasoning | N/A |
| [TextHawk: Exploring Efficient Fine-Grained Perception of Multimodal Large Language Models](https://github.com/yuyq96/TextHawk) | Arxiv 2025 | Efficient Fine-Grained Perception, Text-rich | [GitHub](https://github.com/yuyq96/TextHawk) |
| [Traceable Evidence Enhanced Visual Grounded Reasoning: Evaluation and Methodology](https://arxiv.org/abs/2507.07999v2) | Arxiv 2025 | Traceable Evidence, Visual Grounded Reasoning | N/A |
| [SSR: Enhancing Depth Perception in Vision-Language Models via Spatial Sense and Reasoning](https://arxiv.org/abs/2505.12448) | ICLR 2026 | Depth Perception, Spatial Reasoning, Structured Rationales | [GitHub](https://github.com/yliu-cs/SSR) |
| [Zooming without Zooming: Region-to-Image Distillation for Fine-Grained Multimodal Perception](https://arxiv.org/abs/2504.xxxxx) | Arxiv 2025 | Region-to-Image Distillation, ZoomBench, Single-Pass Perception | [GitHub](https://github.com/inclusionAI/Zooming-without-Zooming) |
| [URSA: Understanding and Verifying Chain-of-thought Reasoning in Multimodal Mathematics](https://arxiv.org/abs/2501.04686v1) | Arxiv 2025 | Mathematical Reasoning, Verification | N/A |
| [Can We Generate Images with CoT? Let's Verify and Reinforce Image Generation Step by Step](https://arxiv.org/abs/2501.13926) | Arxiv 2025 | Image Generation CoT, Verification | N/A |
| [RedStar: Does Scaling Long-CoT Data Unlock Better Slow-Reasoning Systems?](https://arxiv.org/abs/2501.11284) | Arxiv 2025 | Long-CoT, Scaling | N/A |
| [Insight-V: Exploring Long-Chain Visual Reasoning with Multimodal Large Language Models](https://arxiv.org/abs/2411.14432) | Arxiv 2024 | Long-Chain Reasoning, Insightful Analysis | [GitHub](https://github.com/dongyh20/Insight-V) |
| [Perception Tokens Enhance Visual Reasoning in Multimodal Language Models](https://arxiv.org/abs/2412.03548) | Arxiv 2024 | Perception Tokens, Visual Reasoning | N/A |
| [Video-of-Thought: Step-by-Step Video Reasoning from Perception to Cognition](https://arxiv.org/abs/2501.03230) | ICML 2024 | Video Reasoning, Perception to Cognition | [GitHub](https://github.com/scofield7419/Video-of-Thought) |
| [AtomThink: A Slow Thinking Framework for Multimodal Mathematical Reasoning](https://arxiv.org/abs/2411.11930) | Arxiv 2024 | Slow Thinking, Mathematical Reasoning | N/A |

⬆ [Back to Top](#contents)

---

#### Reinforcement Learning

| Title | Venue & Year | Highlights/Keywords | Code |
| --- | --- | --- | --- |
| [VTool-R1: VLMs Learn to Think with Images via Reinforcement Learning on Multimodal Tool Use](https://arxiv.org/abs/2505.19255) | ICLR 2026 | Reinforcement Learning, Tool Use, Thinking-with-Images | [GitHub](https://github.com/VTool-R1/VTool-R1) |
| [Training Multi-Image Vision Agents via End2End Reinforcement Learning](https://arxiv.org/abs/2512.08980v3) | Arxiv 2025 | Multi-Image, End2End RL, Vision Agents | N/A |
| [Perception-Aware Policy Optimization for Multimodal Reasoning](https://arxiv.org/abs/2507.06448) | ICLR 2026 | PAPO, Perception-Aware RL, Implicit Perception Supervision | [GitHub](https://github.com/MikeWangWZHL/PAPO) |
| [Perception-R1: Advancing Multimodal Reasoning Capabilities of MLLMs via Visual Perception Reward](https://arxiv.org/abs/2506.07218) | ICLR 2026 | Visual Perception Reward, RLVR, GRPO | [GitHub](https://github.com/tongxiao2002/Perception-R1) |
| [Spotlight on Token Perception for Multimodal Reinforcement Learning](https://arxiv.org/abs/2510.09285) | ICLR 2026 | Token Perception, Visual Dependency, RLVR Optimization | N/A |
| [VisionReasoner: Unified Reasoning-Integrated Visual Perception via Reinforcement Learning](https://arxiv.org/abs/2505.12081) | ICLR 2026 | Unified Perception-Reasoning, RL, Multi-task | [GitHub](https://github.com/JIA-Lab-research/VisionReasoner) |
| [ViPER: Empowering the Self-Evolution of Visual Perception Abilities in Vision-Language Models](https://arxiv.org/abs/2510.24285) | ICLR 2026 | Self-Evolution, Fine-Grained Perception, RL | [GitHub](https://github.com/Icarus1216/ViPER) |
| [ViCrit: A Verifiable Reinforcement Learning Proxy Task for Visual Perception](https://arxiv.org/abs/2506.10128) | ICLR 2026 | Visual Hallucination Critic, RL Proxy Task, Fine-Grained Perception | N/A |
| [RAPID: Reasoning-Aligned Perception Decoupling for Scalable Multi-modal Large Language Models](https://arxiv.org/abs/2506.04559) | ICLR 2026 | Perception-Decoupling, Reasoning Alignment, Two-stage Pipeline | N/A |
| [R1-VL: Learning to Reason with Multimodal Large Language Models via Step-wise Group Relative Policy Optimization](https://arxiv.org/abs/2503.12937) | Arxiv 2025 | GRPO, Step-wise Reasoning | [GitHub](https://github.com/r1-vl) |
| [LlamaV-o1: Rethinking Step-by-Step Visual Reasoning in LLMs](https://arxiv.org/abs/2501.06186) | Arxiv 2025 | Visual Reasoning, O1-style | N/A |
| [Virgo: A Preliminary Exploration on Reproducing o1-like MLLM](https://arxiv.org/abs/2501.01904) | Arxiv 2025 | O1-like MLLM, Reasoning Exploration | [GitHub](https://github.com/Richar-Du/Virgo) |
| [VisualPRM: An Effective Process Reward Model for Multimodal Reasoning](https://arxiv.org/abs/2503.10291) | Arxiv 2025 | Process Reward Model | N/A |
| [MedVLM-R1: Incentivizing Medical Reasoning Capability of VLMs via Reinforcement Learning](https://arxiv.org/abs/2502.19634) | Arxiv 2025 | Medical Reasoning, RL | N/A |
| [MM-Eureka: Exploring Visual Aha Moment with Rule-based Large-scale Reinforcement Learning](https://arxiv.org/abs/2503.07365) | Arxiv 2025 | Visual Aha Moment, Rule-based RL | N/A |
| [VisualThinker-R1-Zero: R1-Zero's "Aha Moment" in Visual Reasoning on a 2B Non-SFT Model](https://arxiv.org/abs/2503.05132) | Arxiv 2025 | R1-Zero, Visual Reasoning | N/A |
| [R1-Omni: Explainable Omni-Multimodal Emotion Recognition with Reinforcement Learning](https://arxiv.org/abs/2503.05379) | Arxiv 2025 | Emotion Recognition, Explainable RL | N/A |
| [LMM-R1: Empowering 3B LMMs with Strong Reasoning Abilities Through Two-Stage Rule-Based RL](https://arxiv.org/abs/2503.07536) | Arxiv 2025 | Two-Stage RL, Rule-based | N/A |
| [Seg-Zero: Reasoning-Chain Guided Segmentation via Cognitive Reinforcement](https://arxiv.org/abs/2503.06520) | Arxiv 2025 | Segmentation, Cognitive Reinforcement | [GitHub](https://github.com/JIA-Lab-research/Seg-Zero) |
| [Boosting the Generalization and Reasoning of VLMs with Curriculum Reinforcement Learning](https://arxiv.org/abs/2503.07065) | Arxiv 2025 | Curriculum RL, Generalization | N/A |
| [OpenVLThinker: An Early Exploration to Complex Vision-Language Reasoning via Iterative Self-Improvement](https://arxiv.org/abs/2503.17352) | Arxiv 2025 | Self-Improvement, Iterative Training | [GitHub](https://github.com/uclanlp/OpenVLThinker) |
| [VisRL: Intention-Driven Visual Perception via Reinforced Reasoning](https://arxiv.org/abs/2503.07523) | Arxiv 2025 | Intention-Driven, Reinforced Reasoning | [GitHub](https://github.com/zhangquanchen/VisRL) |
| [Boosting Multimodal Reasoning with MCTS-Automated Structured Thinking](https://arxiv.org/abs/2502.02339) | Arxiv 2025 | MCTS, Structured Thinking | [GitHub](https://github.com/waltonfuture/RL-with-Cold-Start) |
| [R1-OneVision: Advancing Generalized Multimodal Reasoning through Cross-Modal Formalization](https://arxiv.org/abs/2503.10615) | Arxiv 2025 | Cross-Modal, Generalized Reasoning | N/A |
| [Mulberry: Empowering MLLM with O1-like Reasoning and Reflection via Collective Monte Carlo Tree Search](https://arxiv.org/abs/2412.18319) | Arxiv 2024 | MCTS, O1-like Reasoning | N/A |
| [Diving into Self-Evolving Training for Multimodal Reasoning](https://arxiv.org/abs/2412.17451) | Arxiv 2024 | Self-Evolving, RL Training | N/A |

⬆ [Back to Top](#contents)

---

### Applications & Domains

*This category covers application domains where fine-grained perception is critical.*

| Title | Venue & Year | Domain | Highlights/Keywords | Code |
| --- | --- | --- | --- | --- |
| [Q-DeepSight: Incentivizing Thinking with Images for Image Quality Assessment and Refinement](https://arxiv.org/abs/2604.16858v1) | Arxiv 2026 | Image Quality | Thinking-with-Images for IQA, Refinement | N/A |
| [Q-Probe: Scaling Image Quality Assessment to High Resolution via Context-Aware Agentic Probing](https://arxiv.org/abs/2601.15356v4) | Arxiv 2026 | Image Quality | Agentic Probing, High-Resolution IQA | N/A |
| [VLA-Thinker: Boosting Vision-Language-Action Models through Thinking-with-Image Reasoning](https://arxiv.org/abs/2603.14523v1) | Arxiv 2026 | Robotics | VLA, Thinking-with-Image, Action Models | N/A |
| [EmoOmni: Bridging Emotional Understanding and Expression in Omni-Modal LLMs](https://arxiv.org/abs/2602.21900v2) | Arxiv 2026 | Emotion | Omni-Modal, Emotional Understanding | N/A |
| [Grounding-IQA: Grounding Multimodal Language Model for Image Quality Assessment](https://arxiv.org/abs/2411.17237) | ICLR 2026 | Image Quality | Grounding-IQA, Multimodal Referring, Quality Assessment | [GitHub](https://github.com/zhengchen1999/Grounding-IQA) |
| [MedVLM-R1: Incentivizing Medical Reasoning Capability of VLMs via Reinforcement Learning](https://arxiv.org/abs/2502.19634) | Arxiv 2025 | Medical | Medical Reasoning, RL | N/A |
| [CoT-Drive: Efficient Motion Forecasting for Autonomous Driving with LLMs and Chain-of-Thought Prompting](https://arxiv.org/abs/2503.07234) | Arxiv 2025 | Autonomous Driving | Motion Forecasting, CoT | N/A |
| [MedCoT: Medical Chain of Thought via Hierarchical Expert](https://arxiv.org/abs/2412.13736) | Arxiv 2024 | Medical | Hierarchical Expert, Medical CoT | N/A |
| [Robotic Control via Embodied Chain-of-Thought Reasoning](https://arxiv.org/abs/2407.08693) | Arxiv 2024 | Robotics | Embodied CoT, Control | N/A |
| [Reason2Drive: Towards Interpretable and Chain-based Reasoning for Autonomous Driving](https://arxiv.org/abs/2312.03661) | ECCV 2024 | Autonomous Driving | Interpretable, Chain Reasoning | [GitHub](https://github.com/fudan-zvg/Reason2Drive) |
| [Dolphins: Multimodal Language Model for Driving](https://arxiv.org/abs/2312.00438) | ECCV 2024 | Autonomous Driving | Driving-specific, Multimodal | [GitHub](https://github.com/SaFo-Lab/Dolphins) |
| [DriveCoT: Integrating Chain-of-Thought Reasoning with End-to-End Driving](https://arxiv.org/abs/2403.16996) | Arxiv 2024 | Autonomous Driving | End-to-End Driving, CoT | N/A |
| [ManipLLM: Embodied Multimodal Large Language Model for Object-Centric Robotic Manipulation](https://arxiv.org/abs/2312.16217) | CVPR 2024 | Robotics | Object-centric, Manipulation | [GitHub](https://github.com/clorislili/ManipLLM) |

⬆ [Back to Top](#contents)

---


### Why We Do It
In an era where synthetic media is increasingly sophisticated and pervasive, our research serves as a critical line of defense. By advancing fine-grained perception technologies, we aim to:
*   **Enhance Visual Understanding:** Enable MLLMs to perceive fine-grained details without expensive inference-time operations.
*   **Bridge the Zooming Gap:** Internalize the benefits of "zooming in" during training for efficient single-pass perception.
*   **Industrial Application & Impact:** We provide robust, scalable perception solutions for Ant Group's diverse content platforms.


### ✉️ Contact Us

For questions or collaborations, please contact:
- Liangbo He: liangbo.hlb@antgroup.com
- Lai Wei: waltonfuture@sjtu.edu.cn
- Jun Lan: yelan.lj@antgroup.com
- Zhuosheng Zhang: zhangzs@sjtu.edu.cn

⬆ [Back to Top](#contents)

---

### Star History

<a href="https://www.star-history.com/?repos=ant-research%2FAwesome-Fine-Grained-Multimodal-Perception&type=date&logscale=&legend=top-left">
 <picture>
   <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/chart?repos=ant-research/Awesome-Fine-Grained-Multimodal-Perception&type=date&theme=dark&legend=top-left" />
   <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/chart?repos=ant-research/Awesome-Fine-Grained-Multimodal-Perception&type=date&legend=top-left" />
   <img alt="Star History Chart" src="https://api.star-history.com/chart?repos=ant-research/Awesome-Fine-Grained-Multimodal-Perception&type=date&legend=top-left" />
 </picture>
</a>

---
