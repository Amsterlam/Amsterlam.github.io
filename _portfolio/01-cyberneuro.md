---
title: "Privacy-Preserving Agentic Workbench for Neuroimaging Analysis"
excerpt: "Research · Supervised by Guorong Wu<br/>A multi-agent LLM framework that automates cohort-scale neuroimaging analysis while keeping patient data on-premise."
collection: portfolio
---

**Supervisor:** Guorong Wu · **Related paper:** [CyberNeuro (arXiv:2607.28841)](/publication/2026-cyberneuro)

- Investigated how LLM agents can automate cohort-scale neuroimaging analysis (metadata curation, pipeline execution, quality control) while keeping patient data on-premise for labs with limited staff and compute.
- Co-designed a multi-agent framework (Planner, Validator, Dispatcher, Reporter) where an LLM plans workflows over registered skills and validators gate every tool call.
- Developed the execution layer, integrating 58 neuroimaging and statistics skills (e.g., FreeSurfer, fMRIPrep, XCP-D) as version-pinned Apptainer containers on a Slurm cluster, with sandboxed multi-user workspaces.
- Built a human-in-the-loop co-visualization panel for quality control, enabling researchers to inspect volumes and edit masks to verify and correct agent outputs.
- With a locally hosted 7B model, raised held-out tool-use accuracy from 40.3% to 69.4% over the base model, and completed a 10-cohort workflow suite with ~10.6% of the per-volume tokens of the NeuroClaw baseline.
