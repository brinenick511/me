---
title: "ROCOB: Dual-Manifold Alignment with Optimal Budgeting for Training-Free PTQ Recovery"
authors: "Haoqi Yang and Teng Xiao and Zuchao Li and Hao Huang and Lefei Zhang and Hai Zhao"
publication: "AACL-IJCNLP Oral"
publicationYear: "2026"
date: 2026-11-01
url: "publications/rocob/"
aliases:
  - "/papers/rocob/"
slug: "rocob"
weight: 0
summary: "Training-free PTQ recovery via dual-manifold alignment and rank budgeting."
description: "AACL-IJCNLP Oral."
bibtex: "yang2026rocob"
hideMeta: true
showBibtex: true
---

<img class="paper-figure-full" src="framework.png" width="5120" height="2880" loading="lazy" decoding="async" alt="ROCOB framework overview">

## Abstract

Post-training quantization facilitates efficient LLM deployment, yet it disproportionately erodes reasoning and mathematical performance. To recover fidelity without costly fine-tuning, we identify a critical vulnerability in existing output-space methods: the tendency to overfit the limited calibration manifold, which necessitates structural regularization for unseen data. We propose **ROCOB** (**R**esilient **O**utput **C**ompensation with **O**ptimal **B**udgeting), a training-free framework based on *Dual-Manifold Alignment*. ROCOB couples a Principal Activation Component (PAC), which minimizes error on the calibration manifold, with an Orthogonal Geometric Component (OGC), which recovers residual weight-space structure without fitting a second calibration objective. To compare methods fairly under the same added-parameter budget, ROCOB uses Global Spectral Energy Maximization (GSEM) to allocate ranks according to recovered spectral energy and module cost. Across Qwen3 and Llama-3 models, quantizers, and reasoning benchmarks, ROCOB improves average post-quantization recovery in most evaluated model–quantizer settings while preserving a training-free construction pipeline.

<img class="paper-figure-result" src="rocob-results.png" width="1250" height="1426" loading="lazy" decoding="async" alt="ROCOB results across Qwen3 models and quantizers">
