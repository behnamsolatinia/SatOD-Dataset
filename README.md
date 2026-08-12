# Satellite Object Detection Dataset 🌍

This repository contains a lightweight, carefully annotated dataset designed for Small Object Detection (SOD) in satellite and aerial imagery, specifically formatted for YOLO architectures.

## 📂 Dataset Structure
The dataset is structured in the standard YOLO format and includes two primary classes: **Airplane** and **Car**.

```text
SatOD-Dataset/
├── data.yaml
├── train/
│   ├── images/
│   └── labels/
├── valid/
│   ├── images/
│   └── labels/
└── test/
    ├── images/
    └── labels/

```
## 🚀 How to Use (Google Colab / Local)
You can directly clone this repository and start training your YOLO models without any extra configuration.
### 1. Clone the repository
```text
git clone [https://github.com/behnamsolatinia/SatOD-Dataset.git](https://github.com/behnamsolatinia/SatOD-Dataset.git)

```

### 2. Train a YOLO model
```text
from ultralytics import YOLO

# Load a pre-trained YOLO model
model = YOLO('yolov9m.pt')

# Train the model using the provided data.yaml
results = model.train(
    data='SatOD-Dataset/data.yaml', 
    epochs=100, 
    imgsz=640,
    batch=16
)
```
---

## 📖 Citation

If you use this dataset in your research or academic projects, please consider citing this repository. 

```bibtex
@misc{satod_dataset_2026,
  author = {Solatinia, Behnam},
  title = {SatOD-Dataset: A Lightweight Aerial and Satellite Imagery Dataset for Small Object Detection},
  year = {2026},
  publisher = {GitHub},
  journal = {GitHub repository},
  howpublished = {\url{[https://github.com/behnamsolatinia/SatOD-Dataset](https://github.com/behnamsolatinia/SatOD-Dataset)}}
}
```
