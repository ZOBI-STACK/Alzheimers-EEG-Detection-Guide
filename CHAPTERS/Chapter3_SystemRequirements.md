# CHAPTER 3: SYSTEM REQUIREMENTS

## 3.1 Hardware Requirements

### 3.1.1 Processor (CPU)

**Minimum:**
- Dual-core processor, 2.0+ GHz
- Intel Core i5 or AMD Ryzen 5
- Sufficient for preprocessing and traditional ML

**Recommended:**
- Quad-core processor, 2.5+ GHz
- Intel Core i7/i9 or AMD Ryzen 7/9
- For deep learning model training

**For Production:**
- 8+ cores, 3.0+ GHz
- Server-grade processor
- Handles concurrent requests

### 3.1.2 RAM (Memory)

**Minimum:** 8 GB
- Suitable for small datasets
- Traditional ML only
- Limited multitasking

**Recommended:** 16 GB
- Comfortable for deep learning
- Multiple models simultaneously
- Large dataset processing

**Optimal:** 32+ GB
- Enterprise-level processing
- Large batch sizes
- Multiple GPU training

### 3.1.3 GPU (Graphics Processor)

**For Deep Learning - HIGHLY RECOMMENDED:**

**NVIDIA GPUs (Recommended):**
- **Entry Level**: GTX 1650, RTX 3050 (4 GB VRAM)
- **Mid-Range**: RTX 3060/3070 (8-10 GB VRAM) ✓ Best for this project
- **High-End**: RTX 4080/4090 (24+ GB VRAM)

**AMD GPUs:**
- Radeon RX 6700 XT
- Radeon RX 7900 XT

**Apple Silicon:**
- M1/M2/M3 Pro/Max
- Built-in GPU acceleration with TensorFlow/PyTorch

**Cloud GPUs (No hardware needed):**
- Google Colab (Free T4 GPU)
- AWS EC2 (p3/p4 instances)
- Azure GPU instances

**GPU Memory Recommendations:**
| GPU VRAM | Max Batch Size | Suitable For |
|----------|---|---|
| 2-4 GB | 8-16 | Inference, testing |
| 6-8 GB | 32-64 | Training small models |
| 10-12 GB | 64-128 | Training DL models ✓ |
| 24+ GB | 256+ | Large-scale training |

### 3.1.4 Storage

**Minimum:** 500 GB SSD
- Project files: 50 GB
- Datasets: 200-300 GB
- Models: 5-10 GB
- Results: 50 GB

**Recommended:** 1 TB SSD
- More comfortable workspace
- Multiple dataset versions
- Model checkpoints
- Backup space

**For Production:** 2+ TB
- Large dataset storage
- Model versioning
- Log files
- Redundancy

### 3.1.5 Complete Hardware Configuration

**Option 1: Budget Setup (~$800-1200)**
```
CPU: Intel i5-12400 / AMD Ryzen 5 5600X
RAM: 16 GB DDR4
GPU: NVIDIA RTX 3060 (12 GB)
Storage: 512 GB NVMe SSD
Monitor: 24" Full HD
Keyboard/Mouse: Standard
```

**Option 2: Optimal Setup (~$1500-2500)**
```
CPU: Intel i7-13700K / AMD Ryzen 7 7700X
RAM: 32 GB DDR5
GPU: NVIDIA RTX 4070 (12 GB)
Storage: 1 TB NVMe SSD + 2 TB HDD
Monitor: 27" 1440p
Peripherals: Mechanical keyboard, mouse
```

**Option 3: Enterprise Setup (~$3000-5000)**
```
CPU: Intel Xeon W9-3495X / AMD EPYC
RAM: 64 GB DDR5
GPU: 2x NVIDIA RTX 4090 (48 GB total)
Storage: 2 TB NVMe SSD + 10 TB HDD
Cooling: Adequate cooling system
Network: 10 Gbps connection
```

---

## 3.2 Software Requirements

### 3.2.1 Operating System

**Supported:**
- Windows 10/11 (64-bit)
- macOS 11+ (Intel/Apple Silicon)
- Ubuntu 20.04+ (Linux)
- CentOS 7+

**Recommended:** Ubuntu 22.04 LTS
- Best ML/DL support
- Official CUDA/cuDNN support
- Lower overhead

### 3.2.2 Python Version

**Requirement:** Python 3.8+
**Recommended:** Python 3.9, 3.10, or 3.11

**Check Python Version:**
```bash
python --version
# or
python3 --version
```

