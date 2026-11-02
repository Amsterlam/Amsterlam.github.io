---
title: "Text-Preserving Lossy Text Compression: A Study of Strategic Deletion and LLM Reconstruction"
collection: publications
category: conferences
permalink: /publication/2026-lossy-text-compression
excerpt: 'A lossy semantic text compression framework that strategically deletes tokens and reconstructs the text with a fine-tuned LLM.'
date: 2026-10-01
venue: 'AACL-IJCNLP 2026'
citation: 'Yuchun Zou, <b>Junhong Tong</b>, Jun Li. &quot;Text-Preserving Lossy Text Compression: A Study of Strategic Deletion and LLM Reconstruction.&quot; <i>AACL-IJCNLP 2026</i>.'
---

We propose a lossy semantic text compression framework that combines token deletion with LLM-based reconstruction.

- Designed multiple deletion strategies (word-frequency, entropy-based, and hybrid) to optimize the compression–quality trade-off.
- Fine-tuned Llama-3.2-3B-Instruct with QLoRA for reconstruction, achieving performance competitive with Gemini 2.0 Flash.
- Evaluated reconstruction quality with BERTScore, CER, and ROUGE-L across datasets including BBC News and Chinese corpora, under compression rates from 10% to 90%.
