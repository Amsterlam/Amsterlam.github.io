---
title: "CyberNeuro: A Privacy-Preserving Agentic Workbench for Cohort-Scale Neuroimage and Clinical Data Analysis"
collection: publications
category: preprints
permalink: /publication/2026-cyberneuro
excerpt: 'A multi-agent workbench that automates cohort-scale neuroimaging analysis while keeping patient data on-premise.'
date: 2026-07-01
venue: 'arXiv preprint arXiv:2607.28841'
paperurl: 'https://arxiv.org/abs/2607.28841'
citation: 'Ran Ren, <b>Junhong Tong</b>, Yunxi Kong, Yiyao Chen, Yucheng Li, Kunhao Zhou, Shaoqi Wang, Yuxiang Tao, Shuheng Cao, Zhihao Fan, Marissa DiPiero, Tingting Dan, Guorong Wu. &quot;CyberNeuro: A Privacy-Preserving Agentic Workbench for Cohort-Scale Neuroimage and Clinical Data Analysis.&quot; <i>arXiv preprint arXiv:2607.28841</i>, 2026.'
---

CyberNeuro investigates how LLM agents can automate cohort-scale neuroimaging analysis (metadata curation, pipeline execution, and quality control) while keeping patient data on-premise, for labs with limited staff and compute.

- A multi-agent framework (Planner, Validator, Dispatcher, Reporter) in which an LLM plans workflows over registered skills and validators gate every tool call.
- An execution layer integrating 58 neuroimaging and statistics skills (e.g., FreeSurfer, fMRIPrep, XCP-D) as version-pinned Apptainer containers on a Slurm cluster, with sandboxed multi-user workspaces.
- A human-in-the-loop co-visualization panel for quality control.
- With a locally hosted 7B model, held-out tool-use accuracy rises from 40.3% to 69.4%, and a 10-cohort workflow suite completes with ~10.6% of the per-volume tokens of the NeuroClaw baseline.
