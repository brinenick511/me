---
title: "Faster MoE LLM Inference for Extremely Large Models"
date: 2025-01-01
url: "papers/faster-moe-llm-inference/"
slug: "faster-moe-llm-inference"
weight: 2
summary: "Efficient MoE LLM inference for extremely large models."
description: "Under review 2025."
bibtex: "yang2025fastermoellminference"
hideMeta: true
showBibtex: true
---

![MoE demo figure](moedemo.png)

![v2l top-k figure](v2ltopk.png)

## Abstract

Sparse Mixture-of-Experts (MoE) LLMs are becoming a mainstream choice for ultra-large models. This paper studies fine-grained MoE inference efficiency under different service loads, with a focus on the trade-off between speed and quality when reducing routed experts. The results show clear optimization opportunities for deployment: reducing the number of *activated* experts can bring significant speed gains with limited quality loss in many settings, while reducing the *total* experts often hurts quality more severely. The method reported in the paper improves throughput by at least 10% without performance degradation.