**Install Python 3.10:**

**Windows:**
1. Download from python.org
2. Run installer
3. Check "Add Python to PATH"
4. Complete installation

**macOS:**
```bash
brew install python@3.10
```

**Ubuntu/Linux:**
```bash
sudo apt-get update
sudo apt-get install python3.10 python3.10-venv python3.10-dev
```

---

## 3.3 Software Installation Guide

### 3.3.1 Anaconda Installation (RECOMMENDED)

**Why Anaconda?**
- Includes Python + 250+ packages
- Easy environment management
- Pre-configured for data science
- Handles dependencies well

**Installation Steps:**

**Windows:**
1. Download from anaconda.com
2. Run installer
3. Check "Add Anaconda to PATH"
4. Complete installation
5. Verify:
   ```bash
   conda --version
   ```

**macOS:**
```bash
# Download from anaconda.com or use Homebrew
brew install anaconda
conda init zsh  # or bash
```

**Ubuntu/Linux:**
```bash
wget https://repo.anaconda.com/archive/Anaconda3-2024.02-Linux-x86_64.sh
bash Anaconda3-2024.02-Linux-x86_64.sh
conda init
```

### 3.3.2 Create Project Environment

**Step 1: Create New Environment**
```bash
conda create -n eeg_ad python=3.10 -y
```

**Step 2: Activate Environment**
```bash
# Windows
conda activate eeg_ad

# macOS/Linux
source activate eeg_ad
```

**Step 3: Verify**
```bash
python --version
which python  # Should show conda env path
```

### 3.3.3 Essential Python Libraries Installation

**Core Data Science Libraries:**
```bash
pip install numpy pandas scipy scikit-learn matplotlib seaborn plotly
```

**EEG Signal Processing:**
```bash
pip install mne pyeeg pywt
```

**Machine Learning:**
```bash
pip install scikit-learn xgboost lightgbm catboost
```

**Deep Learning - TensorFlow:**
```bash
pip install tensorflow keras
```

**Deep Learning - PyTorch (GPU):**
```bash
# For GPU support
pip install torch torchvision torchaudio pytorch-cuda=11.8 -c pytorch -c nvidia

# OR for CPU only
pip install torch torchvision torchaudio -c pytorch
```

**Jupyter Notebook:**
```bash
pip install jupyter notebook jupyterlab
```

**Web Framework:**
```bash
pip install flask flask-cors fastapi uvicorn
```

**Utilities:**
```bash
pip install python-dotenv requests tqdm openpyxl
```

### 3.3.4 Requirements File Installation

**Create requirements.txt:**
```bash
numpy==1.24.3
pandas==2.0.2
scipy==1.10.1
scikit-learn==1.2.2
matplotlib==3.7.1
seaborn==0.12.2
mne==1.4.0
tensorflow==2.13.0
torch==2.0.1
xgboost==2.0.0
jupyter==1.0.0
flask==2.3.2
```

**Install All:**
```bash
pip install -r requirements.txt
```

---

## 3.4 IDE and Editor Setup

### 3.4.1 VS Code (RECOMMENDED)

**Installation:**

1. Download from code.visualstudio.com
2. Install following OS instructions
3. Open VS Code

**Install Extensions:**
1. Python extension (Microsoft)
2. Jupyter extension
3. Python Debugger
4. Pylance
5. Remote - SSH (optional)

**Configuration:**
```json
// .vscode/settings.json
{
    "python.defaultInterpreterPath": "${workspaceFolder}/venv/bin/python",
    "python.linting.enabled": true,
    "python.linting.pylintEnabled": true,
    "jupyter.notebookFileRoot": "${workspaceFolder}"
}
```

### 3.4.2 PyCharm

**Installation:**
- Download Community or Professional edition
- Install JetBrains Toolbox (recommended)
- Open project folder
- Configure Python interpreter

**Professional Edition Features:**
- Advanced debugging
- Remote deployment
- Scientific tools
- Database integration

### 3.4.3 Jupyter Notebook

**Start Jupyter:**
```bash
jupyter notebook
# or
jupyter lab
```

**Browser Access:** http://localhost:8888

---

## 3.5 CUDA/cuDNN Setup (For GPU Training)

### 3.5.1 Why CUDA?

- Enables GPU acceleration
- 50-100x faster training
- Required for TensorFlow/PyTorch GPU

### 3.5.2 Check GPU Support

```bash
# Windows/Linux
nvidia-smi

# macOS
# Check Activity Monitor or Terminal
```

