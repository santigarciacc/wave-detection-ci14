# Redefining Epidemiological Waves: Structural Stability and Global Empirical Validation in Sobolev Spaces

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://python.org)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

**Author:** [Santi García-Cremades](https://github.com/SantiGarciaCremades) - *Universidad Miguel Hernández (UMH)*

This repository contains the full mathematical engine and visualization pipeline for the paper:  
> *"Redefining Epidemiological Waves: Structural Stability and Global Empirical Validation in Sobolev Spaces."*

## 🔬 Overview
Traditional epidemiological models often struggle to universally define what constitutes a "wave," relying on arbitrary thresholds or absolute case counts that are highly vulnerable to administrative noise, testing capacity, and weekend under-reporting. 

This project shifts the paradigm. We introduce **Topological Condemnation**, a purely mathematical approach that detects kinematic fluctuations within an $H^3$ Sobolev Space. By projecting the raw incidence series into this space via Tikhonov regularization, we restore the structural curvature of the pandemic and isolate waves strictly through their local kinematic parameters (velocity zero-crossings).

$$\hat{x} = \arg\min_{x \in \mathbb{R}^n} \|x - Y\|_2^2 + \lambda \|\nabla^3 x\|_2^2$$

## ✨ Key Features
* **$H^3$ Sobolev Regularization:** Strips out administrative noise while preserving the macro-structural geometric curvature of the epidemiological curve.
* **Strict Kinematic Detection:** Waves are perfectly bounded by exact topological zero-crossings of the velocity ($v = 0 \rightarrow v > 0$ to $v = 0 \rightarrow v \leq 0$).
* **Structural Stability Index ($S$):** A robust metric (from 0 to 1) scoring the resilience of an epidemic wave across a 20-configuration hyperparameter grid (varying $\lambda$ and $A_{min}$).
* **Fixed Epidemiological Duration ($L=14$):** Computations are anchored to a minimum duration of 14 days, reflecting the true clinical and transmission cycle of SARS-CoV-2.
* **Memory-Optimized Global Processing:** Capable of processing and rendering hundreds of high-resolution figures for global datasets in a single pass without RAM leaks, utilizing dynamic garbage collection.

## 🚀 Getting Started

### Prerequisites
Ensure you have Python 3.8+ installed. Install the required dependencies:
```bash
pip install numpy pandas scipy matplotlib seaborn jupyter
