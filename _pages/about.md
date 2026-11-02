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
  <h1 class="hero__title">Trustworthy LLM agents <br>for science and health.</h1>
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

At UNC-Chapel Hill I build **CyberNeuro**, a web platform where researchers describe a neuroimaging study in plain language and an LLM agent plans, runs, and checks the analysis, while patient data stays on the lab's own infrastructure. Built on the open-source OpenCode agent engine, it brings together:

- **Multi-user workspace**: a platform gateway and web app with per-user accounts, file browsing, and a live terminal over a persistent SSH connection.
- **HPC execution**: agents submit and monitor Slurm jobs on UNC's Longleaf cluster over SSH/SFTP, with tools packaged as version-pinned containers.
- **58 neuroimaging skills**: FreeSurfer, FSL, ANTs, MRtrix3, TractSeg, NiBabies, SPM-style pipelines, quality control, and statistics, each packaged as an agent skill.
- **Interactive visualization**: a visualization runtime routes every result to the right viewer, from 3D cortical surfaces (PyVista) and diffusion glyphs (FURY) to voxel QC (FSLeyes) and manual mask editing (Freeview).
- **One-image deployment**: the whole stack ships as a single Docker image with pinned toolchains and checksum-verified model weights, so other labs can run it too.

<a class="chevron-link" href="https://arxiv.org/abs/2607.28841">Read the paper</a>&nbsp;&nbsp;&nbsp;<a class="chevron-link" href="/portfolio/01-cyberneuro/">Project details</a>

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