**Expected Output:**
```
+-----------------------------------------------------------------------------+
| NVIDIA-SMI 535.104.05  Driver Version: 535.104.05                          |
| GPU  Name                   Sm  Memory-Usage | GPU-Util  Compute M.       |
|   0  NVIDIA RTX 3060         86    4000MiB /  12000MiB |  30%  Default     |
+------------------------------------------------------+-----------+-----------+
```

### 3.5.3 CUDA Installation

**Check NVIDIA CUDA Compatibility:**
1. Go to nvidia.com/cuda-toolkit
2. Select your OS and GPU
3. Download installer
4. Follow official installation guide

**Verify CUDA:**
```bash
nvcc --version
```

---

## 3.6 Git Installation and Setup

### 3.6.1 Install Git

**Windows:**
- Download from git-scm.com
- Run installer
- Use default settings

**macOS:**
```bash
brew install git
```

**Ubuntu/Linux:**
```bash
sudo apt-get install git
```

### 3.6.2 Configure Git

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

### 3.6.3 Clone Project Repository

```bash
git clone https://github.com/ZOBI-STACK/Alzheimers-EEG-Detection-Guide.git
cd Alzheimers-EEG-Detection-Guide
```

---

## 3.7 Complete Environment Setup Script

**setup_environment.sh (for macOS/Linux):**

```bash
#!/bin/bash

# Create conda environment
conda create -n eeg_ad python=3.10 -y

# Activate environment
source activate eeg_ad

# Install requirements
pip install --upgrade pip setuptools wheel

# Core libraries
pip install numpy pandas scipy scikit-learn matplotlib seaborn

# EEG processing
pip install mne pyeeg PyWavelets

# Machine Learning
pip install xgboost lightgbm

# Deep Learning
pip install tensorflow torch

# Development tools
pip install jupyter notebook jupyterlab

# Web framework
pip install flask fastapi uvicorn

echo "Environment setup complete!"
echo "To activate: conda activate eeg_ad"
```

**setup_environment.bat (for Windows):**

```batch
@echo off
REM Create conda environment
conda create -n eeg_ad python=3.10 -y

REM Activate environment
call conda activate eeg_ad

REM Install requirements
pip install --upgrade pip setuptools wheel

REM Install all packages
pip install numpy pandas scipy scikit-learn matplotlib seaborn mne PyWavelets xgboost lightgbm tensorflow torch jupyter notebook jupyterlab flask fastapi uvicorn

echo Environment setup complete!
echo To activate: conda activate eeg_ad
pause
```

---

## 3.8 Verify Installation

### 3.8.1 Test Script

**test_installation.py:**

```python
#!/usr/bin/env python3
"""Test all required libraries"""

import sys

print("Testing Python Environment...")
print(f"Python Version: {sys.version}")

# Test core libraries
try:
    import numpy as np
    print("✓ NumPy:", np.__version__)
except ImportError as e:
    print("✗ NumPy:", str(e))

try:
    import pandas as pd
    print("✓ Pandas:", pd.__version__)
except ImportError as e:
    print("✗ Pandas:", str(e))

try:
    import scipy
    print("✓ SciPy:", scipy.__version__)
except ImportError as e:
    print("✗ SciPy:", str(e))

try:
    from sklearn import __version__
    print("✓ Scikit-learn:", __version__)
except ImportError as e:
    print("✗ Scikit-learn:", str(e))

try:
    import matplotlib
    print("✓ Matplotlib:", matplotlib.__version__)
except ImportError as e:
    print("✗ Matplotlib:", str(e))

try:
    import mne
    print("✓ MNE-Python:", mne.__version__)
except ImportError as e:
    print("✗ MNE-Python:", str(e))

try:
    import tensorflow as tf
    print("✓ TensorFlow:", tf.__version__)
except ImportError as e:
    print("✗ TensorFlow:", str(e))

try:
    import torch
    print("✓ PyTorch:", torch.__version__)
    print("  CUDA available:", torch.cuda.is_available())
    if torch.cuda.is_available():
        print("  GPU:", torch.cuda.get_device_name(0))
except ImportError as e:
    print("✗ PyTorch:", str(e))

try:
    import xgboost as xgb
    print("✓ XGBoost:", xgb.__version__)
except ImportError as e:
    print("✗ XGBoost:", str(e))

print("\n✓ Installation test complete!")
```

**Run test:**
```bash
python test_installation.py
```

---

**Next: Chapter 4 - Dataset Collection**