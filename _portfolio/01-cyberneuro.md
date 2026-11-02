---
title: "CyberNeuro: AI Agent Platform for Neuroimaging Research"
excerpt: "Research & engineering · UNC ACMLab, Guorong Wu's group<br/>An AI agent platform that lets researchers run neuroimaging analyses in natural language, from Skill selection to Slurm jobs to interactive review."
collection: portfolio
---

**Lab:** UNC ACMLab, Prof. Guorong Wu · **Demo:** [CyberNeuro website](https://wanda-landing-page-orcin.vercel.app/) · **Related paper:** [CyberNeuro (arXiv:2607.28841)](/publication/2026-cyberneuro)

Neuroimaging analysis has a high barrier to entry: the toolchains are complex, the environments are hard to install, and researchers have to write cluster job scripts. We built a platform that lets researchers run these analyses in natural language through its assistant, Wanda.

<a class="pill" href="https://wanda-landing-page-orcin.vercel.app/">Watch the demo</a>

## How it works

A researcher describes what they need in natural language → the agent selects the matching Skill, where each Skill is an instruction document plus a container image (Apptainer SIF) → the agent generates a Slurm job and submits it to the cluster's CPU/GPU nodes → the results are rendered as interactive pages that open in the visualization panel for review.

## Platform

- **Frontend**: a SolidJS web app with a chat interface, a file browser, and a visualization panel. Skills appear as pills in the input box and can also be selected manually.
- **Skill coverage**: 58 Skills spanning structural preprocessing, DICOM-to-BIDS conversion, structural MRI quality control, white-matter normative scoring, DTI and tractography, functional connectivity, and statistics and paper figures.
- **Visualization**: the agent routes each output to a tool by file type. NIfTI volumes go to a slice viewer, FreeSurfer surfaces to PyVista 3D, fiber tracts to FURY/TrackVis, and connectivity matrices to network graphs.

## Case study: 5-step structural MRI QC

From raw images through skull stripping, registration, and tissue segmentation to cortical surfaces, every step produces a review page. Researchers mark each subject as pass or fail, one by one, and can fix the brain mask by hand right in the browser. Once the decisions are exported, the agent goes on to repair or rerun the failed cases.
