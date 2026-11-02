---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

Education
======
* **M.S. in Computer Science**, Queens College, City University of New York (CUNY), USA — expected 06/2026
* **B.Eng. in Electronic Engineering**, South China Agricultural University, Zhujiang College, China — 09/2019 – 06/2023

Research Interests
======
LLM Agents, Coding Theory, Machine Learning, Healthcare, Neuroimaging, Natural Language Processing, Distributed Computing, Large Language Models, Computer Vision, Trustworthy AI.

Publications
======
  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>

Research Experience
======
* **Privacy-Preserving Agentic Workbench for Neuroimaging Analysis** — supervised by Guorong Wu
  * Co-designed a multi-agent LLM framework (Planner, Validator, Dispatcher, Reporter) for cohort-scale neuroimaging analysis with on-premise patient data.
  * Built the execution layer: 58 neuroimaging/statistics skills as version-pinned Apptainer containers on Slurm, with sandboxed multi-user workspaces.
  * Raised held-out tool-use accuracy of a local 7B model from 40.3% to 69.4%; ~10.6% of the per-volume tokens of the NeuroClaw baseline.
* **Text-Preserving Lossy Text Compression** — supervised by Jun Li
  * Token-deletion strategies (WordFreq, entropy-based, hybrid) with QLoRA-fine-tuned Llama-3.2-3B reconstruction, competitive with Gemini 2.0 Flash.
* **Secure Gradient Coding for Distributed Training** — supervised by Jun Li
  * Byzantine-resilient, straggler-tolerant training via Fractional Repetition Codes and a custom robust decoding algorithm.
* **Image-based Predictive Modeling for Drug Evaluation** — supervised by Lihua Cai
  * YOLOv8n-seg organoid segmentation (89% sensitivity) and LightGBM viability prediction (mean R² 0.633).
* **AI Agent Literature Survey** — supervised by Lihua Cai
  * Synthesized 200+ papers into a framework covering autonomy, human alignment, and multi-agent collaboration.

See [Research & Projects](/portfolio/) for details.

Projects
======
* **Cloud Computing** (03/2025 – 04/2025): multi-AZ AWS + Kubernetes with zero-downtime rolling updates; Hadoop/Spark analytics; Redis Cluster benchmarking.
* **Automobile Anti-collision Warning System** (03/2023 – 06/2023): 8-bit MCU firmware, ultrasonic/infrared sensor fusion, tiered warnings, UART telemetry.

Technical Skills
======
* **Languages & Frameworks:** Python, TypeScript, C, Bash, Bun, SolidJS, Hono
* **ML & LLM:** LLM Agents, QLoRA Fine-tuning, YOLOv8, LightGBM
* **Infrastructure:** Docker, Kubernetes, Slurm, Apptainer, AWS, Hadoop, Spark, Redis, GitHub Actions
* **Neuroimaging:** FreeSurfer, fMRIPrep, XCP-D, BIDS

Awards
======
* Outstanding Student Leader Scholarship (09/2021)
* "Outstanding Officer" Award, Student Association (06/2020)
* "Excellent Volunteer" Award, national-level cheerleading competition (12/2019)
