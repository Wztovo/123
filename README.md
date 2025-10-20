# Dual-Source Metric-Based Multi-Client Membership Inference Attack (DSM-MIA)

Official implementation of the paper:  
**"Dual-Source Metric-Based Multi-Client Membership Inference Attack in Federated Learning"**

[[Paper]](https://arxiv.org/abs/xxxx.xxxxx) | [[Project Page]](https://github.com/yourname/DSM-MIA)

---

## 🌟 Overview
This repository provides the official implementation of **DSM-MIA**, a novel membership inference attack designed for **federated learning (FL)**.  
Unlike traditional MIAs that only determine whether a sample was used in training, DSM-MIA **identifies which specific client** in FL owns the sample.

<p align="center">
  <img src="assets/framework.png" width="700"/>
</p>

---

## 🧩 Key Features
- ✅ Dual-source metric construction (global + local model metrics)  
- 🔄 Time-series modeling via RNN/Transformer with attention  
- 🧮 Multi-class attack (member + client attribution)  
- 📈 Comprehensive evaluation across datasets and baselines  

---

## ⚙️ Environment Setup

```bash
conda create -n dsm-mia python=3.9
conda activate dsm-mia
pip install -r requirements.txt

### 🧩 Main Dependencies
- **PyTorch** >= 1.13  
- **NumPy**, **pandas**, **matplotlib**, **seaborn**  
- **scikit-learn**, **tqdm**

