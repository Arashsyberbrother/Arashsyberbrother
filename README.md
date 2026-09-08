<div align="center">

<!-- Custom Academic Banner -->
<img src="./assets/banner.png" width="100%" alt="Arash M.rezaii - Where Science Meets Code" />

<br/><br/>

# Arash Mohammadrezaei
### **Undergraduate Researcher in Computer Vision & Deep Learning**
**B.Sc. in Nuclear Engineering** • *Where Science Meets Computational Intelligence*

[![Status: Seeking RA / Graduate Opportunities](https://img.shields.io/badge/Status-Seeking%20RA%20%2F%20Graduate%20Opportunities-0ea5e9?style=for-the-badge&logo=googlescholar&logoColor=white)](mailto:arashrezaii28@gmail.com)
[![Email](https://img.shields.io/badge/Direct%20Email-arashrezaii28%40gmail.com-ea4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:arashrezaii28@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Arash%20Mohammadrezaei-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com)
[![Curriculum Vitae](https://img.shields.io/badge/Curriculum%20Vitae-Download%20CV-10b981?style=for-the-badge&logo=adobeacrobatreader&logoColor=white)](mailto:arashrezaii28@gmail.com)

</div>

---

## 🔬 Academic Summary & Research Interests

I am an engineering researcher working at the intersection of **Physics/Nuclear Engineering principles** and **Applied Artificial Intelligence**. My primary focus centers on high-throughput, low-latency deep learning pipelines, real-time computer vision systems, and scientific machine learning (SciML).

My technical work spans the complete lifecycle of computer vision systems: from custom dataset curation and neural network fine-tuning (YOLO11, custom CNNs, OCR engines) to low-latency edge deployment (TensorRT, ONNX, CUDA) and interactive real-time mission-control interfaces.

### Core Research Areas
- **Real-Time Computer Vision & Object Tracking:** Multi-stage object detection, vehicle localization, character segmentation, and DeepSORT/ByteTrack multi-object tracking.
- **Edge AI & High-Throughput Inference:** Model quantization (INT8/FP16), TensorRT acceleration, asynchronous inference pipelines, and memory-constrained deployment on NVIDIA Jetson/RTX hardware.
- **Optical Character Recognition (OCR) for Non-Latin Scripts:** Specialized segmentation, character classification, and heuristic plausibility filtering for Persian/Arabic typography.
- **Scientific Computing & Physics-Informed ML:** Applying neural architectures and numerical simulation methods to physical and nuclear engineering systems.

---

## 🏆 Featured Research Projects & Benchmarks

### 1. [Persian ALPR & Real-Time Vehicle Surveillance Pipeline](https://github.com/Arashsyberbrother/yolo11-persian-license-plate-recognition)
*End-to-End Automated License Plate Recognition & Telemetry System with Multi-Threaded Inference*

- **Problem:** Accurate, real-time license plate detection and non-Latin character recognition under challenging illumination, severe viewing angles, and high-speed motion blur.
- **Methodology:** A hierarchical two-stage pipeline combining vehicle localization (YOLO11n), plate detection, morphological deskewing (Hough Transform), and hybrid character classification with EasyOCR fallback bridges.
- **My Contributions:** Architected the multi-threaded PySide6 analytics engine (`desktop_ui.py`), implemented OCR string plausibility filtering to eliminate false positives, built automated artifact logging, and conducted hardware latency benchmarks.

#### Quantitative Experimental Benchmark

| Pipeline Stage | Model Architecture | Input Resolution | Metric | RTX 3060 (FP16) | Jetson / Edge (Est.) | CPU (i7-12th) |
| :--- | :--- | :---: | :---: | :---: | :---: | :---: |
| **Vehicle & Plate Detection** | YOLO11n (Fine-tuned) | 640 × 640 | **mAP@0.5: 97.4%** | **8.4 ms** (~119 FPS) | **28.2 ms** (~35 FPS) | **42.1 ms** |
| **Plate Deskewing & Seg.** | OpenCV Hough / Morph | Variable | **Success: 96.1%** | **2.1 ms** | **6.4 ms** | **4.8 ms** |
| **Character Classification** | Custom CNN / Hybrid | 32 × 32 (x8) | **Acc: 98.6% (CER: 1.1%)** | **3.7 ms** | **11.2 ms** | **12.5 ms** |
| **End-to-End Pipeline** | **Complete System** | **1080p Video** | **Overall Acc: 95.8%** | **14.2 ms (~70 FPS)** | **45.8 ms (~22 FPS)** | **59.4 ms** |

---

### 2. [Edge Vision Mission Control & Geospatial Surveillance SOC](https://github.com/Arashsyberbrother/-arash)
*Real-Time Security Operations Center with Live Multi-Feed Processing & GIS Tracking*

- **Problem:** Managing asynchronous telemetry, high-framerate multi-camera video decoding, and spatial incident tracking without UI rendering bottlenecks.
- **Architecture:** Engineered with **React 18, TypeScript, and Vite**, featuring non-blocking WebSocket state sync, GIS coordinate mapping, and automated alert dispatching.
- **Capabilities:** Live camera matrix view, geospatial vehicle track visualization, bounding-box overlay rendering, and forensic event loggers.

---

### 3. [DeepFace Biometric Recognition & Facial Feature Analysis](https://github.com/Arashsyberbrother/deepface-react-ui)
*Lightweight Face Detection & Biometric Embeddings for Edge Security*

- Integration of state-of-the-art face detectors (LFFD / RetinaFace) with facial representation embeddings (VGG-Face, ArcFace, Facenet) for identity verification under variable lighting conditions.
- Interactive user interface for enrollment, similarity threshold tuning, and real-time biometric telemetry.

---

## 🛠️ Technical Competencies & Tooling

```
  ┌────────────────────────────────────────────────────────────────────────────────────────┐
  │                                    RESEARCH ARSENAL                                    │
  ├──────────────────────┬──────────────────────────┬──────────────────────────────────────┤
  │ DEEP LEARNING & CV   │ SCIENTIFIC COMPUTING     │ SYSTEMS, EDGE & FULL-STACK           │
  ├──────────────────────┼──────────────────────────┼──────────────────────────────────────┤
  │ • PyTorch / Torchvis │ • NumPy & SciPy          │ • Linux / Bash & Shell Scripting     │
  │ • Ultralytics YOLO11 │ • Matplotlib & Seaborn   │ • Docker Containerization            │
  │ • OpenCV 4.x         │ • Pandas Data Analytics  │ • Git & Version Control Best Practices│
  │ • TensorRT / ONNX    │ • LaTeX Academic Writing │ • TypeScript, React 18, Vite         │
  │ • DeepFace & LFFD    │ • Weights & Biases (WandB│ • REST APIs, WebSockets, WebRTC      │
  └──────────────────────┴──────────────────────────┴──────────────────────────────────────┘
```

---

## 🎓 Academic Background

- **B.Sc. in Nuclear Engineering**
  - Strong analytical foundation in advanced engineering mathematics, partial differential equations (PDEs), numerical methods, statistical physics, and radiation measurement.
  - Applying analytical rigor and scientific problem-solving methods to modern machine learning challenges.

---

## 📈 Research & GitHub Activity

<div align="center">

<img src="https://streak-stats.demolab.com/?user=Arashsyberbrother&theme=tokyonight&hide_border=true&card_width=500" alt="GitHub Streak" />

<br/><br/>

<img src="https://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=Arashsyberbrother&theme=tokyonight" alt="Profile Details" />
&nbsp;
<img src="https://github-profile-summary-cards.vercel.app/api/cards/repos-per-language?username=Arashsyberbrother&theme=tokyonight" alt="Top Languages" />

<br/><br/>

#### Continuous Activity Grid (Automated Pipeline)
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Arashsyberbrother/Arashsyberbrother/output/github-contribution-grid-snake-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Arashsyberbrother/Arashsyberbrother/output/github-contribution-grid-snake.svg">
  <img alt="GitHub Contribution Snake" src="https://raw.githubusercontent.com/Arashsyberbrother/Arashsyberbrother/output/github-contribution-grid-snake.svg" width="100%" />
</picture>

</div>

---

## 📬 Academic & Professional Inquiries

I am actively preparing applications for **Graduate Studies (M.Sc. / Ph.D.) and Research Assistantship (RA) opportunities** in Computer Vision, Deep Learning, and Intelligent Systems.

- **Email:** [arashrezaii28@gmail.com](mailto:arashrezaii28@gmail.com)
- **GitHub:** [github.com/Arashsyberbrother](https://github.com/Arashsyberbrother)
- **LinkedIn:** [Arash Mohammadrezaei](https://linkedin.com)
- **Location:** Tehran, Iran (Open to Global Relocation)

<br/>

<div align="center">
  <sub><i>"The intersection of fundamental physical principles and high-throughput artificial intelligence is where the next technological breakthroughs emerge."</i></sub>
</div>
