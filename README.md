# **Preliminary Project Information**
**Student Name:** Fatimah Alali-g202423180

**Project title:** Graph-Guided Story Generation and Semantic Enrichment with Large Vision-Language Models

**Author names for refrence paper:** Fan Lu, Wei Wu, Kecheng Zheng, et al.

**Date:** September 25, 2024
## Problem Statement
The current paper ([Benchmarking Large Vision-Language Models via Directed Scene Graph for Comprehensive Image Captioning](https://openaccess.thecvf.com/content/CVPR2025/papers/Lu_Benchmarking_Large_Vision-Language_Models_via_Directed_Scene_Graph_for_Comprehensive_CVPR_2025_paper.pdf))
employs Large Vision-Language Models (LVLMs) that excel at generating comprehensive single-image captions. However, it lack in creation coherent, emotionally engaging multi-sentence stories that capture both visual details and narrative flow.
The benchmark for the paper achieved a good result in  scene graph annotations for evaluating comprehensive image captioning. 

**The gap found in the current benchmark are:**

1.Temporal Narrative Structure: Existing models generate static descriptions rather than progressive storytelling

2.Emotional Context Integration: Current approaches focus on visual accuracy but lack emotional depth and contextual richness

3.Multi-Sentence Coherence: No systematic framework exists for maintaining narrative consistency across multiple sentences

4.Structured Evaluation: Limited metrics for assessing story quality beyond traditional captioning measures

## Research Idea & Brief Overview

The main aim of this project is the extension of current paper framework by developing a novel approach for scene graph-conditioned story generation. The core innovation lies in transforming static visual scene graphs (objects, attributes, relations) into dynamic narrative structures enriched with emotional and contextual semantics.The expected Key Technical Contributions lies on these points:

**Turning Scene Graphs into Stories**

Using special network to read detailed scene descriptions, A temporal reasoning module helps plan how the story moves forward and  A story writer creates multiple connected sentences so the story feels smooth.

**Adding Emotions and Context**

Enriching scene descriptions with emotional details like mood and character feelings, reasoning system figures out the overall atmosphere of the story from the visuals and the system also tracks how characters change from one part of the story to the next.

**Better Ways to Judge Story Quality**

Measuring story accuracy using CompreCap’s object and relation scores, adding new ways to check story flow, emotions, and engagement.Also, include human reviews to see if people enjoy and understand the stories. 

**The expected methodolgy planned to follow** ddivided into 3 main steps. First is the foundation by reproducing the current paper framework (CompreCap), analyze scene graph structures. Second is the architecture development phase where the pipline of scene-graph-to-story generation designed and implmented. Third phase is developing emotional annotation schema and context inference. Lastly is the training & evaluation in which it will be multi-stage training with comprehensive assessment

**The Expected impacted inteded** to be achieved in terms of **technical**, **academic** and **practical** impact: 

-**Technical:** First systematic approach to story generation using structured visual scene graphs

-**Academic:** Novel evaluation framework for narrative generation from images

-**Practical:** Enhanced human-AI interaction through more engaging visual storytelling

**Resources & Datasets:**

-**Primary:** CompreCap dataset (560 images with detailed scene graphs)

-**Supplementary:** Visual Genome, COCO datasets for broader evaluation

-**Base Models:** LLaVA-Next-34B, InternVL-Chat-V1-5 as foundation architectures

**Potential challenges:**

-Dataset size limitations (560 images may be insufficient for training)

-Computational requirements for multi-modal training

-Human annotation costs for emotional enrichmen

**To summarize,** this project addresses a fundamental limitation in current vision-language models while building systematically on state-of-the-art benchmarking methodology, positioning it for both academic contribution and practical impact in AI-powered storytelling applications.

