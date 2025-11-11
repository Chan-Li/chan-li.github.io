---
layout: single
title: "🧭 Chan’s Curiosity Log — Nov 10, 2025"
date: 2025-11-10
categories: [theory, machine-learning, physics]
tags: [reservoir-computing, recurrent-networks, neuronal-correlation, memory-capacity, scaling-laws, curiosity-log]
permalink: /blog/2025-11-10-curiosity-log/
---

*Daily reflections on new papers, theories, and open questions.*

---

## 🧩 Paper: *Neuronal correlations shape the scaling behavior of memory capacity and nonlinear computational capability of reservoir recurrent neural networks*  
📄 [Phys. Rev. Research (2025)](https://journals.aps.org/prresearch/pdf/10.1103/cwvm-s53p)

### 1.1 Background  
High computational demands pose a major obstacle to applying deep learning in **real-time edge computing**.  
In contrast to conventional training methods such as **backpropagation through time (BPTT)**, **reservoir computing (RC)** optimizes only **readout weights** and leaves all other connections fixed—enabling fast and low-cost learning.  
Despite this simplicity, RC achieves **high computational performance** and has wide applicability for processing time-series data.  

In a typical RC setup, the **readout connections** linking reservoir units to outputs are sparse, meaning that the size of the reservoir \(N\) is much larger than the number of readout units \(L\).

### 1.2 Questions  
Understanding the relationship between \(L\) and the **computational ability** of a reservoir is essential for building cost-effective RC systems.  
However, a **guiding principle** for determining an appropriate \(L\) has yet to be fully explored.

### 1.3 Key Idea  
The authors investigate how **memory capacity (MC)** and **nonlinear computational ability**—two determinants of reservoir computational power—**scale with \(L\)**, focusing on the role of **neuronal correlations**.  
They use the same theoretical method as in **Clark et al.**  
> D. G. Clark, L. F. Abbott, and A. Litwin-Kumar, *Dimension of activity in random neural networks*, Phys. Rev. Lett. 131, 118401 (2023).

### 1.4 Key Conclusions and Results  
1. The **memory capacity** of an RNN **increases monotonically** with \(L\), though its **growth rate declines** as \(L\) grows.  
2. They develop a theory to analytically derive **memory capacity** for \(L \sim O(\sqrt{N})\).  
   Using this framework, they show that even **weak neuronal correlations**—of magnitude \(O(1 / \sqrt{N})\)—play an essential role in the **declining growth rate** of memory capacity.  
3. Numerical simulations reveal that the ability to perform **nonlinear tasks** emerges **supralinearly and sequentially** as \(L\) increases.  
These results suggest that the number of readout connections should be **task-dependent**, tuned to the specific **memory** and **nonlinearity** requirements.

### 1.5 Why It Is Interesting  
Clark’s previous work analyzed **random recurrent neural networks**, computing correlations between neurons across time steps.  
It is natural to **extend** this framework to **reservoir computing**, since its recurrent connections are also random.

### 1.6 Questions Worth Exploring  
If reservoir computing can be described in this way, could we build a version for **transformers**, given that **Ganguli’s group** has already developed a theory for **random transformers**?
