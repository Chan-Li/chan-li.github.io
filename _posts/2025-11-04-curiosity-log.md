---
layout: single
title: "🧭 Chan’s Curiosity Log — Nov 4, 2025"
date: 2025-11-04
categories: [theory, machine-learning, neuroscience, physics]
tags: [renormalization-group, scaling-laws, universality, bifurcation, sleep-dynamics, curiosity-log]
permalink: /blog/2025-11-04-curiosity-log/
---

*Daily reflections on new papers, theories, and open questions.*

---

## 🧩 Paper 1 (Worth Reading in Detail): *Renormalization group for deep neural networks — Universality of learning and scaling laws*  
📄 [arXiv:2510.25553 (2025)](https://arxiv.org/abs/2510.25553)

### 1.1 Background  
**Self-similarity**, where observables exhibit the same statistical behavior at different length scales, is ubiquitous in natural systems.  
Such systems display **power-law correlations** and **universality**, and are elegantly studied through the framework of the **renormalization group (RG)**.  
Interestingly, in modern machine learning, **power-law behaviors** are also pervasive — appearing in scaling laws, loss landscapes, and data distributions.

### 1.2 Question  
Unlike in physics, we currently lack a **precise notion of scale** in data or neural models, and it is unclear how **coarse-graining** should be defined for networks.  
This gap obscures the possible **self-similar origins** of observed scaling behaviors and limits our ability to import analytical tools from critical phenomena into machine learning.

### 1.3 Key Idea  
The authors extend the **Neural Network Field Theory** perspective, treating DNN outputs as **fields** and the stochasticity of training as inducing a **distribution** over these fields.  
Departing from prior qualitative analogies, they aim for a **quantitative RG framework** for DNNs with **power-law correlated data**.  

They address DNN-specific challenges such as **spectral discreteness** and **lack of translational invariance**, which hinder conventional coarse-graining.  
Starting from the **infinite-width (Gaussian Process)** limit — where the kernel spectrum follows a power law — they introduce **weak nonlinearities** (quartic terms or finite-width corrections).  
By identifying low kernel eigenmodes as high-energy degrees of freedom, they construct a consistent RG procedure that tracks the effects of **mode elimination and rescaling**.

### 1.4 Key Conclusions & Results  
1. Establish a **concrete correspondence** between neural scaling laws, self-similarity, and RG fixed points.  
2. Show that the **non-local and discrete** nature of neural field theories renders the traditional **scaling dimension** ill-defined; introduce instead a **scaling interval**.  
3. Develop a **dimensional-analysis framework** linking these scaling intervals to **power laws in learning curves** as a function of dataset size \(P\).  
4. Demonstrate a form of **universality** at large \(P\), analogous to **asymptotic freedom**, governed by a **UV fixed point** corresponding to a Gaussian Process, and derive corrections to GP scaling.  
5. Propose that **hyperparameter transfer** between small and large \(P\) systems corresponds to movement along a **shared RG trajectory**.

### 1.5 Why It Is Interesting  
I’ve long been interested in applying **RG theory** to neural networks to compute **scaling exponents** and identify **phase transitions** in learning.  
This paper represents one of the most concrete realizations of that idea — bridging **statistical physics** and **deep learning theory**.  
It might offer the missing theoretical foundation for defining criticality and universality classes in learning systems.

### 1.6 Questions Worth Exploring  
- Beyond coarse-graining kernel modes, can we perform RG along **training time** as a new scaling axis?  
- How do learning rate schedules and optimizer noise influence this **temporal RG flow**?  
- Can we define a **beta function** describing how effective capacity or generalization scales with time or dataset size?

---

## 🌙 Paper 2: *Falling asleep follows a predictable bifurcation dynamic*  
📄 [Nature Neuroscience (2025)](https://www.nature.com/articles/s41593-025-02091-1)

### 2.1 Background  
Falling asleep involves profound **behavioral and physiological changes** — reduced responsiveness, muscle relaxation, slower heart and respiration rates, and altered pupil and EEG activity.  
These changes reflect coordinated transformations in brain dynamics measurable through **EEG band power**, **connectivity**, and **microstate topographies**.

### 2.2 Question  
Despite extensive EEG studies, our understanding of how these gradual changes culminate in the **loss of wakefulness** remains incomplete.  
Prior approaches segment EEG into discrete microstates (e.g., wake, drowsy, sleep) but offer limited insight into **continuous transition dynamics**.  
Recent models suggest the **wake–sleep transition** might follow a **fold (saddle-node) bifurcation**, yet **no direct experimental confirmation** has been provided.

### 2.3 Key Idea  
The authors develop a **new dynamical framework** for quantifying and modeling the **process of falling asleep**, validated on two independent EEG datasets.  
Their model captures continuous evolution in EEG features and successfully predicts individual sleep trajectories **in quasi-real time**.

### 2.4 Key Conclusions & Results  
- Provide the **first experimental evidence** that falling asleep follows a **bifurcation dynamic** in brain-state space.  
- Show that **sleep onset** can be modeled and predicted through continuous dynamics governed by **fold bifurcation geometry**.  
- Demonstrate **real-time predictive power** for individualized sleep progression.  

### 2.5 Why It Is Interesting  
The **sleep–wake transition** behaves like a **phase transition**, and this paper formalizes it as a **bifurcation phenomenon**.  
It invites the analogy between **neural-state bifurcations** and **critical phenomena** in physics — suggesting that sleep might be viewed through the lens of **order parameter dynamics** and **critical slowing down**.

### 2.6 Questions Worth Exploring  
- Is the sleep transition an **equilibrium phase transition**, or a **non-equilibrium** one akin to the **superconducting transition**?  
- Could one measure a **critical exponent** (e.g., of EEG variance or correlation length) near the sleep onset?  
- Are similar bifurcation structures present in other cognitive transitions, such as **attention** or **consciousness loss** under anesthesia?

---

🌀 *Overall reflection:* both papers highlight the unifying power of **dynamical systems and RG theory** — from scaling in neural networks to bifurcations in neural states — revealing how critical phenomena may underlie both **lea**
