# AI-Driven Permeability Prediction: Benchmarking Seven Machine Learning Models

[![Python 3.9](https://img.shields.io/badge/Python-3.9-blue.svg)](https://www.python.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![RDKit](https://img.shields.io/badge/RDKit-2023.09.1-brightgreen.svg)](https://www.rdkit.org/)
[![TensorFlow](https://img.shields.io/badge/TensorFlow-2.13.0-orange.svg)](https://www.tensorflow.org/)
[![PyTorch](https://img.shields.io/badge/PyTorch-2.0.1-red.svg)](https://pytorch.org/)

## 📌 Overview

This repository contains the complete code, data, and analysis pipeline for the paper:

**"Benchmarking Machine Learning Models for Skin Permeability Prediction: A Comparative Study of SVR, KNN, CNN, RNN, GNN, VAE, and GAN"**

The study compares seven machine learning models for predicting log Kp (cm/s) skin permeability values from molecular SMILES strings, with comprehensive evaluation of accuracy, robustness, scalability, and practical deployment considerations.

### Key Findings
- **SVR** achieved the highest accuracy (98.09%) and scalability for large-scale deployment
- **VAE** showed excellent reconstruction fidelity (96.56%) for molecular descriptors
- **Deep learning models** (CNN, RNN, GNN) underperformed relative to classical methods on this dataset (R² ≈ -0.02)
- **GAN** demonstrated limited applicability (48.92% pseudo-accuracy) for permeability prediction


## 🚀 Quick Start

### Prerequisites

- Python 3.9 or higher
- Conda (recommended) or pip
- 16GB RAM minimum (32GB recommended)
- GPU (optional, for deep learning models)

### Installation

**Option 1: Conda (Recommended)**

```bash
# Clone the repository
git clone https://github.com/yourusername/ai-permeability-prediction-benchmark.git
cd ai-permeability-prediction-benchmark

# Create conda environment
conda env create -f environment.yml
conda activate permeability-benchmark

# Run complete analysis pipeline
python src/training/train_all.py --all-models

# Or run individual models
python src/models/svr_model.py
python src/models/knn_model.py
python src/models/cnn_model.py

# Generate evaluation metrics and figures
python src/evaluation/metrics.py
python src/evaluation/visualization.py

# Run statistical tests
python src/evaluation/statistical_tests.py

Expected Output
After running the pipeline, you should see:

========== SVR REGRESSION REPORT ==========
Accuracy: 98.09%
RMSE: 0.2470
MAE: 0.2055
R2 Score: 0.9049

========== KNN REGRESSION REPORT ==========
Accuracy: 96.70%
RMSE: 0.4235
MAE: 0.3527
R2 Score: 0.7203

========== CNN REGRESSION REPORT ==========
Accuracy: 93.81%
RMSE: 0.8101
MAE: 0.6633
R2 Score: -0.0236

... (continued for RNN, GNN, VAE, GAN)
