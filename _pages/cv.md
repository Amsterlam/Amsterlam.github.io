---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

<a class="pill" href="{{ base_path }}/files/cv.pdf">Download PDF</a>

Education
======
* **M.S. in Computer Science**, Queens College, City University of New York (CUNY), USA — 2026
* **B.Eng. in Electronic Engineering**, South China Agricultural University  
  China — 09/2019 – 06/2023

Experience
======
* **Research Assistant**, University of North Carolina at Chapel Hill — present
  * ACM Lab ([acmlab.unc.edu](https://acmlab.unc.edu/))

Research Interests
======
Healthcare, Machine Learning, Neuroimaging, Coding Theory, Natural Language Processing, LLM.

Publications
======
  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>

Research Experience
======
* **CyberNeuro: AI Agent Platform for Neuroimaging Research (UNC ACMLab)** — supervised by Guorong Wu · [Demo](https://wanda-landing-page-orcin.vercel.app/)
  * Built an AI agent platform whose assistant, Wanda, lets researchers run neuroimaging analyses in natural language, without installing complex toolchains or writing cluster job scripts.
  * The agent maps each request to one of 58 Skills (an instruction document plus an Apptainer SIF image) covering structural preprocessing, DICOM-to-BIDS, structural MRI QC, white-matter normative scoring, DTI/tractography, functional connectivity, and statistics and paper figures, then generates and submits Slurm jobs to CPU/GPU nodes.
  * SolidJS web app with chat, file browser, and visualization panel; Skills appear as pills in the input box. Outputs are routed by file type: NIfTI to a slice viewer, FreeSurfer surfaces to PyVista 3D, fiber tracts to FURY/TrackVis, connectivity matrices to network graphs.
  * 5-step structural MRI QC workflow (raw image, skull stripping, registration, tissue segmentation, cortical surface) with per-subject pass/fail review pages and in-browser brain-mask editing; exported decisions drive the agent's repair or rerun.
  * Co-designed a multi-agent framework (Planner, Validator, Dispatcher, Reporter); with a locally hosted 7B model, raised held-out tool-use accuracy from 40.3% to 69.4%, using ~10.6% of the per-volume tokens of the NeuroClaw baseline.
* **Text-Preserving Lossy Text Compression** — supervised by Jun Li
  * Token-deletion strategies (WordFreq, entropy-based, hybrid) with QLoRA-fine-tuned Llama-3.2-3B reconstruction, competitive with Gemini 2.0 Flash.

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
