---
title: "Can Language Models Help Error-Correcting Codes for Text, and When?"
collection: publications
category: preprints
permalink: /publication/2026-llm-error-correcting-codes
excerpt: 'Under one equal byte budget and a shared noisy channel, we compare eleven ways to combine language models with error-correcting codes for text. LMs help by compressing the text and repairing what the code misses, not by choosing which tokens to protect.'
date: 2026-10-15
venue: 'Under review at ACL Rolling Review (ARR), October 2026'
citation: '<b>Junhong Tong</b>, Yuchun Zou, Jun Li. &quot;Can Language Models Help Error-Correcting Codes for Text, and When?&quot; Under review at ACL Rolling Review (ARR), October 2026.'
---

Language models estimate how likely each part of a text is, so they might help error-correcting codes for text in three ways: by **deciding where redundancy is needed**, by **compressing the text**, or by **repairing what the code fails to correct**. These ideas are easy to get wrong, because the extra data they need, such as summaries or the positions of protected tokens, must share the byte budget and the noisy channel with the text, which can cancel the gains they promise.

## Approach

- **Equal-budget, same-channel protocol.** Every transmitted byte (payload, headers, summaries, and parity) counts toward a single budget and passes through the same byte-level channel, with substitution, erasure, and hybrid errors.
- **Eleven schemes on English news.** Byte-level schemes split the budget between Reed–Solomon parity and an LLM-written summary; token-level schemes pack the article into fixed-width tokenizer IDs and protect them either uniformly or according to how hard each token is for an LM to predict.
- **Two evaluation layers.** Every scheme shares one failure path into zero-shot LLM repair, and we score the text both before repair (coding layer) and after it (LLM layer).

## Findings

- **Packing gives the strongest code.** Packing text into token IDs halves the payload and frees the budget for parity: before repair, character error rate falls to 0.031 against 0.113 for byte-level Reed–Solomon, and 90.4% of packets are recovered exactly against 35.5%.
- **LLM repair fixes bytes, not tokens.** Repair restores visibly garbled bytes from context (byte-level CER 0.113 → 0.029) but cannot detect a well-formed wrong token, so once heavy substitution overwhelms the token-ID code, byte-level coding with repair wins.
- **Selective protection does not pay.** Protecting only the tokens an LM finds hard to predict never beats uniform protection: unprotected tokens cannot be re-derived reliably from damaged context, and protected tokens cost their bytes twice.
- **Summaries help only when verified.** A summary pays off only when it carries its own code and arrives intact, giving the lowest error after repair (CER 0.024).
- **Metrics matter.** Character error rate can declare a tie where word-level metrics and exact recovery show a clear winner, because repair leaves many words slightly wrong.

**Takeaway:** send text as packed token IDs while errors stay within the token-level code's capacity, and as bytes with a protected summary beyond it.
