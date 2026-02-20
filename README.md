# 🛠️ Integration and Comparison of vision models for smart inspection cell


This repository contains the implementation and evaluation of a **deep learning–based computer vision system** for automated surface defect inspection of automotive spur gears. The project focuses on detecting and classifying common manufacturing defects using **YOLOv8** and **MobileNetV2**, with an emphasis on **accuracy, robustness, and inference latency**.

---

## 📌 Project Overview

Surface defects such as **scratches, dents, cracks, and pitting** can significantly affect the reliability of automotive spur gears. Traditional inspection methods are often subjective and difficult to scale. This project explores a **data-driven vision-based approach** using deep learning models to automate defect inspection and evaluate their feasibility for industrial deployment.

---

## 🎯 Project Objectives

- Train **YOLOv8** for defect detection and localization  
- Train **MobileNetV2** for lightweight image-level defect classification
- Build a simulation setup in RoboDK for process control
- Integrate trained models for defect classification and localization
- Compare both models using real-time industrial performance metrics  
- Measure inference latency and runtime behavior  
- Assess feasibility for real-world inspection scenarios  

---

## 📂 Dataset Generation Pipeline

The dataset used in this project is **synthetically generated** to overcome the lack of publicly available spur gear defect datasets.

**Workflow:**
1. Spur Gear CAD Modeling (CATIA – defect-free geometry)  
2. Defect Modeling (Onshape – scratch, dent, crack, pitting)  
3. Synthetic Image Generation (multiple views, lighting, orientations)  
4. Manual Annotation (LabelImg – YOLO `.txt` format)  
5. Dataset Split (Train / Validation / Test)

---

## 🧠 Models Used

### 🔹 YOLOv8 (Object Detection)
- Task: Defect detection and localization  
- Input size: 640 × 640  
- Metrics: Precision, Recall, F1-score, mAP@50, mAP@50–95  

### 🔹 MobileNetV2 (Image Classification)
- Task: Component-level defect classification  
- Input size: 224 × 224  
- Metrics: Accuracy, Precision, Recall, F1-score  

---

## 📊 Evaluation Metrics

The models are evaluated using the following metrics:

- **Accuracy** – Overall correctness of predictions  
- **Precision** – Correct defect detections among predicted defects  
- **Recall** – Ability to detect all actual defects  
- **F1-score** – Balance between precision and recall  
- **mAP@50 / mAP@50–95** – Localization performance (YOLOv8)  
- **Inference Latency** – Time required for single-image inference  
- **Throughput** – Number of components inspected per unit time  

---


---

## 🧪 Experimental Setup
- Simulation tool: RoboDK
- Platform: Google Colab  
- GPU: NVIDIA Tesla T4  
- Frameworks: PyTorch, Ultralytics YOLOv8  
- Batch size: 1
- <img width="1918" height="999" alt="Screenshot from 2026-02-20 13-33-54" src="https://github.com/user-attachments/assets/21bf7f5b-ebd2-43db-86d0-f53574edc143" />




### 1️⃣ Clone the repository
```bash
git clone https://github.com/Sai99897/Integration-and-Comparison-of-vision-models-for-smart-inspection-cell.git
cd Integration-and-Comparison-of-vision-models-for-smart-inspection-cell 








