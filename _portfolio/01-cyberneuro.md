---
title: "CyberNeuro: Agentic Platform for Neuroimaging Analysis"
excerpt: "Research & engineering · UNC-Chapel Hill, Guorong Wu's group<br/>A multi-user web platform where an LLM agent plans, runs, and checks cohort-scale neuroimaging analysis on HPC while patient data stays on-premise."
collection: portfolio
---

**Group:** Prof. Guorong Wu, UNC-Chapel Hill · **Related paper:** [CyberNeuro (arXiv:2607.28841)](/publication/2026-cyberneuro)

CyberNeuro lets researchers describe a neuroimaging study in plain language and have an LLM agent plan, execute, and quality-check the analysis, without patient data leaving the lab's own infrastructure. I build and maintain the platform, which is based on the open-source OpenCode agent engine.

## Platform

- **Multi-user workspace**: a platform gateway and web app with per-user accounts, file browsing over SFTP, and a live terminal on a persistent, pinned-host SSH connection (passwords are never stored).
- **HPC execution**: an HPC provider connects each workspace to UNC's Longleaf cluster, so agents can submit, monitor, and collect Slurm jobs; tools run as version-pinned containers on the compute nodes.
- **Skill system**: 58 neuroimaging, statistics, and visualization skills (FreeSurfer, FSL, ANTs, MRtrix3, TractSeg, NiBabies, SPM-style pipelines, MRIQC-style QC, harmonization, and more), each packaged as an agent skill with its own instructions.
- **Visualization runtime**: a fail-closed visualization controller routes each output to the right viewer based on file type and intent: 3D cortical surfaces and stat maps (PyVista), diffusion glyphs and fibers (FURY), voxel QC (FSLeyes), manual mask editing (Freeview), atlas plots (ggseg), and connectivity graphs (Gephi).
- **One-image deployment**: the full stack, including the web UI, server, neuroimaging toolchains, and checksum-verified model weights, builds into a single immutable Docker image, so other labs can deploy it with Docker alone.

## Research

- Investigated how LLM agents can automate cohort-scale neuroimaging analysis (metadata curation, pipeline execution, quality control) for labs with limited staff and compute.
- Co-designed a multi-agent framework (Planner, Validator, Dispatcher, Reporter) where an LLM plans workflows over registered skills and validators gate every tool call.
- Built a human-in-the-loop co-visualization panel for quality control, enabling researchers to inspect volumes and edit masks to verify and correct agent outputs.
- With a locally hosted 7B model, raised held-out tool-use accuracy from 40.3% to 69.4% over the base model, and completed a 10-cohort workflow suite with ~10.6% of the per-volume tokens of the NeuroClaw baseline.
