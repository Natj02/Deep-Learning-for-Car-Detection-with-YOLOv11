# Deep Learning for Car Detection with YOLOv11

## Overview
This project implements a **YOLOv11**-based object detection model for **car detection in low-light conditions**.  
The model was fine-tuned on a custom low-light car dataset to improve detection performance in challenging environments.

---

## Model Architecture
We use the **Ultralytics YOLOv11** object detection framework, leveraging its state-of-the-art speed and accuracy for real-time detection.  

Key features:
- Pretrained weights for faster convergence.
- Fine-tuned on low-light car images.
- Optimized for bounding box localization and object classification.

---
```
## Training Configuration

| Parameter         | Value |
|-------------------|-------|
| Pretrained model  | yolo11s.pt |
| Image size        | 512 × 512 |
| Batch size        | 16 |
| Epochs            | 10 |
| Optimizer         | AdamW (auto-selected by Ultralytics) |
| Learning rate     | Auto (initial ≈0.002, with cosine decay) |
```
---

## 📊 Performance Metrics

**Overall Results on Test Set:**
- **Precision (P):** 0.736  
  → 73.6% of predicted boxes were correct (IoU ≥ threshold).
- **Recall (R):** 0.766  
  → 76.6% of actual cars in the test set were detected.
- **mAP50:** 0.783  
  → Mean Average Precision at IoU ≥ 0.50, showing balance between precision and recall.
- **mAP50-95:** 0.484  
  → Stricter localization quality measure, averaging AP across IoU thresholds from 0.50 to 0.95.

---

## Dataset
A **low-light car detection dataset** was used for fine-tuning.  
Images were resized to **512×512 pixels** for training consistency.

---

