# Deep Learning Laboratory – Crop Disease Detection

An advanced Deep Learning project focused on **real-world crop disease detection using transfer learning and computer vision**.
This repository demonstrates how pretrained CNN architectures perform under both **controlled laboratory datasets** and **real-world agricultural conditions**.

Unlike many academic implementations that evaluate only on ideal datasets, this project analyzes the **generalization capability** of deep learning models using both **PlantVillage** and **PlantSeg** datasets. 

---

## Project Overview

Crop diseases significantly reduce agricultural productivity and farmer income. Traditional disease identification methods rely heavily on human expertise and manual inspection, which are time-consuming and often inaccurate under real farming conditions.

This project proposes an **AI-powered automated crop disease detection system** using pretrained Convolutional Neural Networks (CNNs) capable of identifying plant diseases from leaf images.

The study particularly focuses on:

* Evaluating model performance on controlled datasets
* Testing robustness on real-world field images
* Comparing lightweight and deep architectures
* Understanding the gap between laboratory accuracy and field deployment

---

## Key Highlights

* Transfer Learning based Deep Learning models
* Real-world generalization analysis
* Comparison between controlled and field datasets
* Lightweight mobile-friendly architecture evaluation
* Comparative performance study
* Practical agriculture-focused AI implementation

---

# Models Implemented

The following pretrained CNN architectures were implemented and evaluated:

| Model           | Purpose                              |
| --------------- | ------------------------------------ |
| **VGG16**       | Transfer learning baseline model     |
| **ResNet50**    | Deep residual learning               |
| **DenseNet121** | Dense feature reuse architecture     |
| **MobileNetV2** | Lightweight mobile-efficient network |

Traditional Machine Learning models were also analyzed:

* Support Vector Machine (SVM)
* K-Nearest Neighbors (KNN)

---

# Datasets Used

## 1. PlantVillage Dataset

A controlled laboratory dataset containing:

* ~54,000+ RGB leaf images
* 14 crop species
* 38 disease categories
* Plain backgrounds and uniform lighting

Used primarily for baseline training and benchmarking.

---

## 2. PlantSeg Dataset (Zenodo)

A real-world agricultural dataset containing:

* ~19,000+ field images
* 34 plant species
* 115 disease classes
* Natural environmental conditions
* Background clutter and lighting variations

Used to evaluate model robustness and generalization capability.

---

# Problem Statement

Most existing crop disease detection systems achieve extremely high accuracy on laboratory datasets but fail under practical agricultural environments due to:

* Complex backgrounds
* Illumination variations
* Occlusions and overlapping leaves
* Environmental noise
* Real-world image inconsistencies

This project aims to bridge the gap between:

> **Controlled Dataset Accuracy**
> and
> **Real-World Deployment Performance**

---

# Methodology

## Data Preprocessing

* Image resizing to 224×224
* Pixel normalization
* Dataset splitting
* Batch loading
* Transfer learning pipeline

## Training Strategy

Two-stage transfer learning approach:

### Stage 1 – Feature Extraction

* Frozen pretrained backbone
* Classification head training

### Stage 2 – Fine-Tuning

* Partial network unfreezing
* Low learning-rate optimization

---

# Performance Results

## Accuracy on PlantVillage Dataset

| Model       | Accuracy   |
| ----------- | ---------- |
| MobileNetV2 | **99.52%** |
| ResNet50    | 99.04%     |
| DenseNet121 | 94.00%     |
| VGG16       | 98.90%     |

---

## Accuracy on PlantSeg Dataset

| Model       | Accuracy   |
| ----------- | ---------- |
| DenseNet121 | **73.46%** |
| ResNet50    | 71.81%     |
| MobileNetV2 | 69.32%     |

---

# Major Observation

Although the models achieved near-perfect accuracy on PlantVillage, performance dropped significantly on PlantSeg.

This demonstrates that:

* High laboratory accuracy does not guarantee real-world performance
* Controlled datasets alone are insufficient for deployment-ready AI systems
* Real agricultural environments remain a major challenge for computer vision models

---

# Research Contributions

This project contributes by:

* Performing cross-dataset evaluation
* Studying real-world generalization
* Comparing lightweight vs deep architectures
* Evaluating deployment feasibility for agriculture applications

---

# Technologies Used

* Python
* TensorFlow
* Keras
* NumPy
* Pandas
* Matplotlib
* OpenCV
* Scikit-learn

---

# Repository Contents

```bash
Deep-Learning-Laboratory/
│
├── MobileNetV2.h5
├── README.md
│
├── Results/
│   ├── Accuracy Graphs
│   ├── Loss Graphs
│   ├── Confusion Matrices
│
├── Reports/
│   ├── Project Report
│   ├── Presentation PPT
│
└── Dataset Information
```

---

# Why Only `.h5` Model File is Uploaded?

The repository intentionally includes only the trained `.h5` model file to:

* Protect implementation privacy
* Avoid unnecessary exposure of proprietary training pipelines
* Reduce repository size
* Share deployable trained weights instead of full source implementation

The focus of this repository is on:

* Research findings
* Experimental analysis
* Model performance
* Real-world evaluation insights

---

# Future Enhancements

Future improvements may include:

* Mobile application deployment
* Real-time disease detection
* Edge-device optimization
* IoT-based smart agriculture integration
* Transformer-based hybrid architectures
* Larger field dataset training
* Disease severity estimation

---

# Conclusion

This project demonstrates the effectiveness of Deep Learning in automated crop disease detection while also highlighting the critical challenge of real-world generalization.

The experimental analysis proves that:

* Transfer learning significantly improves crop disease classification
* Lightweight architectures can support mobile deployment
* Real-world agricultural datasets are essential for practical AI systems

The work establishes a strong foundation for future research in:

* Precision agriculture
* Smart farming
* AI-assisted crop monitoring
* Field-deployable disease detection systems

---

# Academic Report & Presentation

Project report and presentation used for this research:



---

# Authors

* K. Bala Sai
* K. Neha
* S. Sri Krishna Teja
* B. Maithreyi

Under the guidance of:

**Dr. Eva Patel**
Associate Professor
Department of Advanced Computer Science and Engineering
Vignan’s Foundation for Science, Technology & Research

---

# License

This repository is intended for:

* Academic learning
* Educational research
* Non-commercial use only
