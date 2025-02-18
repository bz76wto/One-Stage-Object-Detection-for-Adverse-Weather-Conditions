# One-Stage-Object-Detection-for-Adverse-Weather-Conditions

![](https://img.shields.io/badge/Update-News-blue.svg?style=plastic)

## Overview
This repository focuses on improving **one-stage object detection** in real-world **adverse weather conditions** using **YOLOv5**. The goal is to enhance detection accuracy, robustness, and efficiency in low-visibility environments, critical for **autonomous vehicles** and **traffic safety applications**.

## 🚀 Key Contributions
- **Enhanced YOLOv5 Framework:** Incorporates multiple lightweight **backbones** (ShuffleNetV2, GhostNet, MobileNetv3-Small, VoVNet) for improved efficiency.
- **Advanced Attention Mechanisms:** Integrates **SE Block, CBAM Block, and ECA Block** to refine feature extraction.
- **Improved Object Localization:** Introduces **Transformer Prediction Heads (TPH)** to enhance detection in densely populated scenes.
- **Pruning & Quantization:** Optimizes YOLOv5 for faster inference and lower computational cost, making it practical for real-world deployment.
- **Superior Detection in Adverse Weather:** Achieves **99.1% mAP (IoU 0.5)** on weather-adverse datasets, surpassing previous benchmarks.

---

## 📌 One-Stage Object Detection Enhancements
### 1️⃣ Multi-Backbone YOLOv5
| Model                    | mAP@50 | Parameters (M) | GFLOPs |
|--------------------------|--------|---------------|--------|
| YOLOv5n                 | 26.2   | 1.78          | 4.2    |
| YOLOv5s                 | 34.0   | 7.05          | 15.9   |
| YOLOv5x                 | 40.8   | 86.28         | 204.4  |
| **YOLOv5x-TPH (ours)**  | **63.0** | **112.97**    | **270.8**  |

### 2️⃣ Attention-Based Enhancements
| Mechanism | Purpose |
|-----------|---------|
| **SE Block** | Enhances channel-wise feature selection |
| **CBAM Block** | Incorporates spatial and channel attention for improved detection |
| **ECA Block** | Refines convolutional feature aggregation |

### 3️⃣ Pruning & Quantization Results
| Model                | mAP@50 | Parameters (M) | GFLOPs |
|----------------------|--------|---------------|--------|
| YOLOv5s             | 34.0   | 7.05          | 15.9   |
| YOLOv5s-EagleEye@0.6 | 27.9   | 4.59          | 9.6    |

---

## 📂 Installation
```bash
pip install -r requirements.txt
```

## 🏋️‍♂️ Training & Evaluation
### Training
```bash
python train.py --data dataset.yaml --weights yolov5s.pt --cfg models/yolov5s.yaml --epochs 300 --batch-size 8 --img 640 --device 0,1
```
### Evaluation
```bash
python val.py --data dataset.yaml --weights best.pt --img 640 --device 0
```

---

## 📌 Research Background
This repository is based on **Claire Zhang’s Master’s Thesis** at the **University of Ottawa**, titled:
> **"Enhanced Safety of Autonomous Driving in Real-World Adverse Weather Conditions via Deep Learning-Based Object Detection."**

### 🔬 Research Highlights:
- **One-stage object detection optimization for adverse weather**
- **Lightweight backbone substitution for efficiency**
- **Attention-enhanced feature selection for improved accuracy**
- **Pruning and quantization to enable real-time deployment**

---

## 📄 Citation
If you find this work useful, please cite:
```
@article{zhang2024objectdetection,
  author    = {Biwei Zhang},
  title     = {Enhanced Safety of Autonomous Driving in Real-World Adverse Weather Conditions via Deep Learning-Based Object Detection},
  journal   = {University of Ottawa Thesis},
  year      = {2024}
}
```

---

## 🔗 Connect
- **GitHub:** [@catt07986](https://github.com/catt07986)
- **ORCID:** [0009-0009-7814-9861](https://orcid.org/0009-0009-7814-9861)

