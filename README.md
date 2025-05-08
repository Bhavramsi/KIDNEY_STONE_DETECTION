
---

# Kidney Stone Detection Using Image Segmentation (YOLOv8)

This repository contains the implementation of an **image segmentation model** based on **YOLOv8** for accurate and efficient detection of kidney stones from CT scan images. The project uses annotated datasets, deep learning techniques, and a graphical interface for seamless integration into diagnostic workflows.

---

## Table of Contents

* [Overview](#overview)
* [Problem Statement](#problem-statement)
* [Project Objectives](#project-objectives)
* [Methodology](#methodology)
* [Model Performance](#model-performance)
* [Tools & Technologies](#tools--technologies)
* [Results](#results)
* [Applications](#applications)
* [Limitations & Future Work](#limitations--future-work)
* [How to Run](#how-to-run)
* [References](#references)

---

##  Overview

Over **115 million** people globally suffer from kidney stones. Early and accurate detection through imaging can prevent complications like renal failure. This project applies **deep learning (YOLOv8)** to CT scan images, aiming to automate and improve kidney stone detection using **instance segmentation** techniques.

---

## ❗ Problem Statement

Manual identification of kidney stones in CT scans is time-consuming and prone to human error. The goal is to develop an automated tool using deep learning that ensures **high precision**, **fast diagnosis**, and **detailed localization** of kidney stones.

---

## 🎯 Project Objectives

* Detect and segment kidney stones from CT scans using YOLOv8.
* Build a GUI for uploading images and displaying detection results.
* Achieve high accuracy using annotated datasets and robust preprocessing.

---

## 🧬 Methodology

1. **Dataset Preparation**:

   * 2300 CT scan images collected and annotated.
   * Expanded to 5200 images using augmentation techniques.

2. **Annotation**:

   * Instance segmentation using **Roboflow**.

3. **Preprocessing**:

   * Resizing (640×640), de-blurring (Weiner deconvolution), and noise filtering.

4. **Training**:

   * YOLOv8 model trained using Google Colab with GPU support.
   * Evaluated using precision, recall, F1 score, and confusion matrix.

5. **Detection Interface**:

   * GUI created in Google Colab using `ipywidgets`.

---

## 📊 Model Performance

| Metric    | Value  |
| --------- | ------ |
| Precision | 97.7%  |
| Recall    | 98.45% |
| F1 Score  | 97%    |
| mAP\@0.5  | 90%    |

YOLOv8 significantly outperformed previous architectures such as YOLOv5 and YOLOv7 Tiny.

---

## 🛠️ Tools & Technologies

* **YOLOv8** (Ultralytics)
* **Python**, **Google Colab**, **Matplotlib**
* **Roboflow** (annotation, preprocessing)
* **ipywidgets** (GUI creation)
* **GitHub** (version control)

---

## 📸 Results

* Kidney stones successfully detected and segmented in test/validation CT images.
* GUI allows uploading new CT scans and returns annotated outputs with bounding boxes.

<p align="center">
  <img src="https://user-images.githubusercontent.com/example-kidney-stone-output.png" width="600"/>
</p>

---

## 🩺 Applications

* **Clinical Diagnosis**: Assists radiologists with rapid, accurate detection.
* **Treatment Planning**: Identifies size, location, and count of stones.
* **Medical Education**: Helps train healthcare professionals with real CT data.

---

## ⚠️ Limitations & Future Work

### Limitations:

* Model depends on large, annotated datasets.
* Integration with real hospital systems requires additional work and compliance.

### Future Enhancements:

* Expand dataset with more diverse samples.
* Improve GUI into a full-fledged application.
* Comply with regulatory and ethical standards for deployment in clinical settings.

---

## 🚀 How to Run

1. Clone the repository:

   ```bash
   git clone https://github.com/yourusername/kidney-stone-segmentation.git
   cd kidney-stone-segmentation
   ```

2. Open `kidney_stone_detection.ipynb` on Google Colab.

3. Install dependencies:

   ```bash
   !pip install ipywidgets ultralytics==8.0.196 roboflow
   ```

4. Annotate your dataset on Roboflow and download in YOLOv8 format.

5. Set up training using the GUI:

   * Enter path to `data.yaml`
   * Choose number of epochs
   * Click `Train Model`

6. Upload CT scan images for testing.

---

## 📚 References

* [YOLOv8 - Ultralytics](https://docs.ultralytics.com/)
* [Roboflow](https://app.roboflow.com/)
* [Kidney CT Dataset - Kaggle](https://www.kaggle.com/datasets/nazmul0087/ct-kidney-dataset-normal-cyst-tumor-and-stone)
* [Research Papers](#refer-to-your-project-report)

---

Let me know if you want a logo/banner for the repo or a `requirements.txt` to go with this.
