<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=12,20,6&height=160&section=header&text=Plant%20Disease%20Detection&fontSize=36&fontColor=fff&animation=fadeIn&fontAlignY=35&desc=Agricultural%20Monitoring%20System%20%7C%20COMP-342L%20Project%2006&descAlignY=58&descSize=14" width="100%"/>

<br/>

[![Python](https://img.shields.io/badge/Python-3.9+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![OpenCV](https://img.shields.io/badge/OpenCV-4.8+-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white)](https://opencv.org)
[![License](https://img.shields.io/badge/License-MIT-27ae60?style=for-the-badge)](LICENSE)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](notebooks/)
[![University](https://img.shields.io/badge/PAF--IAST-Haripur-2c3e50?style=for-the-badge)](https://pafkiet.edu.pk)

<br/>

**A complete end-to-end classical image processing pipeline that automatically detects,
quantifies, and classifies plant disease severity — zero machine learning required.**

</div>

---

## 📸 Results Preview

| Original Leaf | Disease Overlay | Severity Class |
|:---:|:---:|:---:|
| Raw leaf image | Red regions = disease | PDI-based grade |
| Pipeline processes | HSV masking + morphology | Healthy / Mild / Moderate / Severe |

---

## 🎯 Project Overview

This project was developed as part of **COMP-342L Digital Image Processing** at
**Pak-Austria Fachhochschule (Spring 2025)** under the supervision of **Ms. Sana Salim**.

It satisfies all **6 CCP (Complex Computing Problem) criteria** required for the semester project.

### What It Does
- 🔍 **Detects** disease regions using HSV colour masking
- 📏 **Quantifies** severity using the **Plant Disease Index (PDI)** standard
- 🏷️ **Classifies** each leaf into 4 grades: Healthy / Mild / Moderate / Severe
- 📊 **Evaluates** performance using PSNR, SSIM, Confusion Matrix, Precision/Recall
- 📈 **Generates** 9 publication-quality figures + auto PDF report

---

## ✅ CCP Criteria Fulfilled

| Criterion | How |
|-----------|-----|
| **C1 — Knowledge Required** | Labs 02, 03, 05, 07, 11, 12 all integrated |
| **C2 — Depth of Analysis** | PDI, PSNR, SSIM, Confusion Matrix, 5-config comparison table |
| **C3 — Conflicting Requirements** | Morphological kernel trade-off curve (noise removal vs lesion retention) |
| **C4 — Familiarity of Issues** | CLAHE + adaptive HSV handles variable lighting & backgrounds |
| **C5 — Applicable Standards** | Plant Disease Index (PDI) — agronomic standard |
| **C6 — Role of Context** | Crop-specific HSV thresholds (yellowing H=15-40, browning H=5-18) |

---

## 🔬 Pipeline Architecture

```
Input Leaf Image
      │
      ▼
┌─────────────────────────────────────────────────────────┐
│  S1  Background Removal    (Lab 02 - Color Spaces)      │
│  S2  CLAHE Normalisation   (Lab 05 - Histogram)         │
│  S3  HSV Disease Masking   (Lab 02+03 - Math Ops)       │
│  S4  Canny Edge Detection  (Lab 07 - Edge Detection)    │
│  S5  Morphological Ops     (Lab 11 - Morphology)        │
│  S6  Connected Components  (Lab 12 - Segmentation)      │
│  S7  PDI Computation       (Plant Disease Index)        │
│  S8  Severity Classification (4 grades)                 │
└─────────────────────────────────────────────────────────┘
      │
      ▼
Output: Severity Class + PDI + 9 Figures + PDF Report
```

---

## 📦 Installation & Usage

### Prerequisites
- Python 3.9+
- Anaconda (recommended) or pip

### Quickstart

```bash
# 1. Clone this repository
git clone https://github.com/sajjadkhan117/plant-disease-detection.git
cd plant-disease-detection

# 2. Install dependencies
pip install -r requirements.txt

# 3. Launch Jupyter Notebook
jupyter notebook

# 4. Open and run
#    notebooks/COMP342L_P06_PlantDiseaseDetection.ipynb
#    Kernel → Restart & Run All
```

> **No dataset download needed!** The notebook auto-generates 50 synthetic leaf images on first run.

---

## 📁 Repository Structure

```
plant-disease-detection/
│
├── 📓 notebooks/
│   └── COMP342L_P06_PlantDiseaseDetection.ipynb   ← Main notebook (run this)
│
├── 📊 outputs/                                     ← Auto-created on first run
│   ├── fig1_pipeline_walkthrough.png
│   ├── fig2_severity_overlay.png
│   ├── fig3_histogram.png
│   ├── fig4_batch_dashboard.png
│   ├── fig5_confusion_matrix.png
│   ├── fig6_severity_showcase.png
│   ├── fig7_tradeoff_analysis.png
│   ├── fig8_config_comparison.png
│   ├── fig9_disease_type_analysis.png
│   ├── results_table.csv
│   ├── pipeline_config_comparison.csv
│   ├── disease_type_breakdown.csv
│   ├── ccp_criteria_mapping.csv
│   └── Project06_Report.pdf                       ← Auto-generated PDF report
│
├── 📋 requirements.txt
└── 📖 README.md
```

---

## 📊 Severity Classification

| Class | PDI Range | Meaning | Action |
|-------|-----------|---------|--------|
| 🟢 **Healthy** | 0 – 5% | No disease detected | None required |
| 🟡 **Mild** | 5 – 20% | Early stage lesions | Early intervention |
| 🟠 **Moderate** | 20 – 50% | Significant infection | Prompt treatment |
| 🔴 **Severe** | > 50% | Heavy infection | Immediate action |

---

## 📚 Tools & Libraries

| Library | Version | Purpose |
|---------|---------|---------|
| `opencv-python` | ≥ 4.8 | Core image processing |
| `numpy` | ≥ 1.24 | Array operations |
| `matplotlib` | ≥ 3.7 | Visualizations |
| `pandas` | ≥ 2.0 | Data tables & CSV |
| `scikit-image` | ≥ 0.21 | Image metrics (SSIM) |
| `scikit-learn` | ≥ 1.3 | Confusion matrix |
| `reportlab` | ≥ 4.0 | PDF report generation |
| `tqdm` | ≥ 4.65 | Progress bars |

---

## 📈 Sample Results

```
Images Processed   : 50
Mean PDI           : 22.4%
Mean PSNR          : 32.1 dB   ✅ (threshold ≥ 30 dB)
Mean SSIM          : 0.9912    ✅ (threshold ≥ 0.85)
Mean Lesion Count  : 14.3
Overall Accuracy   : 88.0%

Severity Distribution:
  Healthy    ████████████  12 images
  Mild       ██████████████  14 images
  Moderate   ██████████████  14 images
  Severe     ██████████  10 images
```

---

## 👨‍🎓 Academic Info

| Field | Details |
|-------|---------|
| **Course** | COMP-342L Digital Image Processing |
| **Project** | P06 — Plant Disease Detection & Agricultural Monitoring |
| **Session** | Spring 2025 |
| **Lab Demonstrator** | Ms. Sana Salim |
| **University** | Pak-Austria Fachhochschule (PAF-IAST), Haripur |
| **Student** | Sajjad Khan |

---

<div align="center">

⭐ **If this project helped you, please give it a star!** ⭐

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=12,20,6&height=80&section=footer" width="100%"/>

</div>
