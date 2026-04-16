
---

# 🚀 MLOps End-to-End Pipeline – Production Ready

## 📌 Overview

This project demonstrates a **complete end-to-end MLOps pipeline**, covering everything from data ingestion to deployment using modern tools and industry practices.

It integrates:

* Data Engineering
* Model Training
* Cloud Deployment
* CI/CD Automation

The goal is to build a **scalable, reproducible, and production-grade ML system**.

---

## 🧠 Key Features

✨ Modular pipeline architecture
✨ MongoDB Atlas integration (cloud database)
✨ Automated data validation & transformation
✨ Model training, evaluation & versioning
✨ AWS S3 model registry
✨ Docker-based containerization
✨ CI/CD pipeline using GitHub Actions
✨ Deployment on AWS EC2

---

## 🏗️ Project Architecture

```
├── src/
│   ├── components/
│   ├── configuration/
│   ├── entity/
│   ├── data_access/
│   ├── aws_storage/
│
├── notebook/
├── artifacts/
├── static/
├── templates/
│
├── app.py
├── Dockerfile
├── requirements.txt
├── setup.py
├── pyproject.toml
```

---

## ⚙️ Tech Stack

### 💻 Programming & ML

* Python 3.10
* Pandas, NumPy, Scikit-learn

### 🗄️ Database

* MongoDB Atlas

### ☁️ Cloud Services

* AWS S3 (Model Registry)
* AWS EC2 (Deployment)
* AWS ECR (Docker Image Storage)

### 🔄 DevOps & MLOps

* Docker
* GitHub Actions (CI/CD)
* DVC (optional)
* Logging & Exception Handling

---

## 🔄 End-to-End Pipeline Workflow

### 1️⃣ Data Ingestion

* Data fetched from MongoDB
* Converted from key-value format → DataFrame
* Stored as artifacts

### 2️⃣ Data Validation

* Schema validation using YAML
* Missing values & data consistency checks

### 3️⃣ Data Transformation

* Feature engineering
* Data preprocessing pipelines

### 4️⃣ Model Training

* Model training with configurable parameters
* Custom estimator implementation

### 5️⃣ Model Evaluation

* Performance comparison with previous model
* Threshold-based acceptance

### 6️⃣ Model Pusher

* Upload trained model to AWS S3 bucket

---

## ☁️ MongoDB Setup

* Create MongoDB Atlas account
* Create cluster (M0 free tier)
* Add IP: `0.0.0.0/0`
* Get connection string (Python driver ≥ 3.6)

```bash
export MONGODB_URL="your_connection_string"
```

---

## ☁️ AWS Setup

### IAM Configuration

* Create IAM user
* Assign `AdministratorAccess`
* Generate access keys

### Environment Variables

```bash
export AWS_ACCESS_KEY_ID="your_key"
export AWS_SECRET_ACCESS_KEY="your_secret"
```

### S3 Bucket

* Bucket name: `my-model-mlopsproj`
* Region: `us-east-1`

---

## 🐳 Docker Setup

```bash
docker build -t mlops-project .
docker run -p 5080:5080 mlops-project
```

---

## 🔁 CI/CD Pipeline

### GitHub Actions Workflow

* Triggered on every push
* Builds Docker image
* Pushes to AWS ECR
* Deploys to EC2

### Required Secrets

```
AWS_ACCESS_KEY_ID
AWS_SECRET_ACCESS_KEY
AWS_DEFAULT_REGION
ECR_REPO
```

---

## 🚀 Deployment (AWS EC2)

### Steps:

* Launch Ubuntu EC2 instance
* Install Docker
* Configure self-hosted GitHub runner
* Open port `5080`

Access app:

```
http://<EC2_PUBLIC_IP>:5080
```

---

## 🌐 Application Features

* Web interface for predictions
* `/training` endpoint for model retraining
* Fully automated pipeline execution

---

## 📊 Logging & Monitoring

* Custom logging system
* Exception handling for debugging
* Pipeline tracking via artifacts

---

## 📦 Installation

```bash
conda create -n vehicle python=3.10 -y
conda activate vehicle
pip install -r requirements.txt
```

---

## 📌 Future Improvements

* Add model monitoring (drift detection)
* Integrate MLflow for experiment tracking
* Kubernetes deployment
* Auto-scaling inference

---

## 🤝 Contribution

Feel free to fork, improve, and contribute 🚀

---

## ⭐ Why This Project Stands Out

This is not just a machine learning model — it’s a **production-ready system** that demonstrates:

✔ Real-world MLOps practices
✔ Cloud-native deployment
✔ Automation & scalability
✔ Clean architecture

---
