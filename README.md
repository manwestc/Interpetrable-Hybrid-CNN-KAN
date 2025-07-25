# Interpretable CNN–KAN Hybrid Architectures for Tabular Data with Synthetic Image Encoding

[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/manwestc/Interpetrable-Hybrid-CNN-KAN/blob/master/LICENSE)
[![Python Version](https://img.shields.io/badge/Python-3.9%2B-blue)](https://pypi.python.org/pypi/)
[![Documentation Status](https://readthedocs.org/projects/morph-kgc/badge/?version=latest)](https://tintolib.readthedocs.io/en/latest/)
[![TINTOlib](https://img.shields.io/badge/library-TINTOlib-9cf)](https://github.com/oeg-upm/TINTOlib)

#### This repository supports the scientific article **"Interpretable CNN–KAN Hybrid Architectures for Tabular Data with Synthetic Image Encoding"**.

It contains all experiments and hybrid model configurations used to evaluate the combination of **Kolmogorov–Arnold Networks (KANs)** and **Convolutional Neural Networks (CNNs)** on synthetic images generated from tabular data using various encoding methods from [TINTOlib](https://tintolib.readthedocs.io/en/latest/), including **TINTO**, **IGTD**, and **REFINED**.

---

## 🔎 Explore this GitHub with DeepWiki

This repository has a dedicated space on **[DeepWiki]([https://deepwiki.com/oeg-upm/TINTOlib](https://deepwiki.com/manwestc/MIMO-indoor-localization-with-HybridNN-TINTOlib))**, where you can explore semantic documentation, relevant links, bibliography, and answers to frequently asked questions about its use and application.

<p align="center">
  <a href="https://deepwiki.com/manwestc/MIMO-indoor-localization-with-HybridNN-TINTOlib" target="_blank">
    <img src="https://deepwiki.com/badge.svg" alt="Ask DeepWiki"/>
  </a>
</p>


## 🧪 Structure of This Repository

- `Experiments/` – Reproducible experiments for CNN, KAN, and CNN–KAN on four datasets.
- `src/` – Adapted subset of the official [`pykan`](https://github.com/KindXiaoming/pykan) library.
- `models/` – CNN, KAN, and hybrid model definitions and training pipelines.
- `imgs/` – Figures used in the scientific article.

> 🔧 This is a customized fork of `pykan`, focused on symbolic-visual hybridization using synthetic image encoding.

---

## 🔍 About TINTOlib

<div align="center">
<img src="imgs/logo.svg" alt="TINTO Logo" width="140"/>
</div>

**TINTOlib** is a Python library that transforms **tidy tabular data** into grayscale **synthetic images**, making it possible to apply deep learning models such as CNNs and ViTs to structured data.

### 📺 VideoTutorial Course (English/Spanish)

🎥 Prefer not to register on Udemy or looking for the English version of the course? No worries — you can follow the full course directly on GitHub!

This hands-on tutorial includes **bilingual videos (English/Spanish)** and **practical notebooks** to help you learn how to use **TINTOlib** with deep learning models like CNNs, ViTs, and hybrid architectures.

<p align="center">
  <a href="https://github.com/oeg-upm/TINTOlib-Crash_Course" target="_blank">
    <img src="https://img.shields.io/badge/GitHub-VideoTutorial%20Course-black?style=for-the-badge&logo=GitHub&logoColor=white" alt="Access the Course on GitHub"/>
  </a>
</p>

### 📘 Learn more: 
- [📘 Documentation](https://tintolib.readthedocs.io/en/latest/)
- [🚀 GitHub](https://github.com/oeg-upm/TINTOlib)
- [📹 Crash Course](https://github.com/oeg-upm/TINTOlib-Crash_Course)

---


## 🧠 About KANs

**Kolmogorov–Arnold Networks (KANs)** are neural networks based on a solid theoretical foundation—the Kolmogorov–Arnold representation theorem. Unlike MLPs, KANs use activation functions on **edges**, enabling symbolic learning and improved interpretability.

📘 Official docs: [https://kindxiaoming.github.io/pykan](https://kindxiaoming.github.io/pykan)

---


## 📊 Datasets

The following tabular datasets were used:

- **Treasury** (regression)
- **Puma** (regression)
- **Forex** (classification)
- **Robot Wall** (classification)

Each dataset is encoded with three image generation methods (IGTD, REFINED, TINTO) and tested with:

- `KAN` – symbolic model
- `CNN` – visual model
- `CNN–KAN` – hybrid late-fusion model

---

## 🧩 Model Architectures

| Model      | Description                                    |
|------------|------------------------------------------------|
| **KAN**    | Symbolic, edge-based activation architecture   |
| **CNN**    | Standard image-based convolutional network     |
| **CNN–KAN**| Late-fusion hybrid model combining CNN and KAN |

Each hybrid model computes a **Global Feature Score (GFS)** to merge relevance signals from symbolic and visual branches.

<div align="center">
<img src="imgs/HyNN.png" alt="Hybrid Neural Network with CNN and KAN" width="550"/>
</div>

---

## ▶ How to Run

1. **Clone the repo:**
```bash
git clone https://github.com/<your-org>/Interpretable-CNN-KAN-Hybrid.git
cd Interpretable-CNN-KAN-Hybrid
```

2. **(Optional) Create a conda environment:**
```bash
conda create --name kan-hybrid python=3.9
conda activate kan-hybrid
```

3. **Install requirements:**
```bash
pip install -r requirements.txt
```

4. **Launch an experiment:**
```bash
python Experiments/train_puma_hybrid.py
```


---

## 🧠 Authors

- **Giovanny Mondragon-Ruiz()**
- **Jiayun Liu**
- **[Manuel Castillo-Cara](https://github.com/manwestc)**
- **Raúl García-Castro**

---

## 🏫 Institutions

<div align="center">
<kbd><img src="imgs/logo-uned-.jpg" width="180"/></kbd>
<kbd><img src="imgs/logo-upm.png" width="120"/></kbd>
</div>

---

## 📜 License

This repository is released under the **MIT License**, inheriting the terms from the original [`pykan`](https://github.com/KindXiaoming/pykan) library by Ziming Liu et al. (MIT).

> This fork is reduced to essential components to support the hybrid CNN–KAN evaluation framework.
