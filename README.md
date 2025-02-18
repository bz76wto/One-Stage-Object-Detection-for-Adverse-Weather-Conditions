# Enhanced Safety of Autonomous Driving in Real-World Adverse Weather Conditions via Deep Learning-Based Object Detection

![](https://img.shields.io/badge/Update-News-blue.svg?style=plastic)

## Overview
This repository is based on **Claire Zhang’s Master’s Thesis** at the **University of Ottawa**, titled:
> **"Enhanced Safety of Autonomous Driving in Real-World Adverse Weather Conditions via Deep Learning-Based Object Detection."**

This research focuses on **one-stage object detection** and enhancing **YOLOv5** for improved performance in **adverse weather conditions**. The objective is to boost detection accuracy, robustness, and efficiency to ensure **safe autonomous driving** in challenging environments.

## 🚀 Key Contributions
- **Enhanced One-Stage Object Detection Framework**: Integration of **YOLOv5** with multiple lightweight backbones such as **ShuffleNetV2, GhostNet, MobileNetv3-Small, and VoVNet**.
- **Advanced Attention Mechanisms**: Incorporation of **SE Block, CBAM Block, and ECA Block** to improve feature selection and model interpretability.
- **Optimized Object Localization**: Introduction of **Transformer Prediction Heads (TPH)** to enhance detection of small and occluded objects in complex scenes.
- **Pruning & Quantization Techniques**: Model compression strategies for faster inference while maintaining high accuracy.
- **Superior Performance in Weather-Adverse Scenarios**: Achieved **99.1% mAP (IoU 0.5)**, significantly surpassing baseline models.

---

## 📌 One-Stage Object Detection Enhancements
### 1️⃣ Multi-Backbone YOLOv5 Performance
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
This research aims to **bridge the gap** between real-world **adverse weather conditions** and **deep learning-based object detection** for autonomous vehicles. 

### 🔬 Research Highlights:
- **Investigation of YOLOv5 and one-stage object detection techniques**.
- **Evaluation of various lightweight backbones for efficient computation**.
- **Improved detection in adverse weather using attention-based feature extraction**.
- **Application of pruning and quantization techniques for real-time deployment**.

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



