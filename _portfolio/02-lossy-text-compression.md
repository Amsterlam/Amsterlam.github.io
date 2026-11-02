---
title: "Text-Preserving Lossy Text Compression with LLM Reconstruction"
excerpt: "Research · Supervised by Jun Li<br/>Strategic token deletion plus QLoRA-fine-tuned LLM reconstruction for semantic text compression."
collection: portfolio
---

**Supervisor:** Jun Li · **Related paper:** [AACL-IJCNLP 2026](/publication/2026-lossy-text-compression)

- Proposed a lossy semantic text compression framework combining token deletion and LLM-based reconstruction.
- Designed multiple deletion strategies (WordFreq, entropy-based, and hybrid methods) to optimize the compression–quality trade-off.
- Fine-tuned Llama-3.2-3B-Instruct using QLoRA for reconstruction, achieving competitive performance with Gemini 2.0 Flash.
- Evaluated reconstruction quality using BERTScore, CER, and ROUGE-L across multiple datasets, including BBC News and Chinese corpora.
- Conducted large-scale experiments under varying compression rates (10%–90%) to analyze robustness and generalization.
