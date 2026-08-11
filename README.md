# Detection-Fusion-of-YOLO-and-RT-DETR-for-Unique-Coral-Instance-Estimation
Detection fusion of YOLOv8 and RT-DETR with Weighted Box Fusion and ByteTrack for unique coral instance estimation in underwater videos.
# Detection Fusion of YOLOv8 and RT-DETR for Unique Coral Instance Estimation

An automated deep learning framework for detecting, tracking, and estimating unique coral instances from underwater images and videos.

## Overview

Coral reef monitoring is challenging due to poor underwater visibility, lighting variations, complex coral structures, and repeated appearances of the same coral across video frames. This project proposes a detection-fusion-tracking framework that combines YOLOv8 and RT-DETR to improve coral detection completeness and tracking consistency.

The framework consists of three main stages:

1. **Dual-Detector Detection** – YOLOv8 and RT-DETR are trained using a two-stage domain adaptation approach. The models are first trained on AIMECORAL1 and subsequently fine-tuned on AIMECORAL2.
2. **Detection Fusion** – Predictions from both detectors are combined using Weighted Box Fusion (WBF) at the inference level to produce refined detections and recover coral instances detected by only one model.
3. **Multi-Object Tracking** – The fused detections are passed to ByteTrack to maintain coral identities across consecutive video frames. Stable tracking IDs and average track length are used to evaluate tracking consistency and estimate unique coral instances.

## Datasets

- **AIMECORAL1:** 580 images from the Southwest Indian Ocean
- **AIMECORAL2:** 282 images from New Caledonia, Pacific Ocean

## Models and Techniques

- YOLOv8
- RT-DETR
- Two-stage domain adaptation
- Weighted Box Fusion (WBF)
- ByteTrack
- Multi-object tracking
- Unique coral instance estimation

## Results

| Model | Precision | Recall |
|-------|-----------|--------|
| YOLOv8 | 87.15% | 83.28% |
| RT-DETR | 86.21% | 87.96% |
| Fusion Model | 53.09% | **97.66%** |

The fusion approach substantially improves recall, helping recover more coral instances that may be missed by individual detectors. It also provides more continuous detections for tracking, resulting in improved tracking consistency.

## Applications

The proposed framework can support automated coral reef monitoring by reducing manual monitoring effort and enabling more efficient analysis of underwater video data.

## Keywords

Coral Reef Monitoring, YOLOv8, RT-DETR, Weighted Box Fusion, WBF, ByteTrack, Object Detection, Multi-Object Tracking, Deep Learning, Underwater Vision, Coral Instance Estimation
