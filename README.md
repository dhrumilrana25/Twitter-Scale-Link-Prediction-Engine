# Twitter-Scale Link Prediction Engine

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)

An S-Ranked, high-performance link prediction system for massive social graphs. [cite_start]This engine leverages a hybrid architecture combining **DeepWalk** embeddings with classical graph heuristics to solve the "Who to Follow" social discovery problem[cite: 1, 9, 13].

## 🚀 Performance Breakthrough
[cite_start]This model effectively demolishes traditional local-only heuristics by capturing long-range structural dependencies in sparse networks[cite: 7, 14].

| Metric | Common Neighbors (Baseline) | Deep-Graph Hybrid (This Model) |
| :--- | :--- | :--- |
| **AUC** | [cite_start]0.50 [cite: 12, 198] | [cite_start]**0.8872** [cite: 12, 205] |
| **Precision** | [cite_start]0.50 [cite: 198] | [cite_start]**0.8707** [cite: 205] |
| **F1-Score** | [cite_start]0.66 [cite: 198] | [cite_start]**0.8217** [cite: 205] |

## 🛠️ Architecture Overview
* [cite_start]**Feature Engineering**: 1028-dimensional vector combining 256-D skip-gram embeddings with Jaccard, Adamic-Adar, and Resource Allocation metrics[cite: 11, 45, 176].
* [cite_start]**Latent Representation**: Optimized DeepWalk implementation using truncated random walks (1,000,000 walks, length 20)[cite: 44, 123, 124].
* [cite_start]**Classification**: Supervised Random Forest model optimized with Gini impurity and stratified sampling to handle network sparsity[cite: 46, 164, 182].
* [cite_start]**Scalability**: Specifically engineered to handle a 1.2M node / 1M edge subset of the Twitter-2010 graph within a resource-constrained CPU environment[cite: 83, 84, 172, 188].

## 💻 Quick Start (Automation-First)
This repository is fully automated for zero-friction deployment.

1. **Clone the Repo**:
   ```bash
   git clone [https://github.com/your-username/Twitter-Link-Prediction-Engine.git](https://github.com/your-username/Twitter-Link-Prediction-Engine.git)
   cd Twitter-Link-Prediction-Engine
