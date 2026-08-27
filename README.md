<h1 align="center">Haffi Irfan</h1>

<p align="center">
  <a href="https://www.linkedin.com/in/haffi-irfan-b8a71021a/"><img src="https://img.shields.io/badge/-LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"/></a>
  <a href="mailto:haffiirfan@gmail.com"><img src="https://img.shields.io/badge/-Email-D14836?style=for-the-badge&logo=gmail&logoColor=white"/></a>
  <a href="https://haffiirfan.vercel.app/"><img src="https://img.shields.io/badge/-Portfolio-00C853?style=for-the-badge&logo=vercel&logoColor=white"/></a>
</p>

<p align="center">
Software engineer working at the intersection of generative AI and systems engineering. I build multi-model pipelines that actually run on hardware people can afford, and ship computer vision systems into production. First-author manuscript currently under peer review at a Springer Nature journal.
</p>

---

###  Research

**OrchestraGen: A Unified Memory-Orchestrated Multi-Model Pipeline for Text-to-Avatar Synthesis**
*Under peer review — Multimedia Systems (Springer Nature MMSJ)*

The paper introduces Dynamic Memory Orchestration (DMO), a scheduling strategy that fits 60.1 GB of heterogeneous model weights into 32 GB of dual-T4 VRAM without quantization or pruning. The pipeline chains six models (Mistral-7B → SDXL Base+Refiner → LivePortrait → Real-ESRGAN) to turn text prompts into animated portrait videos. Key results from the paper:

| Metric | Value |
|:--|:--|
| Memory scaling factor | 4.35× (60.1 GB on 13.8 GB peak per-GPU) |
| Latency reduction | 33.1% via GPU-CPU parallelism + dual-GPU frame splitting |
| CLIP alignment | 0.35 (+9.4% over raw prompts) |
| Identity preservation | ArcFace 0.915 across 40 frames |
| Super-resolution fidelity | PSNR 35.92 dB, SSIM 0.9734 |

---

###  Projects

<table>
<tr>
<td width="50%">

**[NeuroAnimate](https://github.com/haffiirfan/NeuroAnimate-Multimodal-Synthesis-for-3D-styled-imagery-hyper-realistic-Shorts)**

The engineering backbone behind OrchestraGen. Six AI models loaded and unloaded one at a time on Kaggle's free dual-T4 setup. The memory orchestrator keeps peak GPU usage at 13.8 GB by clearing each model before the next one loads. ESRGAN frames are split across both GPUs in parallel, which dropped the upscaling stage from 277s to 140s.

`PyTorch` `Diffusers` `ONNX Runtime` `CUDA` `Gradio`

</td>
<td width="50%">

**[SafetyIQ](https://github.com/haffiirfan/SafetyIQ-AI-Driven-Construction-Safety-Monitoring)**

Real-time construction site monitoring with object detection and natural language incident reports. Fine-tuned YOLO11s on 44,000 PPE images (0.75+ mAP), built a RAG pipeline using ChromaDB + Sentence Transformers + T5 for generating reports from detection events, and pushed detections over WebSocket at under 20ms per frame.

`YOLOv11` `FastAPI` `React` `PostgreSQL` `ChromaDB` `WebSocket`

</td>
</tr>
</table>

---

###  Education

**BSc Software Engineering** — Minhaj University Lahore (2022–2026)

Scored 4.0/4.0 in Artificial Intelligence, Data Structures & Algorithms, Object Oriented Programming, and Calculus. Final year project (NeuroAnimate) led directly to the Springer submission.

---

###  What I work with

**ML / CV / NLP**

![PyTorch](https://img.shields.io/badge/-PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![TensorFlow](https://img.shields.io/badge/-TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white)
![YOLO](https://img.shields.io/badge/-YOLOv8%2F11-111F68?style=flat-square&logo=ultralytics&logoColor=white)
![OpenCV](https://img.shields.io/badge/-OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/-scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white)
![Hugging Face](https://img.shields.io/badge/-Hugging%20Face-FFD21E?style=flat-square&logo=huggingface&logoColor=black)

**Languages & Data**

![Python](https://img.shields.io/badge/-Python-3776AB?style=flat-square&logo=python&logoColor=white)
![C++](https://img.shields.io/badge/-C%2FC%2B%2B-00599C?style=flat-square&logo=cplusplus&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/-PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![NumPy](https://img.shields.io/badge/-NumPy-013243?style=flat-square&logo=numpy&logoColor=white)
![pandas](https://img.shields.io/badge/-pandas-150458?style=flat-square&logo=pandas&logoColor=white)

**Backend & Deployment**

![FastAPI](https://img.shields.io/badge/-FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![React](https://img.shields.io/badge/-React-61DAFB?style=flat-square&logo=react&logoColor=black)
![Docker](https://img.shields.io/badge/-Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Git](https://img.shields.io/badge/-Git-F05032?style=flat-square&logo=git&logoColor=white)
![CUDA](https://img.shields.io/badge/-CUDA-76B900?style=flat-square&logo=nvidia&logoColor=white)

**RAG & Vector Search**

![ChromaDB](https://img.shields.io/badge/-ChromaDB-6E56CF?style=flat-square)
![Sentence Transformers](https://img.shields.io/badge/-Sentence--Transformers-FFCE00?style=flat-square)

---

###  Certifications
- **AI/ML Training Program** | NAVTTC (Corvit Networks), July 2025
- **Microsoft Azure AI Fundamentals (AI-900)** | May 2025
- **NeetCode Blind 75** | Completed Jan 2026

---

###  GitHub Stats

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=haffiirfan&show_icons=true&theme=github_dark&hide_border=true&count_private=true" height="165"/>
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=haffiirfan&layout=compact&theme=github_dark&hide_border=true" height="165"/>
</p>

---

### What I'm working towards

I want to be specialized in computer vision, specifically around efficient multi-model inference and generative AI on constrained hardware. The OrchestraGen work showed me that the real bottleneck in multimodal AI isn't model accuracy anymore; it's getting multiple large models to coexist on the same machine without everything falling apart. That's the problem I want to keep working on.

In parallel, I'm looking for AI/ML engineering roles where I can build production systems while continuing to publish.
