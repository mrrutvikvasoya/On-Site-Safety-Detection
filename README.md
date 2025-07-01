# YOLOv10 and YOLOv11 Safety Detection Project

## Overview

This project aims to fine-tune and evaluate YOLOv10 and YOLOv11 models for safety detection, specifically for identifying safety helmets, safety clothing, and blurred objects in images. The models are trained on the **SFCHD-SCALE dataset**, which contains 50,559 images across 7 classes. The dataset is used to improve the detection of safety-related objects in various environments, particularly in construction and industrial settings.

## Key Features

- **Models**: YOLOv10 and YOLOv11
- **Dataset**: SFCHD-SCALE dataset ("https://github.com/lijfrank-open/SFCHD-SCALE")
- **Classes**:
  - Person
  - Safety Helmet
  - Safety Clothing
  - Other Clothing
  - Head
  - Blurred Clothing
  - Blurred Head
- **Training**:
  - 100 epochs with a batch size of 6 to 16
  - Use of class weights to address dataset imbalance
- **Results**:
  - YOLOv11 with class weights achieved superior performance with a **mAP@0.5: 0.779** and **mAP@0.5:0.95: 0.534**
  - YOLOv10 showed effective results but with lower performance compared to YOLOv11

## Results

The models were evaluated based on multiple performance metrics, including precision (P), recall (R), and mean average precision (mAP) at IoU thresholds of 0.5 and 0.95. Detailed performance metrics for both YOLOv10 and YOLOv11 are available in the results section.

### YOLOv11 with Class Weights Performance

| Class              | P    | R    | mAP50 | mAP50-95 |
|--------------------|------|------|-------|----------|
| Person             | 0.945| 0.953| 0.976 | 0.748    |
| Safety Helmet      | 0.934| 0.885| 0.941 | 0.661    |
| Safety Clothing    | 0.741| 0.838| 0.844 | 0.632    |
| Other Clothing     | 0.902| 0.952| 0.959 | 0.684    |
| Head               | 0.879| 0.647| 0.794 | 0.459    |
| Blurred Clothing   | 0.66 | 0.349| 0.413 | 0.223    |
| Blurred Head       | 0.664| 0.427| 0.529 | 0.334    |
| **mAP@0.5**        | **0.779**|    |       |          |
| **mAP@0.5:0.95**   | **0.534**|    |       |          |

### YOLOv10 with Class Weights Performance

| Class              | P    | R    | mAP50 | mAP50-95 |
|--------------------|------|------|-------|----------|
| Person             | 0.911| 0.953| 0.971 | 0.731    |
| Safety Helmet      | 0.88 | 0.9  | 0.931 | 0.648    |
| Safety Clothing    | 0.753| 0.838| 0.835 | 0.61     |
| Other Clothing     | 0.851| 0.948| 0.959 | 0.665    |
| Head               | 0.824| 0.691| 0.765 | 0.449    |
| Blurred Clothing   | 0.56 | 0.303| 0.369 | 0.197    |
| Blurred Head       | 0.717| 0.462| 0.529 | 0.335    |
| **mAP@0.5**        | **0.766**|    |       |          |
| **mAP@0.5:0.95**   | **0.519**|    |       |          |

## Installation and Setup

To get started with this project, follow these steps:

1. **Clone the repository**:
   ```bash
   git clone https://github.com/your_username/YOLO-Safety-Detection.git
   cd YOLO-Safety-Detection
