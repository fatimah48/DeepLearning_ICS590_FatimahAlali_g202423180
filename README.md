# **Preliminary Project Information**
**Student Name:** Fatimah Alali - g202423180

**Project title:** Graph-Guided Story Generation and Semantic Enrichment with Large Vision-Language Models

**Author names for reference paper:** Fan Lu, Wei Wu, Kecheng Zheng, et al.

## Problem Statement

The current paper ([Benchmarking Large Vision-Language Models via Directed Scene Graph for Comprehensive Image Captioning](https://openaccess.thecvf.com/content/CVPR2025/papers/Lu_Benchmarking_Large_Vision-Language_Models_via_Directed_Scene_Graph_for_Comprehensive_CVPR_2025_paper.pdf)) employs Large Vision-Language Models (LVLMs) that excel at generating comprehensive single-image captions. However, it lacks in creation of coherent, emotionally engaging multi-sentence stories that capture both visual details and narrative flow.

The benchmark for the paper achieved good results in scene graph annotations for evaluating comprehensive image captioning.

**The gaps found in the current benchmark are:**

1. **Temporal Narrative Structure:** Existing models generate static descriptions rather than progressive storytelling

2. **Emotional Context Integration:** Current approaches focus on visual accuracy but lack emotional depth and contextual richness

3. **Multi-Sentence Coherence:** No systematic framework exists for maintaining narrative consistency across multiple sentences

4. **Structured Evaluation:** Limited metrics for assessing story quality beyond traditional captioning measures

5. **Scene Graph Utilization:** Scene graphs used only for evaluation, not as generative input to model architectures

---

## Research Idea & Brief Overview

The main aim of this project is the extension of current paper framework by developing a novel deep learning approach for scene graph-conditioned story generation. The core innovation lies in transforming static visual scene graphs (objects, attributes, relations) into dynamic narrative structures through **learned multimodal representations**.

**Key Technical Contributions:**

**1. Graph Neural Network Scene Encoder**
- Using Graph Attention Network (GAT) to encode scene graph structure
- Learning object relationships through trainable attention mechanisms
- Generating 128D graph embeddings capturing structural information

**2. Cross-Modal Fusion Module** 
- Fusing visual features (BLIP) with graph-structured information (GNN)
- Implementing trainable gating mechanism for adaptive fusion
- Producing 256D multimodal representations

**3. Feature Projection for LLM Conditioning** 
- Mapping fused embeddings into LLM embedding space (4096D)
- Enabling soft prompting with continuous learned features
- Conditioning Mistral-7B on visual-graph representations

**4. Comprehensive Evaluation Framework**
- Measuring story accuracy using CompreCap's object and relation scores
- Adding narrative quality metrics (BLEU, BERTScore, coherence)
- Implementing graph consistency checking (novel metric)


**The expected methodology planned to follow** is divided into 3 main phases:

**Phase 1: Foundation**
- Reproduce current paper framework (CompreCap)
- Analyze scene graph structures
- Load and process dataset (50 samples)

**Phase 2: Architecture Development**
- Design and implement GNN encoder for scene graphs
- Develop cross-modal fusion module
- Create feature projection layer for LLM conditioning
- Establish end-to-end differentiable pipeline

**Phase 3: Generation & Evaluation**
- Generate stories using learned multimodal conditioning
- Conduct ablation studies to prove component contributions
- Evaluate with both factual and narrative quality metrics
- Compare against baseline models

**The Expected impact intended** to be achieved in terms of **technical**, **academic** and **practical** impact:

-**Technical:** First systematic approach to story generation using GNN-encoded visual scene graphs with learned multimodal fusion

-**Academic:** Novel evaluation framework for narrative generation from structured visual representations; extends CompreCap from evaluation-only to generative framework

-**Practical:** Enhanced human-AI interaction through more engaging visual storytelling; applications in accessibility, education, and creative tools

**Resources & Datasets:**

-**Primary:** CompreCap dataset (50 images subset for proof-of-concept; 40 train / 10 test split)

-**Supplementary:** Visual Genome, COCO datasets for broader evaluation (future work)

-**Base Models:** BLIP (vision encoder), Mistral-7B-Instruct-v0.2 (language generation)

-**Framework:** PyTorch, PyTorch Geometric, Hugging Face Transformers


**Challenges Encountered & Solutions:**
-Dataset size limitations (560 images): Use 50-sample subset for proof-of-concept

-Computational requirements for training:Implemented inference pipeline with frozen base models

-CPU-only environment | Optimized inference with batched generation

-Story quality without fine-tuning | Leveraged strong pre-trained LLM (Mistral-7B)

**To summarize,** this project addresses a fundamental limitation in current vision-language models while building systematically on state-of-the-art benchmarking methodology. By implementing three novel deep learning components (GNN encoder, cross-modal fusion, and feature projection), it will demonstrate a principled approach to scene-graph-conditioned narrative generation, positioning it for both academic contribution and practical impact in AI-powered storytelling applications.
