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
```
### 🧩 Main Dependencies
- PyTorch >= 1.13  
- NumPy, pandas, matplotlib, seaborn  
- scikit-learn, tqdm

##📂 Project Structure
```bash
DSM-MIA/
│
├── src/
│   ├── train_attack_model.py      # RNN/Transformer-based attack model
│   ├── feature_extraction.py      # Construct dual-source metric sequences
│   ├── utils.py                   # Helper functions
│
├── draw_pict/                     # Visualization scripts
├── saved_mia_models/              # Trained attack models
├── evaluate/                      # Evaluation results
├── requirements.txt
└── README.md
```
##🚀 Quick Start

###1️⃣ Train a target federated model
```bash
python train_fed_model.py --dataset cifar10 --model resnet18 --n_clients 5
```
###2️⃣ Extract dual-source metrics
```bash
python feature_extraction.py --dataset cifar10 --rounds 60
```
###3️⃣ Train the attack model
```bash
python train_attack_model.py --model RNN_Attention --epochs 50
```
###4️⃣ Evaluate attacks
```bash
python attack_comparison.py --metric AUC --save_fig True
```
##📊 Results
Dataset	Model	Attack	AUC	TPR@FPR=0.001
CIFAR-10	ResNet-18	DSM-MIA	0.874	0.523
CIFAR-100	ResNet-18	DSM-MIA	0.812	0.465
##📚 Citation

If you find our work helpful, please cite:

@article{yourname2025dsmmia,
  title={Dual-Source Metric-Based Multi-Client Membership Inference Attack in Federated Learning},
  author={Your Name and ...},
  journal={arXiv preprint arXiv:xxxx.xxxxx},
  year={2025}
}

##💡 Contact

If you have questions or issues, please open an issue or contact:
##📧 your.email@domain.com

##📜 License

This project is licensed under the MIT License.
