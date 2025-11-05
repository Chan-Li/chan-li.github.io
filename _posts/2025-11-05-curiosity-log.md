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
This paper introduces a powerful **information-theoretic lens** to interpret and improve associative memory.  
By quantifying the **functional contribution of each neuron**, it opens new directions for **analyzing**, **pruning**, or **regularizing** neural systems at the single-unit level.

### 1.6 Questions Worth Exploring  
1. Can **PID** be applied to **other architectures** to quantify contributions at the **connection or module level**, potentially enabling **continual learning** and **network pruning**?  
2. Since **Hopfield networks ≈ Transformers**, could redundancy-based objectives enhance **transformer training** or improve **context retention**?

---

## 🧠 Paper 2: *Space as Time Through Neuron Position Learning*  
📄 [arXiv:2511.01632 (2025)](https://arxiv.org/pdf/2511.01632)

### 2.1 Background  
Biological neural networks exist in **physical space**, where **distance translates into time** through **axonal conduction delays** — a “space as time” principle.  
Connection costs scale with spatial distance, and conduction delays vary across the nervous system, influenced by factors such as axonal length, diameter, and **myelin plasticity**.  
Yet most computational models ignore this **spatial embedding** and its temporal consequences.

### 2.2 Question  
How are **spatial structure** and **temporal processing** jointly organized in the brain?  
Despite being intertwined, existing studies rarely analyze how **neuron position** and **information timing** co-evolve.

### 2.3 Key Idea  
The authors develop a **unified framework** combining **spatial embedding** and **temporal delay learning** for **spiking neural networks (SNNs)**.  
They introduce a **gradient-based learning algorithm** where **synaptic delays** depend on **Euclidean distances** between connected neurons.  
Moreover, they derive **gradients of loss functions with respect to neuron positions**, effectively enabling **neural network shape learning**.

### 2.4 Key Conclusions & Results  
- Networks trained on **temporal classification tasks** spontaneously **self-organize** into **local small-world topologies**.  
- **Modular structure** emerges naturally under **distance-dependent connection costs**.  
- Functional **specialization** aligns with **spatial clustering**, despite no explicit enforcement of such organization.

### 2.5 Why It Is Interesting  
This work connects **spatial embedding** and **temporal coding**, suggesting that neural systems might *learn their own geometry*.  
Just as **positional embeddings** revolutionized NLP, **delay learning** could become a key mechanism for efficient spatiotemporal computation — biologically plausible and potentially extendable to artificial systems.

### 2.6 Questions Worth Exploring  
- Can we design networks that **learn delay embeddings** autonomously, revealing whether **time** and **space** representations co-emerge?  
- How does **delay plasticity** interact with **energy efficiency** and **synchronization** in spiking or transformer-like models?

---

🌀 *Overall reflection:* both studies highlight the emergence of **structure and function from information principles** — one through **redundancy maximization** in associative memory, the other through **spatial-temporal learning** that turns geometry into computation.
