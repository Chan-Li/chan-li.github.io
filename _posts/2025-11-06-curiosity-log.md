---
layout: single
title: "🧭 Chan’s Curiosity Log — November 6, 2025"
date: 2025-11-06
categories: [theory, neuroscience, machine-learning, physics]
tags: [motor-control, predictive-coding, transformer, signal-propagation, dmft, curiosity-log]
permalink: /blog/2025-11-06-curiosity-log/
---

*Daily reflections on new papers, theories, and open questions.*

---

## 🧩 Paper 1: *Sensory expectations shape neural population dynamics in motor circuits*  
📄 [Nature (2025)](https://www.nature.com/articles/s41586-025-09690-9)

### 1.1 Background  
Humans and animals can often **prepare a movement in advance**, and such preparation generally improves precision.  
The neural basis of movement preparation—and its relationship to execution—has frequently been studied through **delayed action paradigms**, in which the upcoming movement is known but execution must await a go cue.

### 1.2 Questions  
Although preparing specific movement parameters is essential for self-initiated actions, movements are often **triggered or corrected by sensory inputs** resulting from disturbances.  
This study asks whether **motor cortical areas rapidly respond to sensory inputs** in ways that account for **biomechanical and task constraints**.

### 1.3 Key Idea  
This is an **experimental paper**. To test whether **expected sensory inputs shape preparatory activity** in motor cortical areas, the authors designed a task where participants received **probabilistic cues** about how an upcoming **mechanical perturbation** would displace their arm.

### 1.4 Key Conclusions & Results  
When cued about the likely direction of future perturbations, **humans and macaques** incorporated these **expectations** into movement preparation, improving performance.  
They show that information about **sensory expectations** is **robust and widespread** in **monkey motor circuits**, but absent in early sensory areas.  
The **neural geometry** of these signals is simple, directly representing the **probability** of each perturbation direction.  
A **normative model** of the motor system explains how this neural geometry benefits countering perturbations and how it depends on the **timing of sensory signals**.

### 1.5 Why It Is Interesting  
This paper provides **experimental validation** of how **movement preparation** shapes neural activity, linking behavior and neural dynamics.

### 1.6 Questions Worth Exploring  
This work connects directly to **predictive coding**, a biologically grounded framework.  
Can **predictive coding** improve model performance in artificial networks?  
Since predictive coding has been shown to be **mathematically equivalent to backpropagation**, this could bridge biological and machine learning models.

---

## 🧠 Paper 2 (Worth Reading in Detail): *Geometric dynamics of signal propagation predict trainability of transformers*  
📄 [Phys. Rev. E (2025)](https://journals.aps.org/pre/pdf/10.1103/gjsm-l642)

### 2.1 Background  
Deep **transformers** have achieved enormous success in NLP, vision, and beyond, yet a strong **theoretical understanding** of their behavior remains elusive.

### 2.2 Questions  
It is unclear how to use a **quantitative description of signal propagation** in deep transformers to guide **initialization schemes** that ensure good generalization.  
How does **depth** influence **trainability**?

### 2.3 Key Idea  
The authors propose a **theoretical framework** for analyzing **forward and backward signal propagation** in deep transformers through the lens of **token geometry**.  
They study an ensemble of random deep transformers acting on \(n\) tokens.  
Each layer consists of a **single-head self-attention block** followed by a **token-wise multilayer perceptron (MLP)** with a **residual branch**.  
The three key components of the layer-wise map are: **attention**, **MLP**, and **normalization**.

### 2.4 Key Conclusions & Results  
> “Our theory reveals distinct **dynamical phases** which would be absent in pure-attention models.  
> In the forward direction, we observe an **order–chaos transition** characterized by diverging versus collapsing token angles.  
> In the backward direction, we find a separate transition between **exploding versus vanishing gradients**.  
> These phase boundaries are distinct, unlike in pure MLPs.  
> We propose an **initialization scheme** that places the transformer at the intersection of both phase boundaries.  
> This ensures that dynamics preserve both \(O(1)\) token angles and \(O(1)\) gradients.  
> Empirically, this initialization improves final test loss, showing that the **geometric dynamics** of deep transformers are crucial for controlling performance.”  

### 2.5 Why It Is Interesting  
This paper introduces the idea of interpreting the **layer-wise architecture as implementing a dynamical system** on the input space.  
Given our familiarity with **dynamical mean-field theory (DMFT)**, it raises the possibility of studying **deep networks as dynamical systems** governed by similar principles.

### 2.6 Questions Worth Exploring  
How can **DMFT** be implemented to analyze deep networks like transformers?  
This framework appears **independent from replica or random matrix theory**, offering a **new theoretical tool** worth mastering.

---
