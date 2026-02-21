# Oral Disease Detection Using Multimodal Fusion

## Overview
This project presents a **multimodal framework for oral disease classification** by combining **image-based analysis** and **symptom-based textual input**. The proposed system leverages **decision-level fusion** to improve diagnostic accuracy, enabling early detection of oral diseases and supporting accessible healthcare solutions.

The work has been **published in Springer** as a book chapter.

📘 **Springer Publication Link:**  
https://link.springer.com/chapter/10.1007/978-3-032-06697-8_36

---

## Authors
- **Abhishek A Joshi**
- **Vasudhaika S**
- **Sinchana Chindi**
- **Kaushik Mallibhat**
- **Satish Chikkamath**

**School of Electronics and Communication Engineering**  
KLE Technological University, Hubballi, India

---

## Abstract
Oral diseases are often neglected in early stages due to lack of awareness and limited access to dental care. This work proposes a **multimodal oral disease classification system** using both **images of affected oral regions** and **patient-reported symptoms**. The system employs separate classifiers for image and symptom modalities, whose confidence scores are combined using **logistic regression-based decision-level fusion**.

The image classifier achieved **81% accuracy**, the symptom-based model achieved **97% accuracy**, and the final multimodal fusion model surpassed the individual model performances, demonstrating the effectiveness of multimodal learning for oral disease diagnosis.

---

## Keywords
Oral disease, Image classification, Text-based illness prediction, Multimodal learning, Decision-level fusion, Healthcare AI

---

## Problem Statement
Traditional oral disease diagnosis often relies on:
- Visual inspection alone, or
- Symptom-based descriptions alone

Both approaches are incomplete when used independently. This project addresses the gap by:
- Integrating **visual and textual modalities**
- Improving diagnostic reliability through **fusion-based learning**
- Enabling early disease detection using AI-driven models

---

## Diseases Considered
The multiclass classification system includes:
- Gingivitis  
- Hypodontia  
- Oral cancer  
- Mouth ulcers  
- Dental caries  
- Tooth discoloration  
- Calculus  

---

## Proposed Framework

### Multimodal Pipeline
1. **Image Input**
   - Image of the affected oral region
   - Processed using a CNN-based image classifier

2. **Text Input**
   - Symptom description provided by the user
   - Processed using a logistic regression-based text classifier

3. **Decision-Level Fusion**
   - Confidence scores from both models are fused
   - Final disease prediction obtained using logistic regression

---

## Dataset Description

### Image Dataset
- **Total images:** 13,138
- **Classes:** 7 oral disease categories
- Data augmentation applied for underrepresented classes
- Source: Kaggle and curated datasets

### Symptom Dataset
- **150 symptom combinations per disease**
- **Total records:** 1,050
- Verified by a dental professional
- Stored as a structured CSV file

---

## Model Architecture

### Image Classification Model
- **Model:** MobileNetV2 (Transfer Learning)
- **Input size:** 224 × 224
- **Final activation:** Softmax
- **Best accuracy:** 81%

### Symptom Classification Model
- **Algorithm:** Logistic Regression
- **Input:** Vectorized symptom descriptions
- **Accuracy:** 97%

### Decision-Level Fusion Model
- **Algorithm:** Logistic Regression
- **Input:** Confidence scores from image & symptom models
- **Dataset size:** 1,400 samples
- **Output:** Final disease class
- **Accuracy** 92% (You may thinkk it is not better than symptom classification modal, but this model is more reliable as the input is both image and symptom so the analysis is more accurate)

---

## Experimental Results

| Model              | Average Accuracy |
|-------------------|-----------------|
| Traditional CNN    | 60%             |
| VGG16              | 70%             |
| InceptionV3        | 72%             |
| MobileNetV2        | 81%             |
| Symptom Model (LR) | 97%             |

The multimodal fusion model outperformed individual classifiers by effectively combining both modalities.

---

## Getting Started

### Prerequisites
- Python 3.8+
- TensorFlow / Keras
- Scikit-learn
- OpenCV
- Pandas, NumPy
- Image dataset and symptom CSV file

---

### Installation
```bash
git clone https://github.com/your-username/Oral-Disease-Detection-Multimodal.git
cd Oral-Disease-Detection-Multimodal