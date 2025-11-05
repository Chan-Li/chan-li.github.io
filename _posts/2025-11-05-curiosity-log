---
layout: single
title: "🧭 Chan’s Curiosity Log — November 5, 2025"
date: 2025-11-05
categories: [theory, machine-learning, neuroscience, physics]
tags: [hopfield-network, redundancy, information-theory, spiking-networks, spatial-learning, curiosity-log]
permalink: /blog/2025-11-05-curiosity-log/
---

*Daily reflections on new papers, theories, and open questions.*

---

## 🧩 Paper 1 (Worth Reading in Detail): *Redundancy Maximization as a Principle of Associative Memory Learning*  
📄 [arXiv:2511.02584 (2025)](https://arxiv.org/pdf/2511.02584)

### 1.1 Background  
The **Hopfield model** provides a classical framework for **associative memory**, where stored patterns can be retrieved through attractor dynamics.  
Recent continuous-valued extensions of Hopfield networks have re-emerged in modern **machine learning**, and notably, the **Hopfield model is equivalent to Transformers**.  

While traditional analyses rely on correlation-based measures, **mutual information** and **Partial Information Decomposition (PID)** offer a more general, nonlinear way to quantify **multivariate dependencies** between variables, distinguishing between redundancy, synergy, and unique contributions.

### 1.2 Questions  
Is there a **unifying principle** that governs how associative memories form?  
If such a principle exists, can it be **directly optimized** to improve performance, rather than engineered through new learning rules?

### 1.3 Key Idea  
The authors analyze **Hopfield networks** from an **information-processing perspective**, applying **PID** to describe how each neuron integrates information from its external inputs and recurrent connections.  
They then construct **local goal functions** that explicitly optimize for **redundancy** (and other PID components) during learning.

### 1.4 Key Conclusions & Results  
- Below the **memory capacity**, a neuron’s activity exhibits **high redundancy** between external inputs and recurrent inputs, while **synergy** and **unique information** remain near zero.  
- Once the memory capacity is exceeded, redundancy collapses and performance declines sharply.  
- By using **redundancy** as a direct learning objective, the authors boost the **memory capacity** to **1.59**, a **>10× improvement** over the **0.14** capacity of the classical Hopfield network, **surpassing even recent state-of-the-art implementations**.

### 1.5 Why It Is Interesting  
This paper introduces a po
