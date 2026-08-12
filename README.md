# Edge AI for Autonomous Search & Rescue Drone

> Real-time computer vision and embedded AI pipeline for autonomous human detection and geo-localization on NVIDIA Jetson edge devices.

![Python](https://img.shields.io/badge/Python-3.8+-blue)
![PyTorch](https://img.shields.io/badge/PyTorch-Deep%20Learning-orange)
![YOLO11](https://img.shields.io/badge/YOLO11-Object%20Detection-green)
![TensorRT](https://img.shields.io/badge/TensorRT-Edge%20Inference-red)
![NVIDIA Jetson](https://img.shields.io/badge/NVIDIA-Jetson%20Nano-76B900)
![Docker](https://img.shields.io/badge/Docker-Containerized-2496ED)
![MAVLink](https://img.shields.io/badge/MAVLink-Telemetry-blue)

---

## Overview

This project focuses on the development and deployment of a real-time **Edge AI computer vision system** for autonomous search-and-rescue applications.

The system performs human detection directly on an NVIDIA Jetson edge device, enabling AI inference without requiring continuous cloud connectivity.

The main focus of this project is the **AI/ML engineering pipeline**, from deep learning inference and model optimization to embedded deployment and real-time telemetry integration.

### Main Objectives

- Real-time human detection from aerial imagery
- GPU-accelerated inference on NVIDIA Jetson
- YOLO11-based object detection
- TensorRT model optimization
- FP16/INT8 inference optimization
- Dockerized ML deployment
- MAVLink-based telemetry integration
- GPS geo-localization of detected targets
- Real-time inference serving
- Edge performance benchmarking
- Foundation for an end-to-end MLOps lifecycle

---

# System Architecture

```text
                         CAMERA
                            │
                            ▼
                  Image Preprocessing
                            │
                            ▼
                         YOLO11
                            │
                            ▼
                   TensorRT Inference
                            │
                            ▼
                     Human Detection
                            │
                 ┌──────────┴──────────┐
                 │                     │
            Bounding Box          Confidence
                 │
                 ▼
            MAVLink Telemetry
                 │
                 ▼
          GPS Geo-localization
                 │
                 ▼
           Detection Event
                 │
            ┌────┴────┐
            │         │
            ▼         ▼
         REST API  WebSocket
            │         │
            └────┬────┘
                 ▼
        Operator / Monitoring UI

AI/ML Pipeline

The core computer vision pipeline follows:

