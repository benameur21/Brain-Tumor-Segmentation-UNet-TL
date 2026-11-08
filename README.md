# 🧠 Brain Tumor Segmentation with U-Net

**🔬 Computer Vision | 🤖 Deep Learning | Transfer Learning**

## 📌 Overview

This project focuses on brain MRI segmentation using a U-Net architecture with a pretrained ResNet34 encoder.

The objective is to identify FLAIR abnormalities associated with Low-Grade Gliomas (LGG) and generate binary segmentation masks.

The project explores two approaches:

- **Baseline:** Train the U-Net decoder while keeping the ResNet34 encoder frozen.
- **Partial Fine-Tuning:** Unfreeze the final encoder block (`layer4`) and fine-tune it alongside the decoder to investigate potential performance improvements.

## 📂 Dataset

**LGG MRI Segmentation** – [Kaggle Dataset](https://www.kaggle.com/datasets/mateuszbuda/lgg-mri-segmentation)

- 🖼️ 7,858 MRI images and corresponding masks.
- 👥 110 patients.
- 📐 Original image resolution: 256 × 256.
- 🎯 Binary segmentation: background (0) and annotated region (1).

Data is split at the patient level to prevent data leakage.

## ⚙️ Methodology

1. Dataset exploration and preprocessing.
2. Patient-level data splitting.
3. U-Net implementation with ImageNet-pretrained ResNet34.
4. Baseline training with a frozen encoder.
5. Partial fine-tuning of the final encoder block.
6. Evaluation using Dice Score and IoU.
7. Visualization and comparison of segmentation predictions.

## 🏗️ Model Configuration

| Parameter | Value |
|---|---|
| Architecture | U-Net |
| Encoder | ResNet34 |
| Pretrained weights | ImageNet |
| Input size | 224 × 224 |
| Input channels | 3 |
| Output channels | 1 |
| Loss | BCE + Soft Dice Loss |
| Optimizer | Adam / AdamW |
| Threshold | 0.5 |

## 🛠️ Technologies

Python · PyTorch · Segmentation Models PyTorch · NumPy · Matplotlib · scikit-learn · Google Colab

## 📁 Repository Structure

```text
Brain-Tumor-Segmentation/
│
├── notebooks/
│   └── brain_tumor_segmentation.ipynb
│
├── README.md
```

## 📊 Results

Baseline and partial fine-tuning results are compared using:

- 📉 Validation Loss
- 🎯 Dice Score
- 📐 Intersection over Union (IoU)
- 🖼️ Qualitative comparison of predicted masks

*Results are documented in the notebook.*

## 👤 Author

**Islem Ben Ameur**

⚠️ **Note:** This project is developed for educational purposes and is not intended for clinical diagnosis.


