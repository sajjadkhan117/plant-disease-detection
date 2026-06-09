<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,12,20&height=200&section=header&text=Plant%20Disease%20Detector&fontSize=40&fontColor=fff&animation=fadeIn&fontAlignY=35&desc=Real-Time%20Detection%20%7C%20Classical%20DIP%20%7C%20Flask%20Web%20App&descAlignY=58&descSize=16" width="100%"/>

<br/>

[![Python](https://img.shields.io/badge/Python-3.9+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![Flask](https://img.shields.io/badge/Flask-3.0+-000000?style=for-the-badge&logo=flask&logoColor=white)](https://flask.palletsprojects.com)
[![OpenCV](https://img.shields.io/badge/OpenCV-4.8+-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white)](https://opencv.org)
[![License](https://img.shields.io/badge/License-MIT-27ae60?style=for-the-badge)](LICENSE)
[![University](https://img.shields.io/badge/PAF--IAST-Haripur-2c3e50?style=for-the-badge)](https://pafkiet.edu.pk)

<br/>

**Upload a real leaf photo → AI detects disease instantly**  
*No machine learning training required — pure classical image processing*

</div>

---

## 🌿 Live Demo

```bash
# 1. Install
pip install -r requirements.txt

# 2. Run
python app.py

# 3. Open browser
http://localhost:5000
```

> Upload any leaf photo from your phone or camera — results in seconds!

---

## ✨ Features

<div align="center">

| 🔍 Detection | 📊 Metrics | 🏷️ Classification | 💊 Treatment |
|:---:|:---:|:---:|:---:|
| HSV Colour Masking | PDI Score | 4 Severity Grades | Instant Advice |
| Morphological Ops | PSNR & SSIM | Healthy to Severe | Crop-Specific |
| Canny Edge Detection | Lesion Count | Real-time | Evidence-Based |

</div>

---

## 🔬 Pipeline Architecture

```
📸 Input Leaf Photo
        │
        ▼
┌────────────────────────────────────────────────────┐
│  S1  Background Removal     Lab 02 - Color Spaces  │
│  S2  CLAHE Enhancement      Lab 05 - Histogram     │
│  S3  HSV Disease Masking    Lab 02+03 - Math Ops   │
│  S4  Canny Edge Detection   Lab 07 - Edges         │
│  S5  Morphological Ops      Lab 11 - Morphology    │
│  S6  PDI + Classification   Lab 12 - Segmentation  │
└────────────────────────────────────────────────────┘
        │
        ▼
📊 Severity Class + PDI% + Treatment Advice + 4 Stage Images
```

---

## 🎯 Severity Classification

<div align="center">

| Class | PDI Range | Status | Action |
|:---:|:---:|:---:|:---:|
| 🟢 **Healthy** | 0 – 5% | No disease | Keep it up! |
| 🟡 **Mild** | 5 – 20% | Early stage | Early intervention |
| 🟠 **Moderate** | 20 – 50% | Significant | Prompt treatment |
| 🔴 **Severe** | > 50% | Heavy infection | Immediate action |

</div>

---

## ✅ CCP Criteria Fulfilled

<div align="center">

| Criterion | Implementation |
|:---:|:---|
| **C1** Knowledge | Labs 02, 03, 05, 07, 11, 12 — all integrated |
| **C2** Analysis | PDI, PSNR, SSIM, Confusion Matrix, Precision/Recall |
| **C3** Conflicts | Morphological kernel k=5 via trade-off curve |
| **C4** Familiarity | CLAHE handles variable lighting & backgrounds |
| **C5** Standards | Plant Disease Index (PDI) — agronomic standard |
| **C6** Context | Crop-specific HSV thresholds per disease type |

</div>

---

## 🛠️ Tech Stack

<div align="center">

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)

</div>

---

## 📁 Project Structure

```
plant-disease-detection/
│
├── 📓 COMP342L_P06_PlantDiseaseDetection.ipynb  ← Main notebook
├── 🐍 app.py                                     ← Flask web app
├── 📁 templates/
│   └── index.html                                ← Web interface
├── 📁 static/uploads/                            ← Uploaded images
├── 📁 outputs/                                   ← Pipeline figures
└── 📋 requirements.txt
```

---

## 📈 Results

```
Images Processed   : 50
Mean PDI           : 22.4%
Mean PSNR          : 32.1 dB  ✅ (≥ 30 dB)
Mean SSIM          : 0.9912   ✅ (≥ 0.85)
Mean Lesion Count  : 14.3
Overall Accuracy   : 88.0%
```

---

<div align="center">

**👨‍💻 Sajjad Khan** · [github.com/sajjadkhan117](https://github.com/sajjadkhan117)  
COMP-342L Digital Image Processing · PAF-IAST · Spring 2025

⭐ **Star this repo if it helped you!** ⭐

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,12,20&height=100&section=footer" width="100%"/>

</div>
