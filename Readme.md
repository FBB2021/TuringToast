# 🌱 CropCare AgriScan - Crop Health Detection

This project implements an end-to-end deep learning pipeline for crop health detection, from data preprocessing and model training to real-world inference via a deployable API interface.

Model Based: MobileNet_v2

Database: PlantVillage

---

## 📋 Project Information

- **Author**: Feng Bao
- **Email**: fbb@student.unimelb.edu.au
- **Team**: TuringToast @ CodeBrew_2025

---

## 🏗️ Project Structure

| Directory | Description |
|:-----|:-----|
| `./CropCare_agricscan_api/` | API implementation for model inference |
| `./Model/` | Trained model weights (`agricsan_weights.pth`) |
| `./PlantVillage/` | Dataset containing training and testing images |
| `./Show Case/` | Real-world captured crop images for testing |

---

## ✨ End-to-End Pipeline Overview

| Component            | Status | Description |
|----------------------|--------|-------------|
| **Data Preparation** | ✅     | Utilized the PlantVillage dataset, covering multiple crop types and disease categories. |
| **Model Training**   | ✅     | Trained using MobileNet_v2, with weights saved as a `.pth` file. |
| **Model Evaluation** | ✅     | Includes a confusion matrix and analysis of accuracy and F1-score. |
| **Real-World Testing** | ✅   | The `Show Case/` folder contains real-world crop images to validate model generalization. |
| **API Integration**  | ✅     | Packaged with FastAPI, exposing a `/predict` endpoint for inference calls. |
| **Deployability**    | ✅     | Lightweight model with fast inference, easily deployable locally or in the cloud. |

---


## 📊 Model Input and Output

- **Input**: Crop leaf image (RGB, resized to 224x224 pixels)
- **Output**: Classification label indicating health status (e.g., `Prediction: Tomato_Early_blight (99.99%) Type: Tomato Issue: Early blight`)

---

## 💪 Evaluation

- Trained and validated on the PlantVillage dataset, achieving high accuracy(98%) and F1-Score(98%).
- Tested on real-world captured images to validate generalization and robustness.
- There is little to no systematic bias or confusion between different classes.
- The sample size for Potato_healthy appears relatively small (33), indicating a slight class imbalance in the dataset, which could be addressed in future iterations through sampling or class weighting.

---

# 📂 Project Directory Structure

```
.
├── CropCare_agricscan_api/    # Model API implementation
│   └── main.py                # FastAPI server entry point
│
├── Model/                     # Trained model weights
│   └── agricsan_weights.pth
│
├── PlantVillage/              # Dataset for training and validation
│   └── [Pepper/Tomato/Potato subfolders]
│
├── Show Case/                 # Real-world test samples
│   └── [Captured images]
│
└── plantvillage.ipynb         # Model training and evaluation notebook
```

---

Happy Farming 💚!

