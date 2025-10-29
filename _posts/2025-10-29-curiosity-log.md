---
layout:single
title: "🧭 Chan’s Curiosity Log — October 29, 2025"
date: 2025-10-29
categories: [theory, machine-learning, physics]
tags: [neuroscience, rnns, spiking-neural-networks, inductive-bias, energy-efficiency, curiosity-log]
permalink: /blog/2025-10-29-curiosity-log/
---

*Daily reflections on new papers, theories, and open questions.*

---

## 🧩 Paper 1: *Single-unit activations confer inductive biases for emergent circuit solutions to cognitive tasks*  
📄 [Nature Machine Intelligence (2025)](https://www.nature.com/articles/s42256-025-01127-2)

### 1.1 Background  
Recurrent neural networks (RNNs) serve as computationally tractable models that capture key features of biological neural networks.  
Analyzing task solutions that emerge in RNNs through training provides hypotheses for how biological circuits may perform similar computations.  
A comprehensive study of RNNs with different architectures found that, despite differences in the geometry of neural dynamics, they rely on similar computational scaffolds characterized by the *topological structure of fixed points.*

### 1.2 Question  
Are these architectural choices (activation functions, connectivity constraints, etc.) truly inconsequential to the circuit mechanisms that emerge in RNNs through training?  
This question has not been systematically tested.

### 1.3 Key Idea  
They trained RNNs with three common activation functions — **ReLU**, **sigmoid**, and **tanh** — both **with** and **without Dale’s law** (restricting each neuron to be either excitatory or inhibitory).  
> **Dale’s law**: a single neuron releases the same neurotransmitter at all of its axon terminals.

### 1.4 Key Results & Conclusions  
1. Neural representations and dynamics differed across RNNs with varying activation functions — **tanh** networks diverged most from both **sigmoid** and **ReLU** RNNs.  
2. Using a **model distillation** approach, the authors found that these differences arose from **distinct circuit solutions** that the RNNs developed to solve the same task.

### 1.5 Why It Is Interesting  
This paper is conceptually linked to yesterday’s study, highlighting that **reverse-engineering RNNs requires caution**.  
It emphasizes the need to identify architectures whose **inductive biases** best align with biological neural data.

### 1.6 Questions Worth Exploring  
- Can we define **universality classes** for neural networks?  
- Can reverse-engineering be done in a **cluster or manifold sense**?  
- Perhaps this should be explored from a **probabilistic** or **statistical-mechanics** perspective.

---

## ⚡ Paper 2: *ONE-TIMESTEP IS ENOUGH: Achieving High-Performance ANN-to-SNN Conversion via Scale-and-Fire Neurons*  
📄 [arXiv:2510.23383 (2025)](https://arxiv.org/pdf/2510.23383)

### 2.1 Background  
The high energy consumption of ANN inference has become a critical bottleneck.  
**Spiking Neural Networks (SNNs)** offer an energy-efficient alternative, but training them remains challenging due to non-differentiable spikes and complex temporal dynamics.  

Two major paradigms exist:  
- **Direct SNN training**, which requires backpropagation through time (BPTT) and is memory-intensive.  
- **ANN-to-SNN conversion (ANN2SNN)**, which replaces ANN modules with spiking counterparts and aligns firing rates with ANN activations — far more efficient but typically requiring **many time steps** to reach comparable accuracy.

### 2.2 Question  
Can SNNs be trained or converted efficiently while maintaining **high performance at arbitrary (especially single) timesteps**?

### 2.3 Key Idea  
The authors develop a **Temporal-to-Spatial Equivalence Theory**, proving that multi-timestep integrate-and-fire (IF) neurons are equivalent to **single-timestep multi-threshold neurons (MTN)**.  
This enables high-precision ANN2SNN conversion under **T = 1** inference.  
They introduce the **Scale-and-Fire Neuron (SFN)** — combining a scaling mechanism with an adaptive fire function for efficient single-step computation.

### 2.4 Key Results & Conclusions  
1. Demonstrated that **temporal integration** can be replaced by **spatial multi-threshold mechanisms** within a single timestep.  
2. Designed the **Scale-and-Fire Neuron (SFN)** for energy-efficient ANN2SNN conversion.  
3. Proposed the **SFN-based Spiking Transformer (SFormer)** that integrates SFN into Transformer architectures, addressing activation variability through custom fire functions and thresholds.  
4. Achieved **88.8 % accuracy on ImageNet-1K at T = 1**, surpassing the previous state-of-the-art (84.0 % at T = 2) while reducing energy use by 5 %.

### 2.5 Why It Is Interesting  
In my future project, I aim to develop a **non-equilibrium training algorithm** that is both **efficient and biologically plausible**.  
The theoretical framework and methods here may offer valuable inspiration for **energy-efficient learning dynamics**.

### 2.6 Questions Worth Exploring  
- What are the **underlying dynamics** of this new training approach?  
- Can such frameworks enable **continual learning** or adaptive energy-aware updates?

---

🧠 *Overall reflection:* both papers emphasize how **architectural biases** and **energy constraints** shape emergent computation — one from the biological-circuit perspective, the other from the hardware-efficiency frontier.
