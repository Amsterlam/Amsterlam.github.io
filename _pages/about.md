---
permalink: /
title: "About Me"
author_profile: true
classes: home
redirect_from: 
  - /about/
  - /about.html
---

<section class="hero">
  <p class="hero__eyebrow">Research Assistant · UNC-Chapel Hill</p>
  <p class="hero__lead">I'm <strong>Junhong Tong</strong>, a Research Assistant at the <strong>University of North Carolina at Chapel Hill</strong>, working with Prof. Guorong Wu. I study <strong>neuroimaging</strong>, <strong>LLM agents</strong>, and <strong>coding theory</strong>, building systems that are useful, verifiable, and private by design.</p>
  <div class="hero__actions">
    <a class="pill" href="/publications/">View publications</a>
    <a class="pill pill--secondary" href="/cv/">Curriculum vitae</a>
    <a class="chevron-link" href="mailto:junhong.tong16@qmail.cuny.edu">Get in touch</a>
  </div>
</section>

## Research focus

<div class="tiles">
  <div class="tile">
    <span class="tile__icon icon--blue"><i class="fa-solid fa-robot" aria-hidden="true"></i></span>
    <h3 class="tile__title">Agents for scientific workflows</h3>
    <p class="tile__body">Privacy-preserving, multi-agent systems that automate cohort-scale neuroimaging analysis while keeping patient data on-premise.</p>
    <a class="chevron-link" href="/portfolio/01-cyberneuro/">Learn more</a>
  </div>
  <div class="tile">
    <span class="tile__icon icon--purple"><i class="fa-solid fa-wave-square" aria-hidden="true"></i></span>
    <h3 class="tile__title">LLMs meet information theory</h3>
    <p class="tile__body">Lossy text compression with LLM reconstruction, and when language models can help error-correcting codes for text.</p>
    <a class="chevron-link" href="/portfolio/02-lossy-text-compression/">Learn more</a>
  </div>
  <div class="tile">
    <span class="tile__icon icon--orange"><i class="fa-solid fa-network-wired" aria-hidden="true"></i></span>
    <h3 class="tile__title">Robust distributed learning</h3>
    <p class="tile__body">Coding-theoretic defenses against Byzantine attackers and stragglers in distributed training.</p>
    <a class="chevron-link" href="/portfolio/03-secure-gradient-coding/">Learn more</a>
  </div>
</div>

## Building CyberNeuro

Neuroimaging analysis has a high barrier to entry: the toolchains are complex, the environments are hard to install, and researchers have to write cluster job scripts. At UNC ACMLab I build **CyberNeuro**, an AI agent platform that lets researchers run these analyses in natural language through its assistant, Wanda.

<div class="steps">
  <div class="step">
    <span class="step__num">1</span>
    <h3 class="step__title">Ask</h3>
    <p class="step__body">Describe the analysis you need in natural language.</p>
  </div>
  <div class="step">
    <span class="step__num">2</span>
    <h3 class="step__title">Pick a Skill</h3>
    <p class="step__body">The agent selects the matching Skill: an instruction document plus an Apptainer SIF container image.</p>
  </div>
  <div class="step">
    <span class="step__num">3</span>
    <h3 class="step__title">Run on the cluster</h3>
    <p class="step__body">The agent writes a Slurm job and submits it to the cluster's CPU/GPU nodes.</p>
  </div>
  <div class="step">
    <span class="step__num">4</span>
    <h3 class="step__title">Review</h3>
    <p class="step__body">Results become interactive pages that open in the visualization panel.</p>
  </div>
</div>

- **Web app**: built with SolidJS, with a chat interface, a file browser, and a visualization panel. Skills show up as pills in the input box and can also be chosen by hand.
- **58 Skills**: structural preprocessing, DICOM-to-BIDS conversion, structural MRI quality control, white-matter normative scoring, DTI and tractography, functional connectivity, and statistics and paper figures.
- **Visualization routing**: the agent sends each output to the right tool by file type. NIfTI volumes open in a slice viewer, FreeSurfer surfaces in PyVista 3D, fiber tracts in FURY/TrackVis, and connectivity matrices as network graphs.
- **Example: 5-step structural MRI QC**. From raw images through skull stripping, registration, and tissue segmentation to cortical surfaces, each step produces a review page. Researchers mark every subject pass or fail and can fix brain masks by hand in the browser; once the decisions are exported, the agent repairs or reruns the failed cases.

<div class="hero__actions">
  <a class="pill" href="https://wanda-landing-page-orcin.vercel.app/">Watch the demo</a>
  <a class="chevron-link" href="https://arxiv.org/abs/2607.28841">Read the paper</a>
  <a class="chevron-link" href="/portfolio/01-cyberneuro/">Project details</a>
</div>

## News

<ul class="news">
  <li><span class="news__date">2026</span><span>Our paper <em>Text-Preserving Lossy Text Compression: A Study of Strategic Deletion and LLM Reconstruction</em> is accepted to <strong>AACL-IJCNLP 2026</strong>.</span></li>
  <li><span class="news__date">2026</span><span><em>CyberNeuro</em>, a privacy-preserving agentic workbench for neuroimage and clinical data analysis, is released on <a href="https://arxiv.org/abs/2607.28841">arXiv</a>.</span></li>
  <li><span class="news__date">2026</span><span><em>NeuroPilot</em> is accepted to the <strong>NeurIPS 2026</strong> Workshop on World Models for High-Stakes Health (WMHS).</span></li>
</ul>

## Research interests

<ul class="tags">
  <li>Healthcare</li>
  <li>Machine Learning</li>
  <li>Neuroimaging</li>
  <li>Coding Theory</li>
  <li>Natural Language Processing</li>
  <li>LLM</li>
</ul>
