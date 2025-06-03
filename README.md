# 🚦 Traffic Sign Recognition – MLOps Pipeline

This project is a full MLOps implementation of a **Traffic Sign Recognition System** using the [GTSDB Dataset](https://www.kaggle.com/datasets/icebearogo/german-traffic-sign-detection-gtsdb-dataset). It includes data preprocessing, model training, experiment tracking, serving a REST API, monitoring, and automated retraining.

---

## 📌 Project Goals

- Train a CNN to classify German traffic signs from image data
- Track experiments with **MLflow**
- Serve real-time predictions via a **FastAPI** REST API
- Containerize training and inference using **Docker**
- Deploy scalable inference with **Kubernetes**
- Monitor system health and performance using **Prometheus** and **Grafana**
- Automate retraining using **Airflow DAGs**
- Automate build/test/deploy with **CI/CD (GitHub Actions)**

---

## 🧱 Tech Stack

| Layer              | Tools                                       |
|--------------------|---------------------------------------------|
| ML & Training       | PyTorch, TorchVision, Albumentations        |
| Experiment Tracking | MLflow                                     |
| API                 | FastAPI, Uvicorn                           |
| Deployment          | Docker, Kubernetes                         |
| Monitoring          | Prometheus, Grafana                        |
| Automation          | Apache Airflow                             |
| CI/CD               | GitHub Actions                             |
| Others              | OpenCV, Pillow, Shell, YAML                |

---

## 📁 Folder Structure

```plaintext
traffic-sign-mlops/
├── data/
│   ├── raw/               # Original Train/Test data
│   └── processed/         # Augmented/resized images
├── notebooks/             # EDA, model experiments
├── src/
│   ├── data/              # Dataset classes
│   ├── model/             # CNN and training scripts
│   ├── api/               # FastAPI app for inference
│   └── utils/             # Helpers: transforms, evaluation
├── docker/
│   ├── api/               # Dockerfile for serving model
│   └── training/          # Dockerfile for training model
├── mlruns/                # MLflow experiment tracking logs
├── k8s/                   # Kubernetes manifests
├── airflow/               # DAGs for model retraining
├── monitoring/            # Prometheus/Grafana config
├── tests/                 # Unit and integration tests
├── .github/workflows/     # CI/CD pipelines
├── requirements.txt
├── README.md
└── setup.py
