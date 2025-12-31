# Fetal Head Biometry — Deep Learning Pipelines (BPD & OFD)

This repository contains two complementary deep-learning pipelines developed for **fetal cranium biometry from ultrasound images**, focusing on automatic measurement of:

- **Biparietal Diameter (BPD)**
- **Occipitofrontal Diameter (OFD)**

The work explores and implements two approaches:

1. **Landmark-based detection using heatmap regression**
2. **Segmentation-based cranium extraction followed by ellipse-fitting**

Each task is organized as an independent research pipeline with code, model weights (external links), training/testing notebooks, and detailed reports.

---


---

## 🟢 Task-1 — Fetal Biometric Landmark Detection (Hourglass Model)

**Folder:** `task_1_landmark/`

This task focuses on detecting **four cranial anatomical landmarks** corresponding to BPD and OFD using a **Single-Hourglass CNN with Gaussian heatmap regression**.

### ✔️ What this pipeline includes

- Dataset preprocessing, scaling & augmentation
- Heatmap-based landmark supervision
- Multiple hypothesis experiments:
  - Single-Hourglass (final selected model)
  - Hybrid Heatmap + Coordinate Regression model
  - Stacked-Hourglass refinement model
- Evaluation based on localization stability & pixel-error behavior
- Final selection prioritizing **robustness and interpretability**

### 📂 Folder contents

- `Model Weights/` — model checkpoints (stored externally, links referenced)
- `Python Script/` — training & testing notebooks
- `Assets/` — dataset reference links
- `Report/` — detailed technical report
- `Readme.pdf` — folder-level documentation

---

## 🟣 Task-2 — Segmentation-Based Fetal Cranium Biometry (U-Net + Ellipse Fitting)

**Folder:** `task_1_segmentation/`

This task implements a **two-stage pipeline**:

1. **U-Net segmentation** — predict fetal cranium mask  
2. **Geometric measurement stage** — contour extraction → ellipse fitting → compute BPD & OFD axes

### ✔️ What this pipeline includes

- Mask preprocessing & morphology refinement
- Dice + BCE based segmentation training
- Experiments on
  - loss variations
  - resolution trade-offs
  - augmentation constraints
- Stable ellipse alignment and measurement consistency
- Interpretation-focused geometry-aware workflow

### 📂 Folder contents

- `Model Weights/` — final trained U-Net checkpoint (stored externally, link referenced)
- `Python Script/` — training & inference notebooks
- `Assets/` — dataset link file
- `Report/` — full segmentation & measurement study
- `Readme.pdf` — folder-level documentation

---

## 🎯 Project Objectives & Outcomes

Across both approaches, this work demonstrates:

- Comparative exploration of **landmark vs segmentation pipelines**
- Emphasis on **anatomical consistency & interpretability**
- Systematic experimentation and hypothesis evaluation
- Robust preprocessing and evaluation workflow
- Research-oriented deep-learning implementation

---

## 🚀 How to Use

Each task folder contains:

- Training notebook  
- Testing / inference notebook  
- Dataset reference link  
- Model weight reference  
- Technical report  

Run the **Tester notebook** in each task to reproduce evaluation results and visualizations.

> Note — Large `.pth` weight files are not stored in the repo.  
> External download links are provided instead for cleaner version control.

---

## 📝 Author

**Gogada Harsha Vardhan**  
Deep Learning & Computer Vision  
IIIT Kottayam

---

## 💡 Future Extensions (Planned / Exploratory)

- Segmentation-guided landmark refinement
- Uncertainty-aware prediction confidence
- Attention-based feature refinement
- Cross-dataset robustness evaluation

---

## 📌 License / Usage

This project is intended for **academic and research purposes**.


