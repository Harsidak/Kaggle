# Kaggle Machine Learning & Deep Learning Pipelines

This repository contains all my Kaggle notebooks and workflows, featuring advanced, production-grade pipelines developed for high-tier competitions. This workspace currently showcases state-of-the-art architectures for both **Protein Function Prediction** using protein Language Models (pLMs) and **Large Language Model (LLM) Reinforcement Learning** for reasoning alignment.

Please do Visit my [KaggleProfile](https://www.kaggle.com/banwait13)

---


## 🧬 1. CAFA-6 Protein Function Prediction Pipeline
**Notebook:** [cafa-6-pred.ipynb](https://www.kaggle.com/code/banwait13/esm2-protbert-x-prott5)

An ensemble-based framework designed to predict Gene Ontology (GO) terms (Biological Process, Molecular Function, Cellular Component) directly from amino acid sequences.

### 🌟 Key Features
*   **Multi-Model pLM Ensemble:** Combines features from Rostlab's **ProtBERT** and Meta AI's **ESM-2** to form a highly robust feature space.
*   **GPU & TPU Optimization:** Accelerates sequence embedding generation using custom PyTorch device dispatching, including native PyTorch-XLA hooks for Google Cloud TPUs.
*   **Exploratory Data Analysis (EDA):** Custom Seaborn/Matplotlib dashboards visualizing sequence length distributions (log-scale) and the frequency distributions of the top 20 Gene Ontology annotations.
*   **Ensemble Learning:** Employs an average-based prediction ensembling technique to reduce output variance and boost competition metric scores.

---

## 🤖 2. Nemotron-30B Alignment & RL Pipeline
**Notebook:** [nemotron-on-steroids.ipynb](https://www.kaggle.com/code/banwait13/Nemotron-on-steroids)

A complete fine-tuning and reinforcement learning pipeline designed to align the **Nemotron-30B** model into a structured reasoning agent. It uses parameter-efficient adapters (LoRA) and a custom reinforcement learning algorithm inspired by BAPO and DAPO.

### 🚀 Training Lifecycle Phases

```
      +-----------------------------------------+
      |  Phase 1: Supervised Fine-Tuning (SFT)  |
      +-----------------------------------------+
                           |
                           v
      +-----------------------------------------+
      |  Phase 2: Custom RL (BAPO + DAPO)       |
      +-----------------------------------------+
                           |
                           v
      +-----------------------------------------+
      |  Phase 3: Export & Submission           |
      +-----------------------------------------+
```

## 🛠️ Environment Setup & Installation

To run these pipelines locally or in a cloud instance:

```bash
# Clone the repository
git clone <repository-url>
cd Kaggle

# Install dependencies
pip install -r requirements.txt
```

## 📜 License

This project is licensed under the Apache License 2.0. See the `LICENSE` file for details.
