---
title: "XQuant: Achieving Ultra-Low Bit KV Cache Quantization with Cross-Layer Compression"
date: 2025-01-02
url: "publications/xquant/"
aliases:
  - "/papers/xquant/"
slug: "xquant"
weight: 1
summary: "Ultra-low bit KV cache quantization with cross-layer compression."
publication: "EMNLP Main"
description: "EMNLP Main."
bibtex: "yang2025xquant"
hideMeta: true
showBibtex: true
---

<img src="workflow_final.png" width="1145" height="303" loading="lazy" decoding="async" alt="XQuant workflow figure">

<img class="paper-figure-medium" src="quantization-schemes.png" width="1008" height="1318" loading="lazy" decoding="async" alt="Three quantization schemes: standard, relaxed-constraint, and calibrated">

## Abstract

Large language models require substantial memory during generation because KV cache grows with context length. XQuant is a training-free, plug-and-play framework for KV cache quantization that combines (1) a computationally light data-free calibration method and (2) cross-layer KV cache compression. The method reaches sub-1.4-bit equivalent quantization and reports stronger trade-offs than prior methods such as KIVI-2bit and AsymKV-1.5bit on TruthfulQA and LongBench.
